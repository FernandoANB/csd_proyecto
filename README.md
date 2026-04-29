# 🏥 Proyecto CSD - Predicción de Estada Hospitalaria

Este proyecto tiene como objetivo predecir los días de estada hospitalaria utilizando técnicas de Machine Learning con Apache Spark.

---

## 🛠️ Requisitos Previos

Para ejecutar este proyecto de forma local, necesitas tener instalado:

- Anaconda o Miniconda  
- Java JDK 17 (requerido por PySpark 4.1.1)  

> ⚠️ **Nota:** El archivo `environment.yml` ya incluye la instalación de `openjdk=17`.

---

## 🚀 Configuración del Entorno

Sigue estos pasos para replicar el entorno de desarrollo:

### 1. Clonar el repositorio
```bash
git clone <url-del-repo>
cd csd_proyecto
```

### 2. Crear el entorno con Conda
El archivo `environment.yml` contiene todas las dependencias necesarias (`pyspark`, `pandas`, etc.).

```bash
conda env create --file environment.yml
```

### 3. Activar el entorno
```bash
conda activate csd_proyecto
```

---

## 📊 Datos

El análisis requiere el archivo de datos oficial.

### Pasos:

1. Exporta el .zip, con esto se creara la carpeta /data (deja la car)
2. con esto se creara la carpeta /data 
3. Deja la carpeta en el mismo nivel que el codigo .ipynb


### 📁 Estructura esperada
```
.
├── Apache_Spark_ML_EGRESOS_2024.ipynb
├── environment.yml
└── data/
    └── EGRESOS_2024.csv
```

---

## 💻 Ejecución del Proyecto

### 🔹 Opción A: Jupyter (Local)

1. Iniciar Jupyter:
```bash
jupyter lab
```

2. Abrir el archivo:
```
Apache_Spark_ML_EGRESOS_2024.ipynb
```

3. Seleccionar el kernel:
```
csd_proyecto
```

4. Ejecutar las celdas en orden

---

### 🔹 Opción B: Google Colab

El notebook incluye una celda inicial (comentada) para instalar dependencias en Colab.

> ⚠️ Esta opción es alternativa; el entorno principal está pensado para ejecución local.

---

## 📝 Configuración de PySpark

Para evitar conflictos de versiones de Python (especialmente en Linux), se configura automáticamente PySpark para usar el Python del entorno activo:

```python
import os
import sys

os.environ['PYSPARK_PYTHON'] = sys.executable
os.environ['PYSPARK_DRIVER_PYTHON'] = sys.executable
```

---

## 📚 Contexto Académico

Este proyecto fue desarrollado como parte del ramo:

**Ciencia de Datos**

---