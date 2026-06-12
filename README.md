# Optimización de Redes Neuronales Convolucionales mediante Algoritmos Genéticos

## Descripción

Este proyecto explora el uso de **algoritmos genéticos** para optimizar automáticamente la arquitectura y los hiperparámetros de una Red Neuronal Convolucional (CNN) aplicada al dataset Fashion-MNIST.

Se comparan dos enfoques:

1. Una CNN base diseñada manualmente.
2. Una CNN optimizada mediante un algoritmo genético implementado con PyGAD.

El objetivo es evaluar la capacidad de los algoritmos evolutivos para encontrar configuraciones de red competitivas sin necesidad de realizar búsquedas manuales exhaustivas de hiperparámetros.

---

## Objetivos

- Implementar una Red Neuronal Convolucional para clasificación de imágenes.
- Aplicar algoritmos genéticos para optimizar hiperparámetros de una CNN.
- Comparar una arquitectura base contra una arquitectura optimizada.
- Analizar el impacto de distintos hiperparámetros sobre el desempeño del modelo.
- Evaluar el comportamiento de la optimización evolutiva en problemas de Deep Learning.

---

## Dataset

Se utilizó el dataset **Fashion-MNIST**, disponible directamente a través de TensorFlow/Keras.

Fashion-MNIST es un conjunto de datos diseñado como reemplazo moderno del clásico MNIST y contiene imágenes de artículos de ropa.

### Características

- 70,000 imágenes en escala de grises.
- Resolución de 28 × 28 píxeles.
- 10 clases diferentes.
- 60,000 imágenes para entrenamiento.
- 10,000 imágenes para prueba.

### Clases

- T-shirt / Top
- Trouser
- Pullover
- Dress
- Coat
- Sandal
- Shirt
- Sneaker
- Bag
- Ankle Boot

---

# Modelo Base

## Descripción

Como referencia inicial se implementó una Red Neuronal Convolucional tradicional utilizando TensorFlow/Keras.

La arquitectura incluye:

- Capas convolucionales (Conv2D).
- MaxPooling.
- Capas densas.
- Dropout.
- Funciones de activación estándar.

Este modelo sirve como punto de comparación para evaluar las mejoras obtenidas mediante optimización evolutiva.

---

# Optimización mediante Algoritmos Genéticos

## Descripción

Se utilizó la biblioteca **PyGAD** para optimizar automáticamente diversos hiperparámetros de la CNN.

Cada individuo de la población representa una configuración específica de la red neuronal.

Durante la evolución, cada solución es evaluada mediante el desempeño obtenido sobre los datos de validación.

La función de aptitud (*fitness function*) busca maximizar la capacidad de clasificación del modelo.

---

## Hiperparámetros Optimizados

Entre los parámetros optimizados se encuentran:

- Learning Rate.
- Número de filtros convolucionales.
- Tamaño de kernel.
- Tamaño de pooling.
- Strides.
- Función de activación.
- Número de neuronas densas.
- Tasa de Dropout.

---

## Mejor Configuración Encontrada

| Hiperparámetro | Valor |
|--------------|---------|
| Learning Rate | 0.02486 |
| Filtros Conv1 | 59 |
| Filtros Conv2 | 21 |
| Función de Activación | softmax |
| Kernel Convolución | 3 |
| Kernel Pooling | 5 |
| Stride Convolución | 2 |
| Stride Pooling | 3 |
| Neuronas Densas | 114 |
| Dropout | 0.4759 |

---

## Resultados

La mejor arquitectura encontrada mediante el algoritmo genético alcanzó los siguientes resultados:

| Métrica | Valor |
|----------|----------|
| Accuracy | 0.8583 |
| Precision | 0.8573 |
| Recall | 0.8583 |
| F1-Score | 0.8558 |

Estos resultados muestran que el algoritmo genético fue capaz de encontrar una configuración de hiperparámetros con un desempeño sólido para la clasificación de imágenes de Fashion-MNIST.

---

## Análisis de Resultados

Los resultados obtenidos indican que la optimización evolutiva puede utilizarse eficazmente para automatizar el proceso de diseño de arquitecturas de redes neuronales.

La similitud entre Accuracy, Precision, Recall y F1-Score sugiere que el modelo mantiene un comportamiento equilibrado entre las distintas clases del dataset y no depende excesivamente de una sola métrica de desempeño.

Además, el algoritmo genético permitió explorar múltiples configuraciones de arquitectura sin necesidad de realizar ajustes manuales extensivos.

---

## Visualizaciones

### Evolución del Fitness

La siguiente figura muestra la evolución del valor de aptitud durante el proceso evolutivo.

![Evolución del Fitness](images/fits_generacion.png)

---

### Matriz de Confusión

La matriz de confusión permite analizar el comportamiento del clasificador para cada una de las categorías del dataset.

![Matriz de Confusión](images/confucion_matriz.png)

---


## Reporte Técnico

El análisis completo de la metodología, fundamentos teóricos, experimentos y resultados puede consultarse en:

```text
reporte_resultados.pdf
```

---

## Tecnologías Utilizadas

- Python
- TensorFlow
- Keras
- PyGAD
- NumPy
- Matplotlib
- Scikit-Learn
- Seaborn

---

## Estructura del Proyecto

```text
.
├── CNN_Fmnist_base_model.ipynb
├── cnn_GA.ipynb
├── README.md
├── reporte_resultados.pdf
└── images
```

---

## Aprendizajes

Durante este proyecto se aplicaron conceptos relacionados con:

- Redes Neuronales Convolucionales (CNN).
- Deep Learning.
- Clasificación de imágenes.
- Fashion-MNIST.
- Algoritmos Genéticos.
- Optimización Evolutiva.
- Búsqueda automática de hiperparámetros.
- Evaluación de modelos de Machine Learning.
- TensorFlow y Keras.

---

## Trabajo Futuro

Algunas extensiones posibles de este proyecto incluyen:

- Optimización simultánea de más capas convolucionales.
- Comparación con métodos tradicionales de búsqueda de hiperparámetros como Grid Search o Random Search.
- Aplicación de la metodología a datasets más complejos como CIFAR-10 o CIFAR-100.
- Uso de algoritmos evolutivos multiobjetivo para equilibrar precisión y complejidad computacional.

---

## Autor

Jairo Isaac Muñoz López

Estudiante de Licenciatura en Matemáticas Aplicadas.

GitHub: https://github.com/munlopezi-lab
