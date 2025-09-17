# PROYECTO 2 – REDES NEURONALES

**Autores:**  
- Santiago Camilo Rey Benavides  
- Tomás Figueroa Sierra  
- Santiago Vides Salcedo  
- Jesús Daniel Molina Emiliani  

**Docente:** Julio Omar Palacio Niño  
**Pontificia Universidad Javeriana – Facultad de Ingeniería – Ingeniería de Sistemas**  
**Bogotá D.C., 2023**

---

## 📌 Descripción General
Este proyecto analiza la **clasificación de la calidad del vino** empleando **redes neuronales feed-forward**, utilizando el dataset *Wine Quality* del repositorio UCI.  
Se comparan tres arquitecturas:
1. **Perceptrón**  
2. **Red Neuronal con 1 capa oculta**  
3. **Red Neuronal con 2 capas ocultas**

El objetivo es evaluar cómo la complejidad de la red afecta las métricas de clasificación (accuracy, precisión, recall, F1-score) y determinar la arquitectura más eficiente.

---

## 🎯 Objetivos

### Objetivo General
Diseñar y evaluar modelos de redes neuronales para la clasificación de la calidad del vino con el dataset UCI *Wine Quality*.

### Objetivos Específicos
1. Analizar y comprender las características químicas del dataset.  
2. Preprocesar los datos (limpieza, normalización, codificación y manejo de atípicos).  
3. Construir modelos de Perceptrón y redes neuronales con una y dos capas ocultas.  
4. Evaluar y comparar métricas de rendimiento: **accuracy, precisión, recall y F1-score**.  
5. Analizar el efecto de distintas proporciones de entrenamiento y prueba sobre el desempeño.

---

## 🧪 Dataset
- **Fuente:** [UCI Machine Learning Repository – Wine Quality](https://archive.ics.uci.edu/ml/datasets/Wine+Quality)
- **Tipo:** Vinos blancos (principal) y combinación blanco/rojo para prueba adicional (“bono”).
- **Características:** 11 variables químicas (acidez, azúcar residual, alcohol, pH, etc.) + variable objetivo **Quality** (0–10).

---

## 🔄 Preprocesamiento
- Eliminación de registros repetidos.  
- Unión de datasets (blanco + rojo) para experimento adicional.  
- Detección y eliminación de outliers con rangos intercuartílicos.  
- Normalización de características numéricas.  
- Selección de variables relevantes según regresión lineal.

---

## 🏗️ Modelado
Se implementaron tres arquitecturas en **TensorFlow/Keras**:

| Modelo                       | Capas ocultas | Activación | Épocas |
|-------------------------------|--------------|-----------|-------|
| Perceptrón                    | 0            | lineal    | 100   |
| Red Neuronal 1 capa           | 1 (sigmoid)  | softmax   | 200   |
| Red Neuronal 2 capas          | 2 (sigmoid)  | softmax   | 200   |

- **División de datos:** 70% entrenamiento / 30% prueba.

---

## 📊 Resultados Principales

| Modelo                     | Accuracy | Precisión | Recall | F1-Score |
|-----------------------------|---------:|---------:|------:|--------:|
| Perceptrón                 | 0.52     | 0.48     | 0.52  | 0.48    |
| Red Neuronal 1 capa        | **0.54** | **0.51** | **0.55** | **0.52** |
| Red Neuronal 2 capas       | 0.52     | 0.49     | 0.52  | 0.45    |
| 2 capas (vino blanco + rojo)| **0.59** | 0.56     | 0.59  | 0.57    |

✅ **Conclusión:**  
La red con **una sola capa oculta** mostró un equilibrio ligeramente mejor entre precisión y recall.  
Al combinar vinos blancos y rojos se logró la mejor accuracy (0.59) gracias a un mayor volumen de datos.

---

## 🧠 Conclusiones
1. **Exploración exhaustiva del dataset** permitió seleccionar atributos clave para la clasificación.  
2. El **preprocesamiento de datos** (limpieza y normalización) fue crítico para obtener resultados estables.  
3. No se observaron diferencias drásticas entre arquitecturas; **aumentar la complejidad no garantizó mejoras**.  
4. La red de **una capa oculta** es suficiente para este problema con los datos actuales.  
5. Mayor cantidad y diversidad de datos podría mejorar significativamente el rendimiento.

---

## 📎 Enlace al Notebook
[Google Colab – Código del Proyecto](https://colab.research.google.com/drive/1Kn6tFDdMZ_bD19kTtLdsZ6xLriITkjSE?usp=sharing)

---

## 🛠️ Tecnologías
- **Lenguaje:** Python  
- **Librerías principales:** TensorFlow, Keras, Scikit-learn, Pandas, NumPy, Matplotlib, Seaborn

---

**Palabras clave:** Redes Neuronales, Clasificación, Wine Quality, TensorFlow, Machine Learning

