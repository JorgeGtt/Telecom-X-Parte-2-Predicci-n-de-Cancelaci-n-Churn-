# 📊 Telecom X - Parte 2: Predicción de Churn de Clientes

## 🎯 Propósito del Análisis

Este proyecto tiene como objetivo **predecir la cancelación de clientes (churn)** en una empresa de telecomunicaciones, utilizando técnicas de análisis de datos y aprendizaje automático. A partir de variables relevantes sobre los clientes y sus comportamientos, se busca identificar patrones que permitan anticipar la deserción y así diseñar estrategias de retención efectivas.

---

## 📁 Estructura del Proyecto

Telecom_X_Parte2/
│
├── 📄 TelecomX_Parte2.ipynb # Cuaderno principal del análisis
├── 📄 datos_tratados.csv # Conjunto de datos preprocesado
├── 📊 visualizaciones/ # Carpeta con gráficos generados durante el EDA
├── 📄 README.md # Este archivo descriptivo
└── 📄 requirements.txt # Librerías necesarias para ejecutar el proyecto

---

## ⚙️ Preparación de los Datos

### ✅ Clasificación de Variables

- **Categóricas**: Género, Tipo de contrato, Método de pago, Servicio de internet, etc.
- **Numéricas**: Cargos mensuales, Cargos totales, Tiempo de permanencia (tenure), etc.

### 🧹 Limpieza y Transformación

- Eliminación de valores nulos y duplicados.
- Conversión de variables categóricas mediante **One-Hot Encoding**.
- Normalización de variables numéricas usando `StandardScaler`.

### ✂️ División del Dataset

- **80%** para entrenamiento (`X_train`, `y_train`)
- **20%** para prueba (`X_test`, `y_test`)

La división se realizó de manera estratificada para conservar la proporción de clases.

---

## 🧠 Modelado y Decisiones

- Se probaron múltiples algoritmos: **Logistic Regression, Random Forest, XGBoost**.
- Se priorizó la **precisión y el recall** debido al desequilibrio en la clase "Churn".
- Se utilizó `GridSearchCV` para optimizar hiperparámetros.
- Se justificó el uso de escalado previo y codificación para asegurar buen rendimiento de modelos sensibles a las magnitudes de los datos.

---

## 📈 Ejemplos de EDA (Exploratory Data Analysis)

A continuación algunos insights destacados:

- 📉 Clientes con contratos mensuales tienen mayor tasa de churn.
- 💳 El método de pago electrónico se asocia a una mayor deserción.
- 🧾 Los cargos mensuales altos también correlacionan con el churn.

Ejemplos de gráficos incluidos en la carpeta `visualizaciones/`:

- `churn_by_contract_type.png`
- `monthly_charges_distribution.png`
- `correlation_heatmap.png`

---

## ▶️ Instrucciones para Ejecutar el Proyecto

1. **Clona o descarga este repositorio:**

```bash
git clone https://github.com/usuario/Telecom_X_Parte2.git
cd Telecom_X_Parte2

pip install -r requirements.txt
import pandas as pd
df = pd.read_csv("datos_tratados.csv")

pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
jupyter

🤝 Contribución
Sugerencias, mejoras y análisis alternativos son bienvenidos. Puedes hacer un fork del proyecto y enviar un pull request.

