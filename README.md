# Predicción de Diabetes - Machine Learning

## 📘 Descripción del Proyecto

Este proyecto tiene como objetivo desarrollar un modelo de clasificación capaz de predecir si un paciente tiene diabetes basándose en ciertas medidas diagnósticas. A través de un **Análisis Exploratorio de Datos (EDA)** exhaustivo y la implementación de un **Árbol de Decisión**, se busca proporcionar una herramienta de apoyo al diagnóstico médico que sea interpretable y precisa.

---

## 🧩 Contexto 

El diagnóstico temprano es la piedra angular para el tratamiento efectivo de la diabetes. Este conjunto de datos, proveniente del *Instituto Nacional de Diabetes y Enfermedades Digestivas y Renales*, permite modelar el riesgo de un paciente a partir de indicadores biológicos comunes. Debido al aumento global de casos, automatizar la identificación de pacientes de alto riesgo permite a las instituciones de salud intervenir de forma preventiva, optimizando los tiempos de atención y priorizando los casos clínicos más urgentes.

---

## 🎯 Objetivos

- Realizar un EDA completo para limpiar datos (especialmente el tratamiento de valores "0" biológicamente imposibles).

- Construir un modelo predictivo utilizando un Árbol de Decisión.

- Crear un ejecutable que pruebe el modelo

---

### Resumen de Características

| Columna | Tipo de Dato | Recuento No Nulo | Descripción |
| :--- | :--- | :--- | :--- |
| **Pregnancies** | `int64` | 768 | Número de embarazos del paciente.. |
| **Glucose** | `int64` | 768 | Concentración de glucosa en plasma a las 2 horas de un test de tolerancia oral. |
| **BloodPressure** | `int64` | 768 |Presión arterial diastólica (medida en mm Hg). |
| **SkinThickness** | `int64` | 768 | Grosor del pliegue cutáneo del tríceps (medida en mm). |
| **Insulin** | `int64` | 768 | Insulina sérica de 2 horas (medida en mu U/ml). |
| **BMI** | `float64` | 768 | Índice de masa corporal (peso en kg/(altura en m)^2). |
| **DiabetesPedigreeFunction** | `float64` | 768 | Función de pedigrí de diabetes (puntuación basada en antecedentes familiares). |
| **Agw** | `int64` | 768 | Edad del paciente. |
| **Outcome** | `int64` | 768 | Variable objetivo: Indica si el paciente tiene diabetes (1) o no (0). |

---

## 🚀 Metodología

### 1. Preprocesamiento de Datos
* **Tratamiento de nulos**: Se identificaron valores "0" en variables críticas (Insulina, BMI, Presión) y se imputaron o eliminaron según su relevancia.
* **División de** Datos: El dataset se dividió en conjuntos de entrenamiento (80%) y prueba (20%).

### 2. Entrenamiento del Modelo
* **Algoritmo:** **Árbol de Decisión** (`DecisionTreeClassifier`).

## 📚 ¿Qué es la Regresión Logística y cómo se usa en este proyecto?

Un **Árbol de Decisión** es un modelo de aprendizaje supervisado que funciona como un diagrama de flujo. El modelo toma decisiones dividiendo los datos en ramas según el valor de las características de entrada, creando una estructura de "nodos" que termina en una predicción final (hoja).

### 🧠 Concepto Básico

En cada paso, el árbol selecciona la variable que mejor separa a los pacientes con diabetes de los que no la tienen. Para medir qué tan buena es esa separación.

### 🎯 ¿Por qué se usa?

* Alta interpretabilidad: Permite visualizar las decisiones mediante reglas lógicas (si/entonces), lo que facilita explicar el diagnóstico médico a personas no técnicas.

* Captura relaciones no lineales: Es capaz de identificar patrones complejos donde el riesgo no aumenta de forma constante, sino que cambia drásticamente a partir de ciertos umbrales.

* Selección natural de variables: El modelo identifica automáticamente qué factores (como la glucosa o el BMI) tienen mayor impacto, ignorando los datos menos relevantes.

* Versatilidad de datos: No requiere que los datos sigan una distribución específica y maneja valores numéricos y categóricos sin necesidad de escalado previo.

* Identificación de interacciones: Detecta fácilmente cómo la combinación de dos factores (ej. edad avanzada y alta presión arterial) aumenta el riesgo de manera conjunta.

### ⚙️ Aplicación en este Proyecto

En este caso, el árbol analiza el historial clínico para crear reglas de decisión. Por ejemplo, el modelo puede aprender que si un paciente tiene una Glucose superior a un umbral crítico, esa es la señal más fuerte para clasificarlo como Outcome: 1. Al final, el árbol optimizado permite al médico ingresar los datos de un nuevo paciente y obtener una respuesta binaria inmediata basada en patrones históricos de miles de casos previos.

* Interpretabilidad: Es extremadamente fácil de explicar a un profesional de la salud (ej: "Si la glucosa es > 125 y la edad es > 30, el riesgo es alto").

* No linealidad: Puede capturar relaciones complejas entre variables sin necesidad de transformaciones matemáticas complicadas.

* Importancia de variables: Nos dice directamente qué factores (como la Glucosa o el BMI) son más determinantes para el diagnóstico.


## 🧠 Tecnologías Utilizadas

- **Python**  
- **Pandas**, **NumPy** – para manipulación y limpieza de datos  
- **Matplotlib**, **Seaborn** – para visualización de datos  
- **Scikit-learn** – para la creación y evaluación de modelos predictivos  
- **Jupyter Notebook** – entorno de desarrollo interactivo  

---

## 👤 Autor

**Bryan Jumbo Torres**  
📍 Mallorca, España  
💻 Proyecto académico / profesional de análisis de datos  