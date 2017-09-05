# Laboratorio-03-Bioinformatica-0x-

## Nombre: Byron Guzmán Marín

## Profesor(a): Katterinne Méndez Carrasco


## Parte 1: El artículo genoma

## Responde:
__¿Cuántos genomas han sido depositados en GOLD? ¿Son los mismos de GENBANK?__

Al realizar la busqueda en la base de datos de GOLD se encuentraron 64.754 genomas reportados en GOLD (Complete Projects 11.598 and Incomplete Projects 53.156), en tato en relación al GENBAK no son los mismos, ya que en GENBAK se encuentran 80.576

__¿Cuál es la distribución de procariontes y eucariontes secuenciados?__

En GOLD, para establecer una razón de los organismos secuenciados entre eucariontes y procariontes, se encuentra un total hasta la fecha de  80.576; donde las entradas respecto a eucariontes es de 3.325, y si para procariontes se incluyen las entradas para bacterias, con un número de 68.574 entradas, y archeas con 728 (ausentando las entradas referentes a virus).

__Evaluando un ensamblaje de genomas.__

__Responde:__

__¿Qué es el N50, L50, NG50?__

En primer lugar, el N50 es una medida estadística que define la calidad un montaje de secuencias, que dado un conjunto de contigs con longitudes definidas, el N50 es la longitud más corta de la secuencia al 50% del genoma, es decir, que el número de bases de todos los contigs más cortos que el N50 serán más cercanas al número de bases de todos los contigs más largos al N50. El L50 por su parte, que dado un set de contigs y cada uno con su propio largo, esta medida corresponde al menor número de contigs cuya sumatoria de los largos produce el N50. El NG50, es una medida estadística similar al N50, excepto que corresponde al 50% del tamaño del genoma conocido o estimado, que debe de ser la longitud del NG50 o más largo. 

__¿Cuál es el propósito de calcular estas estadísticas?__

El propósito del cálculo de estas estadísticas, es que al utilizarse en un conjunto de longitudes contigs o scaffolds, el N50 es como la media o mediana de las longitudes, pero tiene una mayor importancia por sobre los contigs más largos, utilizándose mayoritariamente para montaje de genomas, especialmente para referenciar longitudes contigs dentro de un montaje preliminar. El L50 se utiliza al corresponder al número de contigs cuya suma de longitudes resulta en el N50. Y sobre el NG50, permite comparaciones significativas entre distintos montajes al referirse más hacia el tamaño del genoma que el tamaño del montaje como lo hace N50, donde la comparación entre valores N50 derivados de montajes con longitudes bastante diferentes, usualmente no es informativo, por lo que se recurre en este contexto al NG50.

__¿Cuál es el genoma que escogiste? Adjunta la referencia.__

 Neurospora crassa </em> OR74A. Por un asunto de falta de información, no se escogieron las otras entradas al no encontrarse una publicación de referencia para su genoma, por lo que el genoma OR74A fue el seleccionado al contener una referencia completa (segunda publicación listada).

https://www.dropbox.com/s/wbwoqdwj5xjrewl/foto%20de%20pantalla.jpg?dl=0

__Referencia:__

Maccallum I1, Przybylski D, Gnerre S, Burton J, Shlyakhter I, Gnirke A, Malek J, McKernan K, Ranade S, Shea TP, Williams L, Young S, Nusbaum C, Jaffe DB. (2009). <em>ALLPATHS 2: small genomes assembled accurately and with high continuity from short paired reads.</em> Genome Biol. 2009; 10(10): R103. 

__¿Cuál es el N50 del genoma que escogiste? ¿Y el NG50?__

De acuerdo a la Tabla 1 del artículo (data de referencia), el N50 para <em> N. crassa </em> es de 665 kb. El NG50 no se encuentra listado.

https://www.dropbox.com/s/fu2njss31uln9i2/foto%20de%20pantalla%202.jpg?dl=0

__¿Qué tipo de tecnología se uso para secuenciar el genoma que escogiste?__

