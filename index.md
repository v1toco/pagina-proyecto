# Tasa de Desocupación Durante la Pandemia

INTEGRANTES:
- Tomas Oyaneder
- Ziyu Guo
- Víctor Bórquez

En este proyecto se utilizaron datos de la pandemia (que serán explicados más adelante) recopilados del Ministerio de Ciencia, Tecnología, Conocimiento e Innovación ([link al repositorio](https://github.com/MinCiencia/Datos-COVID19/)) y además; datos de la Tasa de Desocupación que fueron obtenidos desde la Base de Datos Estadísticos del Banco Central ([link a la pagina](https://si3.bcentral.cl/Siete/ES/Siete/Cuadro/CAP_EMP_REM_DEM/MN_EMP_REM_DEM13/ED_TDNRM2)).

Como el propósito del proyecto es intentar relacionar los efectos de la pandemia al trabajo de los chilenos, nuestro analisis se enfocara entre __Marzo 2020 y Septiembre 2021__ ya que a nuestro criterio son los meses donde se puede evidenciar de mejor manera el efecto de la pandemia, debido a por ejemplo las restricciones sanitarias respecto al denominado __"Plan Paso a Paso"__.


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


For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/v1toco/pagina-proyecto/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
