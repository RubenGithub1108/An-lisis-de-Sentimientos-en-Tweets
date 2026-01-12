# Análisis de Sentimientos en Tweets (Sentiment140)

## 📝 Descripción del Proyecto

Este proyecto se enfoca en el **Procesamiento de Lenguaje Natural (PLN)** para realizar un análisis de sentimientos sobre un conjunto de datos de 1.6 millones de tweets extraídos de la API de Twitter. El objetivo es construir y evaluar modelos de Machine Learning capaces de clasificar los tweets como **positivos** o **negativos**.

A través de un riguroso preprocesamiento de texto y la aplicación de algoritmos de clasificación, este análisis busca no solo predecir el sentimiento, sino también comparar el rendimiento de diferentes modelos para esta tarea.

## 🎯 Objetivos

- Aplicar técnicas de limpieza y preprocesamiento a datos textuales extraídos de redes sociales.
- Generar visualizaciones como gráficos de distribución y nubes de palabras para un análisis exploratorio inicial.
- Vectorizar el texto utilizando la técnica **TF-IDF**.
- Entrenar, evaluar y comparar dos modelos de clasificación: **Regresión Logística** y **Random Forest**.
- Probar los modelos entrenados con texto nuevo para validar su capacidad de generalización.

## 🛠️ Herramientas y Librerías

* **Lenguaje:** Python 3.x
* **Análisis y Manipulación de Datos:**
    * **Pandas:** Para la carga y manipulación del dataset.
* **Procesamiento de Texto y PLN:**
    * **NLTK:** Para la eliminación de *stopwords*.
    * **re (Expresiones Regulares):** Para la limpieza de texto (URLs, números, puntuación).
    * **Scikit-learn:** Para la vectorización TF-IDF y el entrenamiento de modelos de Machine Learning.
* **Visualización de Datos:**
    * **Matplotlib & Seaborn:** Para generar gráficos de distribución y matrices de confusión.
    * **WordCloud:** Para crear nubes de palabras representativas de cada sentimiento.
* **Entorno de Desarrollo:** Google Colab / Jupyter Notebook

## 📂 Estructura del Repositorio

```
.
├── 📁 data/
│   └── training.1600000.processed.noemoticon.csv   # Dataset original de Kaggle
├── 📁 notebooks/
│   └── proyecto_pln_sentimientos.ipynb             # Notebook con el código y análisis
└── README.md                                       # Este archivo
```

## 🔬 Metodología de Análisis

1.  **Carga y Exploración de Datos:** Se cargó el dataset `Sentiment140` y se realizó una exploración inicial para entender su estructura y la distribución de las clases (positiva y negativa).

2.  **Limpieza y Preprocesamiento de Texto:**
    * Se eliminaron columnas innecesarias, manteniendo solo el texto y el sentimiento (`target`).
    * Se aplicó una función de limpieza a cada tweet para:
        * Convertir el texto a minúsculas.
        * Remover URLs, números y signos de puntuación.
        * Eliminar *stopwords* en inglés para reducir el ruido.

3.  **Análisis Exploratorio y Visualización:**
    * Se graficó la distribución balanceada de los sentimientos.
    * Se generaron **nubes de palabras** para los tweets positivos y negativos, identificando visualmente los términos más frecuentes en cada categoría.

4.  **Vectorización TF-IDF:** El texto limpio fue transformado en una representación numérica utilizando `TfidfVectorizer`. Se eligió TF-IDF porque penaliza las palabras que son comunes en todos los documentos, dando más importancia a los términos que son distintivos de un sentimiento en particular.

5.  **Entrenamiento y Evaluación de Modelos:**
    * **Modelo 1: Regresión Logística:**
        * Se entrenó un modelo de Regresión Logística como baseline por su eficiencia y buena interpretabilidad.
        * El modelo alcanzó una **precisión (accuracy) del 78%**.
    * **Modelo 2: Random Forest:**
        * Se entrenó un clasificador Random Forest para explorar un modelo basado en ensambles.
        * El modelo obtuvo una **precisión del 71%**, mostrando un rendimiento ligeramente inferior al de la Regresión Logística en este caso.

## 📊 Resultados y Conclusiones

| Modelo | Precisión (Accuracy) | Conclusiones Clave |
| :--- | :---: | :--- |
| **Regresión Logística** | **78%** | Modelo rápido, eficiente y con un rendimiento superior para este dataset. Es una excelente opción como punto de partida. |
| **Random Forest** | **71%** | Aunque robusto, su rendimiento fue menor. Posiblemente requiere un ajuste más fino de hiperparámetros o una mayor profundidad en los árboles. |

- La **Regresión Logística** demostró ser el modelo más efectivo y eficiente para esta tarea de clasificación de texto.
- Las nubes de palabras revelaron términos claramente asociados a cada sentimiento, como "love", "good", "happy" para los positivos, y "sad", "miss", "sorry" para los negativos.
- Ambos modelos fueron capaces de predecir correctamente el sentimiento de tweets nuevos escritos manualmente, validando su aplicación práctica.

## 🚀 Cómo Ejecutar este Proyecto

1.  Clona este repositorio:
    ```bash
    git clone [https://github.com/RubenPalma1108/An-lisis-de-Sentimientos-en-Tweets.git](https://github.com/RubenPalma1108/An-lisis-de-Sentimientos-en-Tweets.git)
    ```
2.  Navega al directorio del proyecto:
    ```bash
    cd nombre-del-repositorio
    ```
3.  Instala las dependencias necesarias:
    ```bash
    pip install pandas scikit-learn nltk matplotlib seaborn wordcloud
    ```
4.  Abre el notebook `proyecto_pln_sentimientos.ipynb` en Jupyter o Google Colab para ver el análisis completo y ejecutar el código.

## ✒️ Autor

- **Rubén Palma**

