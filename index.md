# Tasa de Desocupación Durante la Pandemia

INTEGRANTES:
- Tomas Oyaneder
- Ziyu Guo
- Víctor Bórquez

## DEFINICIONES CLAVES

- La Tasa de Desocupacion expresa el porcentaje de personas desocupadas dentro de la fuerza de trabajo, este último concepto reifere a todas personas mayores de 15 años que se encuentran vinculadas con el mercado laboral.
- Cuando se hable acerca de la 'positividad' en este proyecto nos estamos refiriendo al porcentaje de PCR que otorgan resultado positivo.

En este proyecto se utilizaron datos de la pandemia (que serán explicados más adelante) recopilados del Ministerio de Ciencia, Tecnología, Conocimiento e Innovación ([link al repositorio](https://github.com/MinCiencia/Datos-COVID19/)) y además; datos de la Tasa de Desocupación que fueron obtenidos desde la Base de Datos Estadísticos del Banco Central ([link a la pagina](https://si3.bcentral.cl/Siete/ES/Siete/Cuadro/CAP_EMP_REM_DEM/MN_EMP_REM_DEM13/ED_TDNRM2)).

Como el propósito del proyecto es intentar relacionar los efectos de la pandemia al trabajo de los chilenos, nuestro analisis se enfocara entre __Marzo 2020 y Septiembre 2021__ ya que a nuestro criterio son los meses donde se puede evidenciar de mejor manera el efecto de la pandemia, debido a por ejemplo las restricciones sanitarias respecto al denominado __"Plan Paso a Paso"__.

### Data Tasa de Desocupación

Datos recopilados gracias a la utilización de la API del Banco Central, luego de trabajar y ordenar los datos podemos generar un gráfico que muestra la Tasa de Desocupación en el tiempo de todas las Regiones

![Im](/content/images/tasas_regiones.png)

Al observar el gráfico nos damos cuenta que entre Junio y Octubre de 2020 en practicamente todas las regiones se puede evidenciar un aumento considerable en la tasa de desocupación, por lo que ahora habría que revisar que es lo que pasa con los Datos de la pandemia durante este rango de meses


### Data Covid-19
#### Cantidad de positivos mensuales:
Primero utilizaremos la información correspondiente a la cantidad de casos registrados por region, por lo que modificamos la informacion del archivo 'CasosTotalesCumulativo_T.csv' ubicado en [esta carpeta del repositorio](https://github.com/MinCiencia/Datos-COVID19/tree/master/output/producto3).

Al graficar los resultados por región obtenemos lo siguiente:

![Imagen](/content/images/casos_por_region.png)

Debido a que tener 2000 contagiados por mes en la región Metropolitana (donde viven 7 millones de personas) es muy distinto a tener 2000 contagiados en la Región de los Ríos (donde viven 360 mil habitantes), entonces agregamos un nuevo dataframe al analisis, correspondiente a la cantidad de PCR realizados por mes por región

[PARA MAYOR INFORMACIÓN](/content/pages/covid1.md)

#### Pcr mensuales:

Debido a que la cantidad total de casos era una variable muy general, decidimos ocupar un dataframe (perteneciente al mismo repositorio) que contiene información sobre la cantidad de PCR realizados por comuna.

![Imagen](/content/images/positividad_porcentaje.png)

A primera vista tenemos un grafico algo desordenado y complicado de leer cuando uno intenta identificar una region en especifico, hay colores que se repiten debido a la cantidad de regiones por lo cual tendremos que cambiar nuestra manera de vizualizar los datos

[ANALISIS POR TRAMOS DE MESES](/content/pages/pcr1.md)

#### Evolución Plan Paso a Paso

Utilizaremos los datos de la evolución de las comunas respecto al Plan Paso a Paso del gobierno, ya que dependiendo la fase existían restricciones tales como cuarentena los fines de semana, aforos reducidos; que implica tener menos personal por lo que en teoría la tasa de desocupación debería ser mayor si la comuna o región esta en una peor fase.

Para realizar este analisis nos enfocaremos en la fase que estuvo (en promedio) la capital de la región.

![Imagnn](/content/images/paso_a_paso.png)

Debido a que el Plan Paso a Paso fue implementado recién desde Julio de 2020, por la gran cantidad de casos, el gobierno tomo esta medida que puede ser un factor clave a considerar respecto al alza en la tasa de desempleo justamente entre los meses de Julio y Octubre de 2020, ya que si no se puede salir de las casas es muy probable que el Desempleo aumente, por lo que la tasa de Desocupación en consecuencia también debería aumentar