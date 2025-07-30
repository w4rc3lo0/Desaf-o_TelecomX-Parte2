# Desaf-o_TelecomX-Parte2
La nueva misión QUE NOS IMPARTE ALURA LATAM es desarrollar modelos predictivos capaces de prever qué clientes tienen mayor probabilidad de cancelar sus servicios.
📌 Resumen del Proyecto
Este proyecto analiza los patrones de fuga de clientes (churn) en una empresa de telecomunicaciones (TelecomX) en Latinoamérica. Incluye:
- Preprocesamiento de datos (limpieza, normalización y feature engineering)
- Análisis exploratorio (EDA) con visualizaciones clave
- Modelado predictivo con Machine Learning
- Evaluación de modelos y métricas de desempeño
- Informe final con conclusiones y recomendaciones

📂 Estructura del Proyecto
1️⃣ Datos Originales
TelecomX_Data.json:

Datos crudos en formato JSON con información de clientes.

Columnas principales:

customerID, Churn (target)

Datos anidados: customer, phone, internet, account

2️⃣ Preprocesamiento (Normalización y Limpieza)
🔹 Extracción y aplanado de datos:

Se normalizaron diccionarios anidados con pd.json_normalize().

Columnas resultantes: gender, SeniorCitizen, tenure, Contract, PaymentMethod, etc.

🔹 Limpieza:

Conversión a minúsculas (str.lower()).

Manejo de valores nulos en Churn (3.1% sin etiqueta).

Codificación de variables categóricas (One-Hot Encoding).

3️⃣ Análisis Exploratorio (EDA)
📊 Distribución de Churn:

71.2% clientes retenidos (No).

25.7% abandonaron (Yes).

📈 Hallazgos clave:

Clientes con contratos mensuales tienen mayor tasa de fuga.

Fibra óptica presenta más abandonos que DSL.

Facturación electrónica correlaciona con mayor churn.

(Ver notebook para gráficos de barras, heatmaps y análisis detallado)

4️⃣ Modelado Predictivo (Machine Learning)
🔹 Modelos Implementados
Regresión Logística (baseline)

Random Forest

Gradient Boosting (XGBoost)

🔹 Métricas de Evaluación
Modelo	Accuracy	Precision	Recall	F1-Score	AUC-ROC
Regresión Logística	0.78	0.65	0.52	0.58	0.72
Random Forest	0.82	0.73	0.61	0.66	0.81
XGBoost	0.84	0.76	0.65	0.70	0.85
🔹 Variables más Importantes (Según XGBoost)
tenure (antigüedad del cliente)

MonthlyCharges (cargos mensuales)

Contract_Month-to-month (contratos cortos)

InternetService_Fiber optic

5️⃣ Informe Final y Recomendaciones
📌 Conclusiones
Factores críticos de fuga:

Contratos mensuales (vs. anuales/bianuales).

Precios altos en fibra óptica sin beneficios percibidos.

Falta de soporte técnico efectivo.

🚀 Recomendaciones
Incentivar contratos a largo plazo con descuentos.

Paquetes personalizados para usuarios de fibra óptica.

Mejorar soporte técnico (asistencia 24/7).


Archivos en el Repositorio
TelecomX_LATAM.ipynb: Notebook completo (Colab).

TelecomX_Data.json: Dataset original.

README.md: Este resumen.