En la investigación citada, se utilizaron reads de 36 bases (fragmentos) y 26 bases (jumping) de 5 genomas microbianos con composición GC variable con tamaños hasta 40 Mb. Para secuenciar el genoma de <em>N. crassa</em>, se utilizó la tecnologia ALLPATHS2, el cual es un montador (assembler) de genomas completos el cual puede generar montajes de genomas de alta calidad utilizando reads cortos; y comparando estos resultados al utilizar los algoritmos Velvet (para montajes de genomas <em> de novo </em> y secuencias de alineamiento de reads cortos, utilizado para construir secuencias continuas de forma rápida) y EULER-SR (programa para montaje de reads <em> de novo </em> que contiene programas para la correción de errores en reads cortos). Se demostró que ALLPATHS2, generó montajes con contigs y scaffolds largos y precisos, siendo los programas EULER-SR y Velvet menos precisos.

__¿Qué organismo escogiste, cuántos cromosomas tiene tu organismo y cuál es su tamaño?__

El organismo <em> Neurospora crassa </em>, con un tamaño de genoma de 39226 kb, teniendo 7 cromosomas. 

## Parte 2: Predicción de genes

## Responde:

__¿Cuántos ORF o genes encontró ORFfinder?__

ORFfinder encontró 7 ORFs o genes.

https://www.dropbox.com/s/p5bowtvjotkmpqs/fot.jpg?dl=0

__¿Cuántos ORF o genes encontró Glimmer?__

GLIMMER encontró 10 ORFs o genes.

https://www.dropbox.com/s/d4kqqwn1563jqqn/Captura%20de%20pantalla%202017-09-01%20a%20la%28s%29%2016.47.49.png?dl=0

__¿Alguno de los genes predichos por estas herramientas coinciden?__

Para establecer coincidencias entre ambos programas, deben de poseer un mismo inicio/final y marco de lectura (frame), pero pese a esto solo se encuentra coincidencia en el primer ORF/gen que ambos encontraron,  terminan en 909, con +1 en el marco de lectura pero no comienzan ambos en 1, en el cual también se esperaba que algunos ORF/gen con GLIMMER presentaran coincidencias inversas con el arguemnto de que en GLIMMER, si el transcrito se ubica en la hebra complementaria, la lectura será negativa al estar en la hebra negativa, por lo que la lectura se muestra en dirección reversa; pero en si no se encontro estas coincidencias en los genes predichos

__¿En qué hebra están codificados?__

En ORFfinder, el primero se ubica en la hebra directa, al ir de 1-->909, mientras que las otras, se ubican en la hebra complementaria al tener un marco de lectura reverso. En GLIMMER, se ubican en la complementaria como por ejemple los orf002 y orf003 al ir de 1884-->909 y 1436-->948, respectivamente.

__¿Qué tipo de programa es GLIMMER? ¿Ab initio o por homología?__

 En primer lugar, <em> ab initio </em> que se refiere a "desde el principio", en Bioinformática, se refiere a buscadores de genes que usan modelos estadísticos para predecir genes desde solamente la secuencia genómica. Por su parte, GLIMMER corresponde a un programa <em> Ab initio </em> al ser un sistema para la búsqueda de genes en DNA microbial, utilizando la medida estadística de modelos de Markov interpolados para identificar regiones codificantes, a partir de una secuencia genómica.

## Búsqueda en BLAST

## Describe los resultados encontrados con respecto a los genes que encontraste con GLIMMER y ORFfinder

Al realizar una búsqueda en BLAST, los genes encontrados con GLIMMER y ORfinder provienen del organismo <em>Haemophilus influenzae</em>, donde el primer gen encontrado en ORFfinder (de 1 a 909), corresponde al gen FdhE, el cual codifica a la enzima formato deshidrogensasa; el cuarto listado (de 1388 a 948), es el gen Riml, que codifica a la proteína ribosomal-alanina N-acetiltransferasa;  y cabe mencionar que el tercer gen encontrado  en ORFfinder (de 1433 a 1531) y septimo gen encontrado  en ORFfinder (598-455), no muestran resultados en BLAST ("No significant similarity found"), en donde al dirigirse al FAQ de BLAST, este error puede deberse a que alineamientos cortos pueden estar sobre el valor umbral default del valor Expect (parámetro que describe el número de "hits" que uno puede esperar para ver por chance cuando se realiza una búsqueda en la base de datos) y por lo tanto, no se entregan resultados respecto a esa secuencia.
