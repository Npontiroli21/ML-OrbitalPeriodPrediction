# Predicción del período orbital de asteroides

Proyecto académico de Machine Learning orientado a estimar el período orbital de asteroides a partir de variables orbitales disponibles en un conjunto de datos astronómicos.

## Objetivo

Construir y evaluar un flujo reproducible de regresión que permita:

- explorar la relación entre las variables orbitales;
- preparar y transformar los datos;
- comparar un modelo base con alternativas regularizadas;
- evaluar el error de generalización y analizar los residuos.

## Alcance de mi trabajo

Diseñé e implementé la mayor parte del flujo analítico del proyecto:

- análisis exploratorio y control inicial de calidad;
- limpieza y preparación del conjunto de datos;
- selección e ingeniería de variables;
- separación entre entrenamiento y prueba;
- estandarización de variables;
- generación y comparación de transformaciones polinómicas y fraccionarias;
- entrenamiento con LassoCV y validación cruzada;
- evaluación mediante error cuadrático medio y análisis gráfico de residuos;
- documentación de resultados y limitaciones.

## Metodología

1. **Exploración:** revisión de distribuciones, valores faltantes y relaciones entre variables.
2. **Preprocesamiento:** preparación de datos y separación del conjunto de prueba.
3. **Ingeniería de variables:** evaluación de transformaciones para capturar relaciones no lineales.
4. **Modelado:** regresión regularizada con LassoCV y validación cruzada de cinco particiones.
5. **Evaluación:** comparación mediante MSE y revisión de residuos para detectar patrones de error.

## Tecnologías

- Python
- Pandas y NumPy
- scikit-learn
- Matplotlib y Seaborn
- Jupyter / Google Colab
- Git LFS para el conjunto de datos

## Datos

El archivo utilizado en el proyecto se encuentra versionado con Git LFS y proviene del conjunto [Asteroid Features for Hazardous Prediction](https://www.kaggle.com/datasets/brsdincer/asteroid-classification-for-hazardous-prediction), construido a partir de información astronómica de NASA/JPL.

Como referencia primaria de estas variables puede consultarse la [Small-Body Database de JPL](https://ssd.jpl.nasa.gov/tools/sbdb_query.html).

## Estructura del repositorio

- **Notebook principal:** exploración, preparación, modelado y evaluación.
- **data/Asteroid_Updated.csv:** conjunto de datos administrado con Git LFS.
- **README.md:** contexto, decisiones y alcance del proyecto.

## Cómo revisar el proyecto

1. Clonar el repositorio con Git LFS habilitado.
2. Instalar las dependencias indicadas en requirements.txt.
3. Abrir el notebook en Jupyter o Google Colab.
4. Configurar la lectura del dataset desde data/Asteroid_Updated.csv antes de ejecutar todas las celdas.

## Limitaciones

- Se trata de un proyecto académico y no de un modelo desplegado en producción.
- Los resultados dependen de la calidad y cobertura del conjunto de datos.
- El notebook original fue desarrollado en Colab; la normalización completa de rutas y ejecución de punta a punta forma parte de la siguiente mejora del repositorio.
- No se publica una métrica final en este README hasta completar una nueva ejecución reproducible del flujo completo.

## Próxima iteración

- Convertir todas las rutas a referencias relativas.
- Separar preparación, entrenamiento y evaluación en módulos reutilizables.
- Incorporar un pipeline reproducible y pruebas sobre las transformaciones.
- Registrar métricas y parámetros de cada experimento.
