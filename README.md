# Challenge Telecom X

Este repositorio contiene un notebook de Python (`.ipynb`) en el que se desarrolla un análisis de datos de cancelaciones de clientes para la empresa Telecom X, con el objetivo de determinar posibles estrategias para mejorar la retención.

## Descripción

El proyecto incluye:

- Importación y manipulación de datos desde una API
- Aplicación de conceptos de ETL (extracción, transformación y carga) de los datos
- Creación de visualizaciones para identificar patrones y tendencias
- Realizar un análisis exploratorio de los datos
- Generar un informe con datos relevantes

## 📁 Contenido

- `TelecomX_LATAM.ipynb`: Notebook con todo el análisis realizado paso a paso, incluyendo visualizaciones e informe detallado.

## Cómo usar

Para comprobar el contenido del notebook, usa Google Colab a través de [![este enlace](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/antonioacunab/challenge-telecom-x/blob/main/TelecomX_LATAM.ipynb)

Este proyecto requiere de tener disponibles las librerías Pandas, Matplotlib y Plotly en el entorno de ejecución.

## Informe de Resultados - Análisis de Cancelaciones - Telecom X

### Introducción

Telecom X es una empresa que ofrece servicios de Internet y Telefonía, y como es bien sabido, sus ingresos se ven directamente relacionados con la cantidad de clientes que tengan y los servicios que estos mismos contraten.

La empresa ha identificado que hay un índice muy alto de cancelaciones, afectando sus ganancias, y quieren identificar cuáles son aquellos factores que podrían tener más relación con que los clientes decidan dejar de contratar los servicios.

Para cumplir con los objetivos de este análisis, se utilizó Python y las bibliotecas Pandas, Matplotlib y Plotly.

### Limpieza y Tratamiento de Datos

Para iniciar con el análisis, primero se realizó la obtención y tratamiento de los datos. Los pasos a seguir fueron los siguientes:

- Se identificó el archivo con la información, la cual estaba almacenada en formato JSON.
- Se importó el archivo JSON y se convirtió en un dataframe con Pandas.
- Se hizo revisión de duplicados, valores nulos y valores vacíos
- Se suprimieron los valores vacíos, los cuales constituían un porcentaje muy pequeño de la información (3%). Adicionalmente estos hacían parte de la columna `Churn` y estimarlos podría haber afectado el análisis final.
- Se renombraron las columnas para que fuese más fácil poder presentarlas a los stakeholders y procesarlas en los siguientes pasos.

### Análisis Exploratorio de Datos

Durante el análisis realizado, se identificó que el porcentaje de cancelaciones que se ha tenido es de `26.5%`. A continuación, se la correlación que se identificó entre algunos de los datos que se estudiaron y la cantidad de cancelaciones:

### Conclusiones e Insights

A continuación, se presentan los principales hallazgos referentes a las cancelaciones de clientes

#### Datos Categóricos

- Género: No se evidenció una diferencia significativa entre las cancelaciones realizadas por hombres y mujeres, la cual constituyó entre un `26%` y un `27%`.
- Edad: Se evidenció que las personas mayores de 65 años tienen una tasa de cancelación mucho más alta `(41.7%)` en comparación con las personas menores de 65 años `(23.6%)`.
- Pareja: Se evidenció que las personas sin pareja tienden a presentar más cancelaciones `(33.0%)` en comparación con las personas que tienen pareja `(19.7%)`.
- Dependientes: Se evidenció que las personas sin dependientes tienden a presentar más cancelaciones `(31.3%)` en comparación con las personas que si tienen dependientes `(15.5%)`.
- Servicio de teléfono: No se evidenció una diferencia significativa entre las personas que contratan el servicio telefónico y las que no, estando ubicadas entre un `24.9%` y un `26.7%`
- Servicio de internet: Se evidenció una tasa superior de cancelaciones por parte de los clientes que contrataron el servicio de internet de fibra óptica `(41.9%)`, seguida por las personas que contratan DSL `(19.0%)` y por último las que no contratan servicio de internet `(7.4%)`.
- Tipo de contrato: Se evidenció que las personas con tipo de contrato mes-a-mes tienen una muy alta tasa de cancelaciones `(42.7%)`, seguida por las personas con tipo de contrato de un año `(11.3%)`, y por último las que tienen contrato de dos años `(2.8%)`

#### Datos Numéricos

- Antiguedad: Se evidenció una diferencia significativa en el porcentaje de cancelaciones según la antiguedad, presentando el primer mes de contrato una tasa de cancelaciones de `62%`, valor que va disminuyendo a medida que avanza el tiempo hasta un `1.65%` en el mes 72, con pequeñas variaciones durante este eje.
- Costos mensuales: No se evidenció una diferencia significativa entre las tasas de cancelaciones en función del costo mensual de los servicios
- Costos totales: No se evidenció una diferencia significativa entre las tasas de cancelaciones en función del costo total que ha asumido el cliente a lo largo del tiempo

### Recomendaciones adicionales

Con base en los datos recopilados anteriormente y los análisis realizados, se recomiendan los siguientes planes de acción para mejorar las tasas de retención de clientes:

- Ofrecer alternativas o paquetes preferenciales a adultos mayores
- Hacer revisiones en el servicio de internet, se debe validar la calidad del servicio de fibra óptica dado que es el que más cancelaciones presenta. También se deberían identificar posibles mejoras en el servicio de DSL.
- Revisar los tipos de contrato que se ofrecen, posiblemente suprimiendo el tipo de contrato mes-a-mes, dado que es el que genera menos retención de clientes, presentando un porcentaje de cancelaciones del 42.7%
- Ofrecer incentivos o facilidades de pago a clientes nuevos, intentando lograr que conserven el producto por más de 3 meses donde la tasa de retención ya comienza a incrementar respecto a al tasa de cancelaciones

## Autor

Este proyecto fue desarrollado por: Antonio Acuña

Encuéntrame como @antonioacunab
