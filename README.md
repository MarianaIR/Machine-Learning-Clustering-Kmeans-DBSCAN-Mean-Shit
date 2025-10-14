# 🧩 MACHINE LEARNING: CLUSTERING - K-MEANS, DBSCAN Y MEAN SHIFT

[![Python](https://img.shields.io/badge/Python-3670A0?style=flat&logo=python&logoColor=ffdd54)](https://www.python.org/)  
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)  
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)](https://pandas.pydata.org/)  
[![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=flat&logo=matplotlib&logoColor=white)](https://matplotlib.org/)

Este proyecto es una exploración avanzada del **Aprendizaje No Supervisado**. Se enfoca en comparar y aplicar tres algoritmos de *clustering* de gran relevancia: **K-Means, DBSCAN y Mean Shift**. El objetivo es seleccionar el método más efectivo para la **segmentación de clientes** y el análisis de la **personalidad del cliente** en un contexto de *marketing*.

---

## 🧠 Contenido del Proyecto

### 1️⃣ Análisis Exploratorio y Dataset
- **Dataset:** Se utiliza el dataset **Customer Personality Analysis** de Kaggle, el cual contiene datos de comportamiento de clientes ideales para una campaña de *marketing*.
- **Objetivo Práctico:** El análisis busca identificar la manera en que los clientes compran para modificar campañas y productos ofrecidos.

### 2️⃣ Algoritmos de Clustering Implementados
El proyecto ejecuta y compara los resultados de tres metodologías de *clustering*:

| Algoritmo | Tipo | Principio Básico | Métrica Clave de Evaluación |
|:---:|:---:|:---:|:---:|
| **K-Means** | Particional | Agrupa datos en *K* clústeres, minimizando la **distancia euclidiana** entre puntos y su centroide. | **Método del Codo** y Coeficiente de Silhouette. |
| **DBSCAN** | Basado en Densidad | Agrupa puntos que están cerca unos de otros (alta densidad), marcando como ruido (*outliers*) los puntos en regiones de baja densidad. | Coeficiente de Silhouette. |
| **Mean Shift** | Basado en Centroides | Mueve los centroides (*mean*) hacia las áreas de mayor densidad de datos de forma iterativa. | N/A (Generalmente, no requiere selección de *K*). |

### 3️⃣ Evaluación y Optimización
- **Coeficiente de Silhouette:** Se utiliza para evaluar la **calidad de la clusterización**, midiendo qué tan bien se ha agrupado cada punto. Un valor cercano a +1 indica que el punto está bien agrupado.
- **Optimización de DBSCAN:** Se demuestra la búsqueda de los hiperparámetros óptimos para DBSCAN:
    * **`eps`:** Radio de la vecindad alrededor de un punto.
    * **`min_samples`:** Número mínimo de puntos para formar una región densa.
- **Resultado de Optimización:** El análisis encuentra numéricamente los mejores valores de `eps` y `min_samples` (ej. 4.0 y 71) que maximizan el Coeficiente de Silhouette.

---

## 🛠️ Librerías Utilizadas

| Librería       | Uso principal                               |
|----------------|---------------------------------------------|
| **Scikit-learn**| Implementación de los algoritmos de *clustering* (`KMeans`, `DBSCAN`, `MeanShift`) y el Coeficiente de Silhouette|
| **Pandas**     | Carga y manipulación de los datos de clientes|
| **Matplotlib** | Visualización de los resultados de *clustering* (inferido) |

---

## 🎯 Objetivo del Proyecto
El objetivo es ir más allá de la simple aplicación de K-Means, enseñando al usuario a **seleccionar el algoritmo de *clustering* adecuado** para diferentes estructuras de datos. El proyecto enfatiza la **evaluación rigurosa** de los modelos de *clustering* mediante el Coeficiente de Silhouette y la optimización de hiperparámetros.

---

## 📈 Resultados Clave
- Se obtienen y comparan los resultados de segmentación utilizando tres técnicas de *clustering* diferentes.
- Se demuestra cómo utilizar el **Coeficiente de Silhouette** para determinar la calidad de la agrupación en un problema no supervisado.
- Se identifican los **hiperparámetros óptimos** para el algoritmo DBSCAN, lo que resulta en una segmentación más precisa y una mejor comprensión de la estructura de densidad de los datos.

