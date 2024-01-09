# Proyecto MLOps: Sistema de Recomendación de Videojuegos para Usuarios de Steam

En este proyecto abordamos un procedimiento completo de MLOps Engineer que incluye tres etapas principales:

- **Ingeniería de Datos.**
- **Análisis Exploratorio y Transformación de Datos.**
- **Modelado con técnicas de Machine Learning.**

En la primera etapa, implementaremos técnicas de Ingeniería de Datos con el fin de disponibilizar los datos para su posterior consumo y consulta. Además, crearemos consultas específicas para obtener información relevante.

En la segunda etapa, nos sumergiremos en la fase de Análisis Exploratorio de los Datos (EDA), donde limpiaremos y exploraremos los datos preparándolos adecuadamente para la recomendación. Este análisis será un paso crucial para entender las relaciones entre las variables y detectar posibles patrones y anomalías.

En la tercera y última etapa, llegaremos al corazón de este proyecto: el Modelo de Recomendación. Aquí utilizaremos un modelo de Machine Learning para desarrollar un sistema de recomendación sobre los juegos en Steam utilizando técnicas de cálculo de similitud, este sistema es "item-item" ya que ingresando un id de producto, recibiremos como respuesta una lista con 5 juegos recomendados similares al ingresado. Además, se desarrolló una API utilizando el framework FastAPI para disponibilizar los datos mediante diferentes consultas.

## Objetivo

El objetivo principal de este proyecto es desarrollar un sistema de recomendación de videojuegos que pueda proporcionar a los usuarios de Steam sugerencias personalizadas basadas en sus preferencias y comportamientos pasados.

## Tareas Realizadas

### ETL 

Realizamos un proceso de ETL (Extracción, Transformación y Carga) en el que extrajimos datos de diferentes [Datasets](https://drive.google.com/drive/folders/1cROSSeOnG7hJp1DGdjZV7GS8qWgOfj3E?usp=drive_link), los transformamos según las necesidades del proyecto y los cargamos en un destino final para su análisis y uso posterior.

La herramienta utilizada fue: Python y Pandas

### EDA

Se realizó un EDA (Análisis Exploratorio de Datos) para investigar las relaciones entre las variables del dataset y descubrir patrones. Se utilizaron técnicas de visualización y se generaron gráficas. Las herramientas utilizadas fueron: Numpy, Pandas, Matplotlib, Seaborn y Wordcloud.

## Deployment de la API

Se desarrolló una API utilizando el framework FastAPI para disponibilizar los datos. Se implementaron las siguientes consultas:

- **def PlayTimeGenre( genero : str )**: devuelve el año con mas horas jugadas para dicho género.

- **def UserForGenre( genero : str )**: Devuelve el usuario que acumula más horas jugadas para el género dado y una lista de la acumulación de horas jugadas por año.

- **def UsersRecommend( año : int )**: Devuelve el top 3 de juegos MÁS recomendados por usuarios para el año dado.

- **def UsersWorstDeveloper( año : int )**: Devuelve el top 3 de juegos MENOS recomendados por usuarios para el año dado.

- **def sentiment_analysis( año : int )**: Según el año de lanzamiento, devuelve una lista con la cantidad de registros de reseñas de usuarios que se encuentren categorizados con un análisis de sentimiento.

Las herramientas utilizadas fueron: Uvicorn, Render, FastAPI

## Modelo de Machine Learning

Realizamos un modelo de Machine Learning para generar recomendaciones de juegos, utilizando algoritmos y técnicas que analizaron patrones en los datos de usuarios y juegos, con el fin de brindar recomendaciones personalizadas y precisas basadas en los gustos y preferencias de cada usuario.

La herramienta utilizada fue: Scikit-Learn
