# PROYECTO DATA ANALYST

# INTRODUCCIÓN

<div align="justify">
En este trabajo se realiza un análisis de datos de los siniestros viales de la Ciudad Autónoma de Buenos Aires en el periodo 2016 a finales del 2021. Se realiza un proceso de transformación de los datos para que estos sean explorados de manera exhaustiva en el procesos de análisis exploratoratorio de estos datos.
</div>
<div align="justify">
De esta manera se encuentran hallazgos de importancia los cuales nos llevarán a conclusiones sobre este tema tan delicado como los homicidios en siniestros viales para posteriormente dar recomendaciones para disminuir las cifras de víctimas.
</div>
<div align="justify">
Estos hallazgos serán presentados en un dashboard interactivo en la plataforma Power Bi no solo para su presentación sino para que otros usuarios puedan acceder y poder ver toda la información y no solo los hallazgos.
</div>

# DESARROLLO

<div align="justify">
A continuación se realizara una descripción del desarrollo llevado a cabo de todo el proceso del trabajo, la parte de código y lo más específico se puede encontra en el archivo mencionado en cada etapa y solo se brindará un resumen de las mismas.
</div>

## ETL

<div align="justify">
En primer lugar se realizará un proceso de ETL donde se descargará la información y se transformará para dejar un dataset limpio y con la información para realizar el EDA de manera eficiente.
</div>
<div align="justify">
En este caso se utiliza como fuente principal de información el archivo <em>homiciodios.xlsx</em>, que se encuentra dentro de la carpeta Datasets, el cual se descargo del sitio de <a href="https://data.buenosaires.gob.ar/dataset/victimas-siniestros-viales">Buenos Aires Data</a>, el cual contiene la información del periodo 2016-2021 de homicidios en siniestros viales en la Ciudad Autónoma de Buenos Aires.
</div>
<div align="justify">
Este documento cuenta con información de los hechos y de las víctimas en diferentes hojas del archivo por lo que se decide unificar esta información y tratarla como un solo dataframe
</div>
<div align="justify">
Luego se procede a quedarse con información relevante para el análisis de la situación y se procede a dar formato y normalizar todo para su posterior tratamiento.
</div>
<div align="justify">
La información que se considera importante para este proyecto es:
<ul>
<li>Cantidad de victimas del siniestro.
<li>Fecha y hora en la que ocurrió.
<li>Lugar de donde ocurre el hecho.
<li>Tipo de calle donde se da el accidente.
<li>Comuna donde tuvo lugar el siniestro.
<li>Longitud y latitud del lugar.
<li>Los involucrados.
<li>La víctima del homicidio.
<li>El acusado del accidente aunque no lo fuera legalmente.
<li>El rol que tenía la víctima en el homicidio.
<li>El sexo de la víctima.
<li>La edad de la víctima
</ul>
</div> 
<div align="justify">
Con todos estos datos se genera un archivo llamado <em>data.xlsx</em> que se encuentra en la carpeta Datasets y se utilizará para el análisis exploratorio de los datos.
</div>

## EDA
<div align="justify">
En el proceso de análisis exploratorio de datos se va a hacer hincapié en la imputación de datos y en los criterios tomados para realizar las mismas, además de los criterios para llevar a cabo otros análisis. Se trabajará aqui con el archivo <em>data.xlsx</em>.
</div>
<div align="justify">
Lo primeros que se hace en esta etapa es convertir los valores <strong>SD</strong> a nulos para poder estudiar el dataframe de manera normalizada y poder ver la cantidad de datos faltantes en el dataset. Aclaramos que si bien muchas veces es más mejor por cuestiones costo-beneficio borrar filas con datos faltantes que llevar a cabo un análisis para lograr una buena imputación de datos, en este caso se hace énfasis en la imputación de datos para hacer uso de esta herramienta.
</div>
<div align="justify">
Para la imputación de los valores faltantes en general la idea es no modificar la distribución de datos de la variable en la que hay valores nulos.
</div>
<div align="justify">
En el caso que falten pocos datos y haya clases de la variable en cuestión que tengan una mayor frecuencia se le imputan los datos faltantes a esa clase, ya que esta imputación no modificará de manera significativa la ditribución de los mismos. Como por ejemplo en las variables <em>sexo</em> donde mayoritariamente son HOMBRES o en el caso de <em>víctimas</em> donde la mayoria son MOTOS.
</div>
<div align="justify">
Cuando la cantidad de datos faltantes ya es importante lo que se hace es verificar si la imputación por algún valor no modifica la distribuciónde. Los metodos que se pueden ver en el notebook son imputación por la mediana, la media, la moda y mediante un muestreo por un método de la librería Pandas de Python.
</div>
<div align="justify">
Una vez hecha la imputación de valores faltantes se verifica que las distribuciones no se modifican y se elige la opción más idonea.
</div>
<div align="justify">
En lo que respecta a los valores atípicos en este set de datos solo se han registrado en una situación en particular pero se verá esto en los hallazgos.
</div>
<div align="justify">
En el proceso de análisis, se comienza con cada variables en particular para buscar patrones y luego se continua con las ventanas de tiempo típicos como trimestre, semestre, mes y semana.
</div>
<div align="justify">
También se analizan las horas en la que suceden los siniestros para ver patrones en días laborales y no laborales.
</div>
<div align="justify">
Una vez completado el EDA se crea un nuevo dataset, <em>data_final.xlsx</em> para ser utilizado con Power Bi y poder hacer la presentación del análisis realizado en esta sección.
</div>

# HALLAZGOS

# CONCLUSIONES

# RECOMENDACIONES

# TECNOLOGÍAS