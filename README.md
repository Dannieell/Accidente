Proyecto Individual 2

Para este proyecto individual vamos asumir el rol de data analitycs, donde se nos encormadara un datasets de homicidios, donde refiere data de accidentes fatales para la 
Cuidad Autonoma de Buenos Aires. El objetivo del proyecto es realizar un EDA consistente y usar alguna herramienta de visaulizacion de datos ya sea tablue, power bi o stream li
para realizar los graficos, usar metricas, hallar KPI's todo ello organizado en un dashboard. El dashboard se va tener que argumentar en el Demo y explicar las tendencias, registros 
y discuciones de la data, segun nuestro trabajo realizdo.

1. EDA

El notebook EDA, realizamos el analisis exploratorio de datos con el objetivo de:

*  Tener una familiaridad con los datos de homocidios.xlxs, se entiende entonces que tiene buena calidad de datos y obtenemos una mejor compresion de la estructura de los datos.
* Mediante algunos gráficos de barras y resumen de datos pudimos obtener información valiosa sobre los datos y tambien tenemos una nocion de la hipotesis sobre las victimas de accidentes
   fatales en la Cuidad Autonoma de Buenos Aires (CABA)
* Detectamos valores atípicos y abordamos adecuadamentemente mediante imputación de datos
* Preparamos los datos de tal manera, que el analisis en power bi, se realiza de manera mas ligera sin utilizar muchas transformaciones

Pasos Realizados en el notebook:

* Importación de Librerías: Se importan las liberias habituales que utilizan para realizar el EDA como: pandas, os, numpy, matplotlib.pyplot, seaborn, datetime, etc.
* Carga del datasets: Realizamos la carga del dataset homicidios.xlxs, como se puede verificar tenemos 2 tablas distintas, por lo cual, lo convertimos en 2 dataframes distintos para hacer la manipulacion de datos
* Verificación de tipos de datos: Realizamos una verificación rápida de los tipos de datos en cada columna
* Eliminación de columnas irrelevantes: Eliminamos las columnas que no aportan al analisis de los datos, son redundantes o tiene valores nulos
* Conversión de datos: Realizamos conversiones de datos, es decir, le damos el tipo de dato apropiado a cada columna de nuestro dataframe

Como primer resultamos de este 1er analisis obtenemos 2 dataframes depurados, sin embargo, observamos que podemos realizar una separacion aun mas fina, es decir, obtener 3 dataframes con caracteristicas unicas y que estan unidos mediante su 'Id' de accidentes, con el principal objetivo de preparar, adaptar y optimizar los datos para su posterior analisis en power bi. Por lo tanto, los dataframes finales son: 

1. Tiempo: Se observa columnas como fecha, anio, hora, mes, etc.  
2. Ubicacion: Se oberva columnas como altitud,longitud, tipo de calle, etc.
3. Accidente: Se oberva columnas como Rol, Victima, Seco, Edad, Acudado, etc.

Con estos nuevos dataframes se realizar los graficos para verificar las tendencias, se hace analisis univariado, analisis bivariado, mapa geográfico y distribución de los datos. Para resumir se comentan las conclusiones obtenidas en cada dataframe:

1. Tiempo: Los acciddentes viales en CABA en los anos 2016 al 2021 tiene presentan las siguientes conclusiones:

* Hay una tendencia a la disminuacion de los accdientes viales en los ultimos anos, esto es debido a las medidas de confinamiento por el Covid-19, sin embargo despues de la pandemia aun se observa esa tendencia a la baja
* Los ultimos meses de fin de ano representan siempre un alza en los accidentes viales, esto debido a que la poblacion en esa epoca del ano realizan numerosos traslados por las avenidas
* Las 7 horas representan mas accdidentes viales que en toda las demas horas, sienda en hora de la manana donde se debe realizar mas fiscalizacion
* Las horas de la madrugrada y horas despues de almuerza representan la menor cantidad de accidentes, debido a la escazes de trafico en las calles y tambien por la limunosidad de las calles, respectivamente
* El ano 2020 del mes diciembre se produjo la maoyr cantidad de accidentes viales en el periodo del 2016-2020, justo despues de la reanudacion de las actividades por e confinamiento

2. Ubicacion: Los acciddentes viales en CABA en los anos 2016 al 2021 tiene presentan las siguientes conclusiones:

* El tipo de calle 'Avenida' representa las de 400 accidentes fatales, siendo el tipo de calle mas peligroso de CABA
* La comuna 1 tiene mas accidentes fatales que todas las demas comunas esto debido a su densidad poblacional
* Las regiones sur y este de CABA tiene una mayor cantidad de accidentes fatales con respecto a los demas puntos cardinales, siendo la ubiacion de las comunas mas pobladas

3. Accidente: Los acciddentes viales en CABA en los anos 2016 al 2021 tiene presentan las siguientes conclusiones:

