# TelecomX – Parte 2F: Predicción de Churn

## Descripción
Este repositorio incluye el notebook **Telecom-2F.ipynb**, con un pipeline de *Machine Learning* para predecir la cancelación (**churn**) de clientes de **TelecomX**, usando el dataset tratado de la parte anterior.

## Contenido principal
- Notebook: `Telecom-2F.ipynb`
- Estrategias de selección de variables: filtrado por correlación, filtrado por VIF
- Técnicas de balanceo: SMOTE (oversampling), undersampling
- Modelos entrenados: KNN, Random Forest, Árbol de Decisión

## Datos de entrada
- Archivo: `datos_tratados.csv` (generado en la Parte 1)
- Posible columna objetivo según el código: Churn, Evasion, Evasión

## Requisitos
```bash
pip install pandas numpy scikit-learn matplotlib
```

## Cómo ejecutar
**Local:**
```bash
python -m venv .venv && source .venv/bin/activate  # (Windows: .venv\Scripts\Activate.ps1)
pip install pandas numpy scikit-learn matplotlib
```
Abre el notebook `Telecom-2F.ipynb` y ejecútalo de arriba a abajo.

**Google Colab:**
1. Sube `Telecom-2F.ipynb`.
2. Asegura que `datos_tratados.csv` esté en la raíz del entorno (o usa su URL *raw*).
3. Ejecuta las celdas en orden.

## Pipeline (resumen)
1. Carga del dataset `datos_tratados.csv`.
2. Preparación del objetivo (mapeo `Yes/No` → `1/0`).
3. Limpieza y selección de características (IDs fuera; filtrado por correlación, filtrado por VIF).
4. Partición **train/test** estratificada.
5. Preprocesamiento: imputación (mediana/moda), escalado para modelos que lo requieren y codificación one-hot.
6. Balanceo de clases en entrenamiento: SMOTE (oversampling), undersampling.
7. Entrenamiento de modelos y evaluación (accuracy, precision, recall, F1, ROC-AUC).
8. Selección del mejor modelo (“champion”) y validación en test.

## Resultados (extracto)
- from sklearn.preprocessing import OneHotEncoder,MinMaxScaler, LabelEncoder
from sklearn.metrics import confusion_matrix,ConfusionMatrixDisplay,classification_report,RocCurveDisplay
from sklearn.metrics import accuracy_score, precision_score, recall_score, f1_score
- Escalo las variables para que estén en la **misma escala**. Lo hago **después** del split (train/test) y dentro de un **Pipeline** usando `StandardScaler` o `MinMaxScaler`, según el caso. Repito el proceso para las tres versiones del dataset: **original**, **filtrado por correlación** y **filtrado por VIF**.
- * **Exactitud (accuracy)**
* **Recall**
* **F1-score**
> *Nota:* Los valores pueden variar al re-ejecutar el notebook.

## Estructura sugerida del repositorio
```
telecomx-parte2f/
├─ Telecom-2F.ipynb
├─ datos_tratados.csv
├─ outputs/               # métricas y curvas generadas (si aplica)
└─ README.md
```

## Licencia
MIT (o la que definas).
