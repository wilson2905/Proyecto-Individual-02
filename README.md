<h1 align='center'>
 <b>Reporte Homicidios por  Siniestros Viales  en CABA</b>
</h1>

# <h1 align="center">**`Por Fer Abraham`**</h1>

<h1 align='center'>
 <b>Análisis de Accidentes de Tránsito en la Ciudad Autónoma de Buenos Aires</b>
</h1>

<p align='center'>
<img src="https://cdn.aarp.net/content/dam/aarp/auto/2021/05/1140-minor-fender-bender-esp.imgcache.rev.web.700.402.jpg" alt="Accidente de tránsito">
</p>

# Introducción

Este proyecto aborda el análisis de datos de accidentes de tránsito en la Ciudad Autónoma de Buenos Aires con el objetivo de proporcionar información crucial para tomar medidas que reduzcan las víctimas fatales en siniestros viales. El proyecto se desarrolla desde un rol de analista de datos, en colaboración con el `Observatorio de Movilidad y Seguridad Vial` (OMSV) de la ***Secretaría de Transporte*** del Gobierno de la Ciudad Autónoma de Buenos Aires, y la Asociacion Civil "Luchemos por la Vida" y se basa en datos recopilados entre 2016 y 2021.

# Estructura del Proyecto

### Contenido del Repositorio

- **DATOS**:
  - `homicidios.xlsx`, `poblacion_comunas.xlsx` y `comunas.xlsx`: Datasets originales.
  - `df_final_consumo.csv`: Datos listos para su consumo externo.
  - `df_siniestros_victimas.csv`y`df_siniestros.csv`: Datos limpiados y listos para unirlos en un DataSet final.


- **NOTEBOOKS**:
  - `ETL.ipynb`: Proceso de Extracción, Transformación y Carga.
  - `EDA.ipynb`: Análisis Exploratorio de Datos.
  - `PI02-DashBoard_Seg_Vial.pbix.ipynb`: Visualizaciones DashBoard en Power By.

# Proceso de Trabajo

El análisis se centra en dos bases de datos en archivos Excel: `homicidios.xlsx`, en complementos con `comunas.xlsx`
 y `poblacion_comunas.xlsx` que contienen información sobre accidentes de tránsito, informacion sobre el nombre 
 de comunas y la poblacion total de cada comuna respectivamente, en la Ciudad de Buenos Aires. Estos datos se 
 someten a un proceso de ETL para unificar y limpiar los datos. Luego, se realiza un análisis exploratorio de
  datos (EDA) para comprender las tendencias y patrones clave.

### Paso 1: ETL

- Extracción, transformación y carga de datos de `homicidios.xlsx`.Cabe destacar que los DataSets `comunas.xlsx`
y `poblacion_comuna.xlsx`no se realizan trabajos adicionales de limpieza ya que provienen estructurados 
correctamente
- Unión de datos de víctimas fatales y víctimas con lesiones en un solo DataFrame.

### Paso 2: EDA

F7F979

- Normalización de tipos de datos y limpieza.
- Visualización y análisis inicial.
- Creación de `df_final_consumo.csv` para su uso en Power BI.

### Paso 3: Visualizaciones y KPI

- se crean los KPIs a partir de las siguientes formulas y objetivos a tratar:
- Definimos a la tasa de homicidios en siniestros viales como el número de víctimas fatales en 
-    accidentes de tránsito por cada 100,000 habitantes en un área geográfica durante un período de 
-    tiempo específico. Su fórmula es:
-    (Número de homicidios en siniestros viales / Población total) * 100,000
- Objetivo: Reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses,
-    en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior.
- Definimos a la cantidad de accidentes mortales de motociclistas en siniestros viales como el 
-    número absoluto de accidentes fatales en los que estuvieron involucradas víctimas que viajaban 
-    en moto en un determinado periodo temporal. Su fórmula para medir la evolución de los 
-    accidentes mortales con víctimas en moto es: 
-    (Número de accidentes mortales con víctimas en moto en el año anterior - Número de accidentes 
-    mortales con víctimas en moto en el año actual) / (Número de accidentes mortales con víctimas 
-    en moto en el año anterior) * 100
- Objetivo Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, 
-    en CABA, respecto al año anterior.
- Definimos la cantidad de accidentes fatales con respecto a la suma entre conductores profesionales, es
-    decir, entre Transportistas de Cargas y Transportistas de Pasajeros, de la siguiente formula:
-    (((Número de víctimas en Transporte de Pasajeros)+(Número de víctimas en Transporte de Cargas)) / Cantidad
-    Total de Accidentes)
- Objetivo Reducir la Tasa de Accidentes Profesionales en un 20% sobre el total de accidentes.   


