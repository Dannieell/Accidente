# Accidentes Viales

Soy Daniel Gomero y soy profesional en analisis de datos, actualmente estoy trabajando en proyecto independiente, donde me han proporcionado un conjunto de datos de homicidios que contiene información sobre accidentes fatales en la Ciudad Autónoma de Buenos Aires (CABA). La metodología para este proyecto es realizar un Análisis Exploratorio de Datos (EDA) consistente en Visual Studio COde y utilizar Power BI para crear gráficos, utilizar métricas, hallar KPIs y organizar todo ello en un dashboard. 

## 1. EDA
   
En el notebook de EDA, realizamos el análisis exploratorio de datos con los siguientes objetivos:

* Familiarizarnos con los datos del archivo homicidios.xlsx, comprendiendo su calidad y estructura.
* Utilizar gráficos de barras y resúmenes de datos para obtener información valiosa sobre los datos y tener una noción de las hipótesis sobre las víctimas de accidentes fatales en la Ciudad Autónoma de Buenos Aires (CABA).
* Detectar valores atípicos y abordarlos adecuadamente mediante imputación de datos.
* Preparar los datos para su posterior análisis en Power BI de manera más eficiente, minimizando la necesidad de transformaciones adicionales.
  
### Pasos Realizados en el notebook:

* Importación de Librerías: Importamos las librerías habituales para realizar el EDA, como pandas, os, numpy, matplotlib.pyplot, seaborn, datetime, etc.
* Carga del dataset: Cargamos el conjunto de datos homicidios.xlsx, el cual consta de 2 tablas distintas. Convertimos estas tablas en 2 dataframes diferentes para su manipulación.
* Verificación de tipos de datos: Realizamos una verificación rápida de los tipos de datos en cada columna.
* Eliminación de columnas irrelevantes: Eliminamos las columnas que no aportan al análisis de los datos, son redundantes o tienen valores nulos.
* Conversión de datos: Convertimos los datos a los tipos de datos apropiados para cada columna de nuestro dataframe.

Como resultado de este primer análisis, obtenemos 2 dataframes depurados. Sin embargo, observamos que podemos realizar una separación aún más refinada para obtener 3 dataframes con características únicas, unidos mediante su 'Id' de accidentes. Esto se hace con el objetivo de preparar, adaptar y optimizar los datos para su posterior análisis en Power BI. Por lo tanto, los dataframes finales son:

1. Tiempo: Contiene columnas como fecha, año, hora, mes, etc.
2. Ubicacion: Contiene columnas como altitud, longitud, tipo de calle, etc.
3. Accidente: Contiene columnas como Rol, Victima, Sexo, Edad, etc.

Con estos nuevos dataframes, se realizarán gráficos para verificar las tendencias, se llevará a cabo análisis univariado, análisis bivariado, mapas geográficos y distribución de los datos. Para resumir, se comentarán las conclusiones obtenidas en cada dataframe:

## Conclusiones:

### 1. Tiempo:

* Se observa una tendencia a la disminución de los accidentes viales en los últimos años, influenciada por las medidas de confinamiento por el Covid-19.
* Los últimos meses del año muestran un aumento en los accidentes viales debido a la mayor actividad en las calles.
* Las horas de la mañana representan la mayor cantidad de accidentes, lo que indica la necesidad de una mayor fiscalización en ese horario.
* Las horas de la madrugada y después del almuerzo tienen la menor cantidad de accidentes, debido a la escasez de tráfico y a la iluminación de las calles, respectivamente.

### 2. Ubicacion:
   
* Las avenidas presentan la mayor cantidad de accidentes fatales, siendo las más peligrosas de CABA.
* La comuna 1 tiene más accidentes fatales que todas las demás comunas debido a su densidad poblacional.
* Las regiones sur y este de CABA presentan una mayor cantidad de accidentes fatales en comparación con otras áreas, debido a su mayor población.

