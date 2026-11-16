# ⚙️ Modelo de Mantenimiento Predictivo Industrial

## 📋 Descripción del Proyecto
Este proyecto implementa un sistema de **Machine Learning en Python** diseñado para anticipar fallas críticas en maquinaria industrial mediante el análisis de telemetría de sensores. El enfoque principal resuelve uno de los mayores desafíos en la industria: el **desbalance extremo de clases** (donde los eventos de falla son muy raros frente al funcionamiento normal), permitiendo detectar anomalías a tiempo para evitar costosas paradas de planta no programadas.

## 🛠️ Stack Tecnológico
* **Lenguaje:** Python 3.x
* **Librerías principales:** Pandas, Scikit-Learn (`RandomForestClassifier`, `StandardScaler`)
* **Entorno de desarrollo:** Google Colab

## 🚀 Fases y Metodología
1. **Simulación de Datos Operativos:** Generación de un entorno industrial con 5 variables físicas clave (`Temperatura`, `RPM`, `Torque`, `Vibración` y `Desgaste`), modelando un escenario realista de clases desbalanceadas (99% operación normal / 1% falla crítica).
2. **Preprocesamiento y Escalado:** Normalización de las variables operativas mediante `StandardScaler` para nivelar las magnitudes de los sensores.
3. **Modelado y Mitigación de Desbalance:** Entrenamiento de un `RandomForestClassifier` optimizado con un esquema de penalización de pesos (`class_weight`) para maximizar la detección de fallas (*Recall* alto) y minimizar el riesgo de pasar por alto incidentes graves.
4. **Interpretabilidad (Feature Importance):** Análisis del comportamiento del modelo para identificar qué variables tienen más peso, descubriendo que las fluctuaciones en las **RPM** y los umbrales críticos de **desgaste** actúan como los principales inductores de fallo.
5. **Evaluación de Probabilidad de Riesgo:** Extracción de probabilidades de colapso en tiempo real (`predict_proba`) para establecer umbrales de alerta temprana orientados a la toma de decisiones operativas.

## 📈 Resultados Clave
* El modelo optimizado aísla componentes en riesgo extremo con alta precisión, permitiendo identificar anomalías críticas (como desviaciones severas en desgaste y velocidad de rotación) antes de que se conviertan en detenciones de línea.

---
*Desarrollado como parte de un portafolio de Ciencia de Datos e Ingeniería Aplicada.*
