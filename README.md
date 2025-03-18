# Proyecto 01 - Denoising Autoencoder y Variational Autoencoder

## Autores
- **Luther Williams Sandria**
- **Juan Pablo Echeverría Villaseñor**

## Asignatura
**Aprendizaje Profundo**

## Introducción
Este proyecto consiste en la extracción, preprocesamiento y entrenamiento de modelos de aprendizaje profundo para la eliminación de ruido en imágenes y la generación de nuevas imágenes a partir de una distribución latente. Se trabajó con imágenes de dos clases: latas de Coca-Cola y latas de Pepsi, aplicando **Denoising Autoencoders (DAE)** y **Variational Autoencoders (VAE)**.

## Extracción de Datos
Para obtener el conjunto de datos, se utilizaron herramientas de Python como `bing_image_downloader` para descargar 100 imágenes por cada categoría:
- **Coca-Cola**
- **Pepsi**

## Preprocesamiento de Datos
Las imágenes descargadas fueron sometidas a diversas transformaciones:
- **Redimensionamiento** a 512x512 píxeles
- **Conversión** a formato RGB
- **Normalización** de valores entre 0 y 1
- **División** en conjuntos de entrenamiento (80%), validación (10%) y prueba (10%)
- **Almacenamiento** en carpetas separadas según su categoría

## Denoising Autoencoder (DAE)

### Definición
Un **Denoising Autoencoder** es una red neuronal diseñada para eliminar el ruido en imágenes. Su arquitectura consta de:
- **Codificador (Encoder):** Reduce la dimensión de la imagen y extrae características principales.
- **Decodificador (Decoder):** Reconstruye la imagen a partir de la representación latente.

![DAE Encoder](./images/dae_encoder.png)
![DAE Decoder](./images/dae_decoder.png)

### Entrenamiento
El modelo fue entrenado utilizando imágenes con ruido artificial, con el objetivo de minimizar la diferencia entre la imagen original y la reconstruida.

### Resultados
Se compararon imágenes originales ruidosas con sus respectivas reconstrucciones para evaluar la efectividad del modelo.

## Variational Autoencoder (VAE)

### Definición
Un **Variational Autoencoder** introduce una distribución probabilística en la representación latente, permitiendo la generación de nuevas imágenes similares a las originales.

### Arquitectura
- **Codificador:** Transforma la imagen en parámetros de una distribución latente.
- **Espacio latente:** Representación probabilística de las imágenes.
- **Decodificador:** Reconstruye imágenes a partir de muestras tomadas del espacio latente.

![VAE Encoder](./images/vae_encoder.png)
![VAE Decoder](./images/vae_decoder.png)

### Resultados
Se generaron nuevas imágenes basadas en la distribución aprendida, evaluando su calidad y similitud con las imágenes originales.

## Conclusión
Este proyecto demostró la eficacia de los **Denoising Autoencoders** en la eliminación de ruido y la capacidad de los **Variational Autoencoders** para generar imágenes realistas a partir de un espacio latente aprendido. Estos modelos tienen aplicaciones en reducción de ruido, generación de imágenes sintéticas y compresión de datos en aprendizaje profundo.
