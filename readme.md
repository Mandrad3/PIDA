# DATA SCIENCE - PROYECTO INDIVIDUAL Nº2
# Data Analytics

Este proyecto abarca una serie de pasos para desarrollar un proceso de **`Data Analytics`** sobre un dataset de accidentes aéreos, para posteriormente disponibilizar un **`Dashboard Interactivo`** utilizando **`Power BI`**.

## Contexto

Se plantea la necesidad de analizar datos históricos de **`accidentes aéreos`** a los efectos de identificar patrones, tendencias y factores que ayuden a mejorar la seguridad en la aviación civil. 

## Dataset

El [dataset](https://github.com/fedeandresg/2-proyecto-individual-Data-Analytics/blob/main/AccidentesAviones.csv) en cuestión posee información acerca de vuelos que han sufrido un siniestro a lo largo de todo el mundo desde 1908 hasta 2021. El mismo cuenta con 5008 filas (representando cada fila un accidente aéreo) y 18 columnas (atributos de cada vuelo).

## Objetivo

El propósito del trabajo fue describir las características de vuelos siniestrados a los efectos de analizar los siguientes **`KPI's`** propuestos:

- Reducción en un 5% de la **`tasa anual de mortalidad`** (personas fallecidas/personas a bordo);
- Aumento en la **`tasa anual de supervivencia`** (personas sobrevivientes / personas a bordo) para aerolíneas con gran cantidad de accidentes históricos ;
- Evolución de accidentes aéreos y comparación con métricas para definir **`tendencia`**;
- Disminución de la **`cantidad de accidentes`** para el país con mayor cantidad de siniestros.

## ETL  

Para realizar los procesos de ETL se utilizó **`Python`** con librerías de Numpy, Pandas, Matplotlib y Seaborn, entre otras.

## Análisis exploratorio de datos

A los efectos de poder entender los datos presentados, se realizaron una serie de análisis y estudios sobre las variables del dataset a los efectos de poder encontrar relaciones entre los datos y comprender la relevancia de los mismos.
Dentro de los análisis efectuados se encuentran: 
- Nubes de palabras para identificar causas comunes en las descripciones de los accidentes;
- Distribuciones de frecuencias y estadísticas de las variables numéricas;
- Análisis e identificación de outliers en variables de interés (total_aboard y total_fatalities);
- Identificación de variables categóricas y sus valores; 
- Análisis de accidentes, tasa de mortalidad, tasa de supervivencia y seguridad en vuelos por: país, aerolínea, aeronave, marca de aeronave y categoría de vuelo;
- Análisis temporales por hora, día, mes y año.

## Dashboard

el Dashboard se encarga de analizar los accidentes y la cantidad de pasajeros con sus respectivas tendencias a lo largo del tiempo.
Podemos destacar que no siempre existe una relación directa entre la tendencia de accidentes por período y la cantidad de pasajeros (véase en tendencia mensual).
Por otro lado se pueden analizar la cantidad de accidentes a lo largo de los años con la media móvil de 10 períodos, lo cual nos permite concluír que los años donde la cantidad de accidentes se ha encontrado por debajo de la media móvil, han resultado años con baja siniestralidad, mientras que aquellos años donde la cantidad ha estado por encima han sido años con una gran cantidad de accidentes (años entre 1946 y 2004). Dicha media móvil puede ser ajustada en función de las circunstancias del futuro. Tal es así que podemos inferir que a nivel mundial estamos en una tendencia a la baja en cantidad de accidentes desde 1989 (año en que comienza a descender la cantidad de accidentes) y por debajo del promedio móvil de 10 años en los años siguientes por lo que resulta interesante mantenerse por debajo de dicho patrón para los próximos años.
Por último analizamos la variación interanual de accidentes y podemos filtrar por países como Estados Unidos para observar cómo se ha comportado en los últimos años pese a tener la mayor cantidad de accidentes y pasajeros históricos.

## Conclusiones

- La tendencia anual de accidentes a lo largo de la historia comenzó una gran tendencia alcista desde los días de los primeros vuelos hasta 1945. La tendencia pudo consolidarse entre 1946 y 2004 para finalmente romper la zona de acumulación en 2005 (año en que confirmamos la tendencia a la baja comenzada en 1989). La media móvil de 10 años nos ayuda a visualizar años de baja siniestralidad, por lo que se alienta a mantenerse por debajo de la misma y activar alertas en el momento en que la tendencia anual se aproxime a la misma (situación que ha acontecido numerosas veces a lo largo de la historia). Es positivo a su vez, poder afirmar que la aviación ha alcanzado un nivel de seguridad que permite estar en los niveles de accidentes más bajos de la historia, considerando la cantidad de vuelos, personas transportadas y avances tecnológicos en contraposición a los primeros días;
- Por último es destacable la tendencia anual de accidentes para los países como Estados Unidos y Rusia, los cuales pese a tener la mayor cantidad de accidentes históricos, mantienen marcadas tendencias a la baja en los últimos años, en concordancia con la tendencia mundial. 