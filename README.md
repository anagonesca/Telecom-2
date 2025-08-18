# Telecom-2

## Descripción
`Telecom-2` es un proyecto de análisis de datos enfocado en el sector de las telecomunicaciones. Este repositorio contiene un cuaderno Jupyter (`Telecom-2.ipynb`) que realiza un análisis exploratorio, preprocesamiento de datos y modelado predictivo, relacionado con la predicción del abandono de clientes (churn) en una empresa de telecomunicaciones. El proyecto incluye visualizaciones como matrices de confusión, curvas ROC y mapas de calor de correlación para evaluar el rendimiento de modelos y explorar relaciones entre variables.

## Contenido
- **`Telecom-2.ipynb`**: Cuaderno Jupyter que contiene el código principal para el análisis de datos, preprocesamiento, modelado y visualización. Incluye:
  - Cálculo de correlaciones entre variables (por ejemplo, `Evasion` y `Meses contrato`).
  - Visualización de matrices de confusión para evaluar modelos de clasificación.
  - Generación de curvas ROC para analizar el rendimiento predictivo.
  - Diagramas de caja (box plots) para explorar distribuciones de variables.
  - Mapas de calor para visualizar correlaciones entre características.

## Requisitos
Para ejecutar el cuaderno, necesitas las siguientes bibliotecas de Python:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn plotly
```

## Instalación
1. Clona el repositorio:
   ```bash
   git clone https://github.com/anagonesca/Telecom-2.git
   ```
2. Navega al directorio del proyecto:
   ```bash
   cd Telecom-2
   ```
3. Instala las dependencias:
   ```bash
   pip install -r requirements.txt
   ```
   (Nota: Si no hay un archivo `requirements.txt`, instala las bibliotecas mencionadas anteriormente manualmente).

4. Abre el cuaderno Jupyter:
   ```bash
   jupyter notebook Telecom-2.ipynb
   ```

## Uso
1. Abre `Telecom-2.ipynb` en Jupyter Notebook, JupyterLab O Google Colab.
2. Asegúrate de tener un conjunto de datos compatible (por ejemplo, un CSV con columnas como `Evasion`, `Meses contrato`, `Total`, etc.).
3. Ejecuta las celdas del cuaderno para realizar el análisis y generar las visualizaciones.

## Visualizaciones
El proyecto utiliza una paleta de colores personalizada de [Color Hunt](https://colorhunt.co/palette/0d1164640d5fea2264f78d60) (`#0D1164`, `#640D5F`, `#EA2264`, `#F78D60`) para las visualizaciones, incluyendo:
- Mapas de calor de correlación.
- Matrices de confusión.
- Curvas ROC.
- Diagramas de caja.

## Contribuciones
¡Las contribuciones son bienvenidas! Si deseas contribuir:
1. Haz un fork del repositorio.
2. Crea una rama para tus cambios (`git checkout -b feature/nueva-funcionalidad`).
3. Realiza tus cambios y haz commit (`git commit -m 'Añadir nueva funcionalidad'`).
4. Envía un pull request.

## Contacto
Para preguntas o sugerencias, contacta a [anagonesca](https://github.com/anagonesca) en GitHub.