### 3. Accidente:

* Los conductores representan la mayor cantidad de fallecimientos, seguidos por los peatones.
* Las motocicletas, al ser vehículos livianos y sin protección, causan un alto número de muertes en los últimos 5 años.
* La cantidad de víctimas del sexo femenino es considerablemente menor que la de los hombres, lo que sugiere que las mujeres son más prudentes al conducir.
* La mayor cantidad de fallecimientos se encuentra en el rango de edad de 21 a 30 años.

## 2. POWER BI

El archivo se llama Siniestros.pbix y contiene las siguientes dos páginas:

### 2.1. Generalidades:

* Victimas Fatales: Tarjeta que muestra todos los accidentes fatales entre los años 2016 al 2021.
* Gráficos de Género: Tres tarjetas con iconos de hombre, mujer y desconocido que muestran los porcentajes de accidentes por género.
* Filtros Interactivos: Se presentan 4 filtros (Sexo, Acusado, Día de la Semana y Comuna) para un análisis más detallado y personalizado.
* Gráficos de Tendencia: Se incluyen gráficos de barras con líneas que muestran la tendencia de accidentes mes a mes y año tras año.
* Mapa Geográfico: Se muestra un mapa de ubicación de siniestros de CABA para visualizar la densidad de accidentes en diferentes áreas.
* Matrices Detalladas: Se proporciona una matriz para cada gráfico con información detallada sobre el tiempo, cantidad de muertos y KPIs correspondientes.

### 2.2. Indicadores:

Se han incluido 3 KPIs:

* KPI Motocicleta: Indica el porcentaje de aumento o disminución con respecto al año anterior en las víctimas de motocicleta. Para que el KPI cumpla su meta, debe haber una reducción del 7% con respecto al año anterior.
* KPI Peaton: Mide el % de aumento o disminución en las víctimas que son peatones. Se considera una reducción del 15% con respecto al año anterior como meta.
* KPI Homicidios: Evalúa si hubo una reducción o aumento de manera semestral. Una reducción del 10% con respecto al semestre anterior se considera un buen resultado.
Estos KPIs se presentan mediante gráficos de barras con líneas que muestran la tendencia de los datos y matrices detalladas que proporcionan información específica sobre cada período de tiempo. Además, se utiliza formato condicional para resaltar si se ha cumplido o no la meta establecida.

## 3. Conclusiones:

* Tendencias Temporales: Se observa una tendencia a la disminución de los accidentes viales en los últimos años, posiblemente influenciada por las medidas de confinamiento durante la pandemia de Covid-19. Sin embargo, aún se observan fluctuaciones estacionales, como picos en los últimos meses del año.

* Factores de Riesgo: Las avenidas representan el tipo de calle más peligroso, y las regiones sur y este de CABA tienen una mayor incidencia de accidentes fatales, posiblemente debido a la densidad poblacional y la infraestructura vial.

* Perfil de las Víctimas: Los conductores son el grupo más afectado por los accidentes fatales, seguidos por los peatones. La moto, al ser un vehículo liviano y sin protección, es responsable de una cantidad significativa de muertes en los últimos años.

* Distribución por Género y Edad: Existe una disparidad de género en las víctimas, con una cantidad considerablemente menor de mujeres afectadas. Además, la mayoría de las víctimas se encuentran en el rango de edad de 21 a 30 años, lo que sugiere una mayor vulnerabilidad en ese grupo demográfico.

* Análisis de KPIS: Los KPIs establecidos permiten monitorear el progreso hacia objetivos específicos, como la reducción de accidentes en ciertas categorías de víctimas. Si bien es cierto los KPIS no estan cumpliendo con el objetiv, a lo largo de periodo evaluada hay una tendencia de la disminuación de los accidentes, es decir, hay todavia mucho trabajo por realizar sin embargo, se puede observar que la cuidadania esta tomando conciencia de los accdientes viales.

