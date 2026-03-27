# Problema de regresión: Estimación de Edad a partir de Imágenes Faciales

## 1. Análisis preliminar

### Por qué es un problema de regresión? 

Este problema corresponde a una tarea de regresión debido a que la variable objetivo es continua. En este caso, se busca estimar la edad de una persona a partir de una imagen facial, lo cual implica predecir un valor numérico dentro de un rango (por ejemplo, entre 0 y 100 años).

A diferencia de los problemas de clasificación, donde las salidas son discretas (clases), en este caso el modelo debe aprender una función que relacione las características visuales de la imagen con un valor continuo.

Por lo tanto, el objetivo es aproximar una función:

Edad = f(imagen)

donde la salida es un valor real.

### Características de entrada

Las variables de entrada corresponden a imágenes faciales, las cuales son representaciones matriciales de píxeles.

Cada imagen puede describirse como un tensor de dimensiones:

Alto × Ancho × Canales

Dependiendo del dataset, las características incluyen:

Dimensiones: Las imágenes pueden variar en tamaño, por lo que es necesario redimensionarlas (ej. 64×64 o 128×128).
Espacio de color: Generalmente RGB (3 canales), aunque algunas pueden estar en escala de grises.
Valores de píxeles: Enteros entre 0 y 255, que representan la intensidad de cada canal.

Además, las imágenes contienen información visual relevante como:

- Textura de la piel
- Arrugas
- Forma facial

Estas características son utilizadas por modelos CNN para aprender patrones asociados con la edad.