### Paso 4: Power BI

- Creación de un dashboard interactivo y un informe de análisis(en README).

********************************************************************

`A continuación se presenta un resumen del reporte explicado oralmente.`

# Hallazgos y Patrones en los Datos

Durante el análisis de los datos, se destacaron hallazgos importantes:
- Teniendo en cuenta la presentacion de dicho Informe, podemos observar que mundialmnete el pais de Argentina a lo largo del tiempo no ha tomado medidas significativas en materia de seguridad para evitar o disminuir los accidentes fatales.

- Anaizando los accidentes totales, se puede observar en gran cantidad proporcional a otros, que el primer lugar en los ultimos años lo ocupa los vehiculos que son manejados por profesionales, es decir, por Transportistas de Pasajeros y Vehiculos de carga. Este punto se puede analizxar en otro KPI exclusivo para este tema, en donde se puede deducir que, mediante el análisis de Siniestros con Choferes Profesionales en el ámbito de Transporte de Pasajeros y Transportes de Cargas, se sugiere que
      *  A pesar de tener una tendencia bajista, se debe llevar mas Capacitaciones Profesionales en el Manejo Defensivo para Choferes Profesionales, ya que por manejar vehículos de menor porte(Taxis) o mayor porte (Camiones, Colectivos) están propensos a producir daños a terceros como se puede ver en la Grafica comparativa a los Siniestros Vehiculares. Es por ello, se tomen las medidas	necesarias en el municipio correspondiente a cada comuna, para realizar dichas capacitaciones.

- Mediante las Graficas y la Geo-Localización, teniendo en cuenta los últimos 3 años se sugiere que
      * Se realicen mayor concentración de Controles Vehiculares(Autos Principalmente) en Comuna 1, Comuna 4 y Comuna 9	debido a la alta taza de Siniestros en esas Zonas.
      * Realizar Control Vehicular Periódicamente en Comuna 7 y Comuna 3, debido a la alta taza de numero de victimas

- Luego del análisis en cantidades agrupadas por mes, y observando las comunas afectadas, se sugiere que
      * Se realicen Controles exahustívos de Transito(destinado mayormente al parque moto-vehicular), en las 	Comuna 3, Comuna 7 y Comuna 15.
      * Se realicen Campañas de Publicidad alentando la toma de precauciones al conducir un moto-vehículo, orientada sobre las fechas de fin de año, en donde se ve un incremento significativo de siniestros

# Conclusiones

Mediante el análisis de Base de Datos Proporcionadas de Siniestros viales, se pudo observar gran actividad de Accidentes en Comuna 3 y Comuna 7, además de la Falta de Capacitación de los choferes profesionales en el manejo de Vehículos que Transportan Pasajeros o Cargas, y una falta de Control de Transito que pudiese prevenir accidentes en vehículos Automotor y Moto-vehículos respectivamente, dado también a la falta de Interés publico sobre la protección vehicular(por ej. uso debido del casco en caso de motos) e conducción imprudente(manejo ofensivo, exceso de velocidad). Esto conlleva a implementar Pautas de Acercamiento a la comunidad informando dichas medidas para la  Prevención de Accidentes Vehiculares 

***

# Enlaces y Links de Consulta

### Enlaces Principales:

* [Repositorio de GitHub](https://github.com/wilson2905/ProyectoIndividual02)
* [Linkedin](https://www.linkedin.com/in/jorge-fernando-abraham-451a44290/)

### Otros Enlaces

* [Enlace a Dashboard Interactivo](https://www.novypro.com/project/informe-de-siniestros-viales-en-la-ciudad-de-buenos-aires---2016-a-2021)
* [Enlace a Streamlit](https://proyectoindividual2jeremiaspombo.streamlit.app/)

***

#### El presente trabajo fue realizado por Fernando Abraham utilizando:
* Bibliotecas seaborn, pandas, numpy, matplotlib
* Power Bi y Power Service
