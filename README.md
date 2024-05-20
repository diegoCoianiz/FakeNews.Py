# Detector de Fake News con procesamiento de lenguaje natural (NLP)

![alt text](image.png)

# Introducción

Este estudio de Google Colab corresponde al módulo 6 del bootcamp de Ciencia de Datos & IA de la academia española [CodeSpace](https://codespaceacademy.com/), y tiene como finalidad el desarrollo de un modelo predictivo de clasificación de noticias falsas propuesto en la plataforma [Kaggle](https://www.kaggle.com/datasets/saurabhshahane/fake-news-classification/data)

# Acerca del conjunto de datos

El dataset es un conjunto de datos de 72.134 artículos de noticias con 35.028 noticias reales y 37.106 noticias falsas. Para ello, los autores fusionaron cuatro conjuntos de datos de noticias populares (es decir, Kaggle, McIntire, Reuters, BuzzFeed Political) para evitar un ajuste excesivo de los clasificadores y proporcionar más datos de texto para un mejor entrenamiento de ML.

El conjunto de datos contiene cuatro columnas: Número de serie (a partir de 0); Título (sobre el título de la noticia del texto); Texto (sobre el contenido de la noticia); y Etiqueta (0 = falso y 1 = real).

# Descripción del proyecto
El proyecto consta de 3 notebooks:

 * fake-news-classification : En el se realizan los estudios, desde la construcción de modelos (etapas 1, 2 y 3), pasando por su experimentación con MLFlow (etapa 4) hasta finalmente levantar una API REST con un servidor hecho con Flask que escuche solicitudes POST y prediga, en la etapa final de producción (etapa 5), resultados de nuevos datos que lleguen desde la web.

 * NgrokMFLow_connection : es la Conexión a MLFlow UI con Ngrok, una plataforma que permite crear tuneles desde puertos locales a URL públicas para comunicación en tiempo real. Este notebook debe ejecutarse previamente a la ejecución de las etapas de experimentación en **fake-news-classification**  a fines de poder mantener una comunicación entre todos los participantes del estudio con el servidor de laboratorio levantado con MFLow UI, tanto para las pruebas experimentales individuales como para el registro de modelos y el paso a producción.

 * Streamlit web App : Una webpage para predicción de noticias generada con Streamlit, una librería de construcción rápida de páginas estáticas. El notebook levanta una página estática que transforma cadenas de texto, provenientes de un input, en data vectorizada que envía, vía POST, al servidor Flask construido en la etapa 5 del notebook **fake-news-classification** y recibe la respuesta del modelo de producción de MLFlow al final. 

# Contribuye!
¡Las contribuciones son bienvenidas! Si desea contribuir al proyecto, no dude en ponerse en contacto y pullerar sus actualizaciones!

# Licencia
Este proyecto está bajo la licencia MIT . Siéntase libre de usarlo, modificarlo y distribuirlo de acuerdo con los términos de la licencia.