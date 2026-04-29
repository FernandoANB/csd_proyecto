# Modelo Predictivo de Mortalidad al Ingreso Hospitalario para Optimización de Camas Críticas

Este proyecto aborda la dificultad de los equipos médicos para identificar de forma temprana a pacientes que, aunque parezcan estables, presentan un alto riesgo de fallecer. El modelo procesa y analiza un gran volumen de egresos hospitalarios (DEIS 2024) para predecir la probabilidad de fallecimiento (Condición de egreso). Esto permite priorizar cuidados intensivos y optimizar la asignación de camas críticas.

---

## 👥 Integrantes

- Cristóbal Salvo  
- Fernando Núñez  
- Fabian Mejías  
- Cristóbal Valenzuela  

**Asignatura:** Ciencia de Datos (NRC: 7931)

---

## 📂 Estructura del Proyecto

Para asegurar el correcto funcionamiento del proyecto, mantén la siguiente estructura:

```
.
├── Apache_Spark_ML_EGRESOS_2024.ipynb   # Notebook principal
├── environment.yml                      # Configuración de entorno Conda
└── data/                                # Carpeta para el dataset
    └── EGRESOS_2024.csv                 # Dataset (no incluido en el repositorio)
```

> ⚠️ **Importante:** El archivo CSV debe utilizar punto y coma (`;`) como separador.

---

## 🚀 Opciones de Ejecución

El proyecto puede ejecutarse de tres formas distintas según tus preferencias:

---

### 🔹 Opción 1: Google Colab (Sin instalación local)

Ideal si quieres ejecutar el proyecto rápidamente sin configurar dependencias en tu equipo.

**Pasos:**

1. Subir el archivo `.ipynb` a Google Colab  
2. Crear una carpeta `data/` en el panel lateral  
3. Subir el archivo `EGRESOS_2024.csv` dentro de esa carpeta  
4. Ubicar la celda:  
   ```
   Instalación de Apache Spark en Google Colab
   ```
5. Descomentar las líneas que contienen:
   ```
   !apt-get
   !wget
   !tar
   !pip
   ```
6. Ejecutar la celda para configurar el entorno  

---

### 🔹 Opción 2: Local sin Anaconda (Pip + Venv)

Alternativa para usar Python estándar.

**Requisitos previos:**
- Tener instalado **Java JDK 17**
- Configurar la variable de entorno `JAVA_HOME'* (Revisar como al final del documento).

**Pasos:**

1. Crear entorno virtual: (En la carpeta raiz del proyecto)
```bash
python -m venv env_spark
```

2. Activar entorno:

- **Windows**
```bash
.\env_spark\Scripts\activate
```

- **Linux / Mac**
```bash
source env_spark/bin/activate
```

3. Instalar dependencias:
```bash
Instalar dependencias: `pip install -r requirements.txt`.
```

4. Iniciar Jupyter: (O vscode con la extension de jupiter)
```bash
jupyter lab
```

---

### 🔹 Opción 2: Local con Anaconda (Recomendado)

Recomendado para mantener un entorno controlado y reproducible.

**Pasos:**

1. Abrir una terminal en la carpeta del proyecto  

2. Crear el entorno:
```bash
conda env create --file environment.yml --prune
```

3. Activar el entorno:
```bash
conda activate csd_proyecto
```

4. Iniciar Jupyter:
```bash
jupyter lab
```

---


## 🛠️ Tecnologías Utilizadas

- **Lenguaje:** Python 3.10  
- **Procesamiento de Datos:** Apache Spark / PySpark 4.1.1  
- **Machine Learning:** Spark MLlib  
  - Regresión Lineal  
  - Ridge (L2)  
  - Lasso (L1)  
  - Elastic Net  
- **Análisis de Datos:** Pandas, NumPy  

---

## 📌 Notas

- El dataset **no está incluido** en el repositorio.  
- Asegúrate de colocarlo en la carpeta `data/` antes de ejecutar el notebook.  
- El proyecto está diseñado para ser reproducible en distintos entornos.  

---

## 📚 Contexto

Este proyecto fue desarrollado como parte del curso **Ciencia de Datos**, enfocado en el uso de herramientas de procesamiento distribuido para análisis de datos reales del sistema de salud en Chile.

---

## Configurar variable HOME

1. Localizar la ruta de instalación
Primero deben saber dónde se instaló Java 17.

Windows: Generalmente es C:\Program Files\Java\jdk-17

2. Configurar la Variable
En Windows (Interfaz Gráfica)

    1. Buscar "Editar las variables de entorno del sistema" en el menú Inicio.

    2. Hacer clic en el botón Variables de entorno.

    3. En Variables del sistema, hacer clic en Nueva....

    4. Nombre de la variable: JAVA_HOME

    5. Valor de la variable: C:\Program Files\Java\jdk-17 (o la ruta donde lo instalaron).

    6. Buscar la variable Path en la misma lista, seleccionarla, hacer clic en Editar... y añadir una nueva línea: %JAVA_HOME%\bin.

3. Verificar la configuración
En una nueva terminal, deben ejecutar estos dos comandos. Ambos deben responder con éxito:

```bash
echo %JAVA_HOME% 
```
