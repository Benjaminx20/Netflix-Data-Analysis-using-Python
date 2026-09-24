# 🎬 Netflix Data Cleaning & Transformation Project

Este proyecto demuestra el proceso de **limpieza, transformación e ingeniería de atributos (*Feature Engineering*)** aplicado a un conjunto de datos del catálogo de Netflix, utilizando tanto **Microsoft Excel** como **Python (Pandas)**.

---

## 📌 Objetivos del Proyecto

* **Detección e imputación de datos nulos:** Reemplazo estratégico de valores faltantes en columnas categóricas (`director`, `cast`, `country`).
* **Tratamiento de formatos y tipos de datos:** Conversión explícita de variables numéricas como `release_year` a tipo de dato entero (`integer`).
* **Ingeniería de atributos:** Extracción del género principal (`primary_genre`) a partir de cadenas separadas por comas en la columna `listed_in`.
* **Optimización de la estructura:** Eliminación de columnas no relevantes para el análisis estadístico.

---

## 🛠️ Herramientas Utilizadas

* **Python 3.x** (Pandas, Kagglehub) — Ejecutado en Google Colab
* **Microsoft Excel** (Fórmulas estructuradas, Tablas y Búsqueda/Reemplazo)
* **Kaggle API / Kagglehub** (Fuente de datos)

---

## 🔄 Proceso de Limpieza y Transformación

### 1. Manejo de Valores Faltantes
* **En Excel:** Filtros por columna y sustitución masiva con `Ctrl + B`.
* **En Python:**
  ```python
  columnas_texto = df.select_dtypes(include=['object']).columns
  df[columnas_texto] = df[columnas_texto].fillna('Sin información')
