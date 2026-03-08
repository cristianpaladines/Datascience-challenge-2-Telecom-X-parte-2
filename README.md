# Datascience-challenge-2-Telecom-X-parte-2

# Telecom X - parte 2
# Predicción de Cancelación de Clientes (Customer Churn) – Proyecto de Machine Learning

## Descripción del Proyecto

La cancelación de clientes (**Customer Churn**) es uno de los principales problemas para las empresas que ofrecen servicios por suscripción, como las compañías de telecomunicaciones. Cuando los clientes cancelan su servicio, la empresa pierde ingresos y debe invertir más recursos en adquirir nuevos clientes.

El objetivo de este proyecto es desarrollar un **modelo de Machine Learning capaz de predecir qué clientes tienen mayor probabilidad de cancelar el servicio**, utilizando información demográfica, de uso del servicio y datos de facturación.

Este tipo de modelo permite a las empresas **identificar clientes en riesgo y aplicar estrategias de retención de manera anticipada**.

---

# Dataset

Para este proyecto se utilizó el dataset **Telecom X Customer Churn**, que contiene información sobre clientes de una empresa de telecomunicaciones.

El dataset incluye variables como:

* Antigüedad del cliente (Tenure)
* Cargo mensual (Monthly Charges)
* Tipo de servicio de internet
* Tipo de contrato
* Método de pago
* Servicios adicionales (Streaming, soporte técnico, seguridad, etc.)

Variable objetivo:

**Churn**

* Yes → el cliente canceló el servicio
* No → el cliente continúa con el servicio

---

# Flujo del Proyecto

El proyecto sigue un flujo típico de **Machine Learning**:

1. **Exploración de datos (EDA)**

   * Análisis inicial del dataset
   * Identificación de valores faltantes
   * Comprensión de las variables

2. **Preprocesamiento de datos**

   * Codificación de variables categóricas
   * Preparación de variables predictoras
   * División en conjunto de entrenamiento y prueba

3. **Entrenamiento de modelos**

   * Regresión Logística
   * Random Forest

4. **Evaluación de modelos**

   * Accuracy
   * Precision
   * Recall
   * F1-score
   * Curva ROC
   * AUC

5. **Interpretación del modelo**

   * Importancia de variables
   * Identificación de factores que influyen en el churn

---

# Desempeño de los Modelos

Se evaluaron dos modelos de clasificación:

| Modelo              | AUC       |
| ------------------- | --------- |
| Regresión Logística | **0.843** |
| Random Forest       | **0.821** |

El modelo de **Regresión Logística obtuvo un mejor rendimiento**, alcanzando un **AUC de 0.843**, lo que indica una buena capacidad para diferenciar entre clientes que cancelan el servicio y aquellos que permanecen.

## Curva ROC del modelo

![ROC Curve](https://github.com/user-attachments/assets/6435141d-728b-4c5d-93a1-2d4adfad9dbd)

---

# Principales Factores que Influyen en el Churn

El análisis de los coeficientes del modelo permitió identificar variables que aumentan o reducen la probabilidad de cancelación.

### Factores que aumentan la probabilidad de cancelación

* Servicio de **internet por fibra óptica**
* Método de pago **Electronic Check**
* Uso de **Streaming TV**
* Uso de **Streaming Movies**
* Clientes con **múltiples líneas telefónicas**
* **Facturación electrónica (Paperless Billing)**

Estos resultados sugieren que los clientes que utilizan **más servicios digitales o paquetes más completos** pueden tener mayores expectativas respecto al servicio o ser más sensibles al precio.

---

### Factores que reducen la probabilidad de cancelación

* **Contratos de 1 o 2 años**
* Servicio de **soporte técnico**
* Servicio de **seguridad online**
* Clientes con **pareja o dependientes**
* Mayor **antigüedad del cliente (tenure)**

Uno de los hallazgos más importantes es que **los contratos de largo plazo reducen significativamente la probabilidad de churn**.

---

# Impacto para el Negocio

El modelo desarrollado puede ayudar a las empresas a:

* Identificar **clientes con alto riesgo de cancelación**
* Aplicar **estrategias de retención personalizadas**
* Promover **contratos de mayor duración**
* Ofrecer **servicios adicionales que aumenten la fidelidad del cliente**

El uso de modelos predictivos permite tomar **decisiones basadas en datos para reducir la pérdida de clientes**.

---

# Tecnologías Utilizadas

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Jupyter Notebook

---

# Estructura del Repositorio

```
Datascience-challenge-2-Telecom-X-parte-2/
│
├── 1_Challenge_telecomX_parte2.ipynb
├── README.md
└── data/
    └── datos_tratados.csv
```

---

# Posibles Mejoras Futuras

Algunas mejoras que podrían implementarse en futuras versiones del proyecto:

* Probar modelos adicionales (XGBoost, Gradient Boosting)
* Ajuste de hiperparámetros
* Ingeniería de características (Feature Engineering)
* Explicabilidad del modelo usando **SHAP**
* Creación de un **dashboard interactivo para visualizar predicciones**

---

# Autor

Crhistian Camilo Paladines

Proyecto desarrollado como parte de un proceso de aprendizaje en **Machine Learning y Ciencia de Datos**.