* Por encima de lo que normalmente se cree el conductor es quien termina con la mayor cantidad de fallecimiento seguido por los peatones
* La moto al ser un vehiculo livino y sin proteccion representan mas de 300 muertes en los 5 anos
* El sexo femenino no es ni la mitad de las victimas del sexo masculino, esto quiere decir, que las muejeres son mas prudentes en la conduccion
* La mayor cantidad de fallecimiento esta en el rango etario de los 21 a los 30 anos

2. POWER BI

El aricho se llama Siniestros.pbix, donde se tuvo en cuenta el tipo de graficos, los colores de fondo, las formas, el patron Z e iteratividad para obtener las siguientes dos paginas:

2.1. Generalidades: Donde acontuniacion se describe el trabajo realizado.

* Victimas Fatales: Es una tarjeta donde cuenta todos los accidentes fatales entre los anos 2016 al 2021, sin excepcion.
* Luego se tiene 3 tarjetas con unos iconos de hombre, mujer y desconocido para dar alucion a los porcentaje de los accidentes por genero
* En la parte izquierda se tiene 4 filtros donde se obtiene resultados interesantes, estos filtros son: Sexo, Acusado, Dia de la Semana y Comuna, con estos filtros se busca tener un analisis mas detallado y hacer enfasis segun lo que requiera el usuario, ademas podemos observar que las graficas en algunas ocasiones seguir la tendencia global y en otras van a contracorriente.
* Despues se tiene un grafico de barras apiladas donde se realiza el analisis de mes a mes en todos los anos, como se realizo la hipotesis que a fin de ano ocurren mas accidentes, este grafico revela que efectivamente diciembre seguido de noviembre representan la mayor cantidad de victimas fatales
* Tambien se tiene un grafico embudo, donde se analiza que el rango etario entre los 21 a 30 anos tiene la maor cantidad de fallecidos, esto quiere decir que los adultos jovenes son los que tienen mayor probabilidad de morir en un accidente vial
* Ademas se tiene un grafico circular por el tipo de calle donde ocurre la mayor cantidad de victimas siendo esta la 'Avenida', seguido por 'Calle'
* Tambien se tiene un grafico de anillos donde se obseva que el 46% de victimas hacian el rol de conductor y 37% de victimas eran peatones de CABA
* Adiconalmente se tiene un mapa de ubiacion de siniestros de CABA donde claramente se observa una densidad mayor de accidentes en l sur y este de la cuidad, esto debido por la cantidad poblacional y las abundantes avenidas en dichos lugares
* Finalmente, se tiene el grafico de ano y mes donde se observa una tendencia a la baja de los accdientes, inclusive despues del pico de la reanudacion de las actividades post pandemia el grafico indica que en el ano 2021 los accidentes se han reducido con respecto a los anos anteriores

2.2. Indicadores: 

Para los indicadores se han considerado 3 KPI's que son KPI motocicleta: que indica el porcentaje si hubo un aumento o una disminucion con respecto al ano anterior con respecto a las victimas de motocicleta, para el que KPI haya cuplido su meta debe estar tener una reduccion del 7% con respecto al ano anterior, KPI peaton: KPI importante ya que mide nuevamente el % de aumento o disminucion por victimas que son peatones para que se cumpla la meta hemos considerado una reduccion del 15% con respecto al ano anterior, es interesante observar esta grafica ya que, las victimas de peatones se mantienen casi estables entre un ano a otro, salvo 2018, donde el KPI se disparo y por ultimo tenemos KPI Homicidios donde evalua si hubo una reduccion o aumento de manera semestral una reduccion del 10% con respecto al mes anterior seria un buen semenestre.

Para hallar estos KPI's se realizo lo siguiente:

* Primero se creo la tabla KPI que tiene las siguientes columnas Ano, Moto (cantidad de victimas de moto), KPI Moto (ya explicado), Peton (cantidad de victimas que son peatones ) y KPI Peaton
* Luego se creo la tabla KPI Homicidios, donde se tienen las siguientes columnas: Semestre, Anio, Poblacion (de CABA), Homicidios (Nro. de muertos), Tasa de Homicidios y KPIHomicidios
* Despues de colocan los filtros de tiempo para el caso KPIHomicidios se tiene el filtro de semestre y para los casos de KPI moto y KPI peaton el filtro de tiempo Ano, esto con el objetivo de si queremos ser especifimos con el tiempo podamos realizarlo de manera iterativa
* Luego para los tres casos se han aplicado graficos de barras con linea, donde las barras representan la cantidad de victimas ya sea totales, motos o peatones y la linea pueda observar la tendencia de estos KPIs, luego en la parte de leyenda se puede observar la variacion porcentual entre los semestres o anos
* Finalmente se tiene una matriz para cada grafico donde nuevamente se detalla el el tiempo, la cantidad de muertos y los KPIS, adicionalmente se realiza un formato condicional para los iconos donde si cumple con el objetivo descrito va salir un check en verde caso contario un aspa en rojo.

Para concluir con los Indicadores se tiene la siguientes concluiones:

* Las motos son la forma de vehiculos mas peligrosa para CABA, sin embargo, 


