# Auto MPG - Análisis de Regresión Lineal

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-black?logo=pandas)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine_Learning-orange?logo=scikitlearn)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Dataset](https://img.shields.io/badge/Dataset-Auto_MPG-green)

Este proyecto usa **Python** para realizar un análisis de regresión lineal simple y múltiple en el conjunto de datos **Auto MPG** de **UC Irvine Machine Learning Repository**. 

El objetivo principal es predecir el consumo de combustible de los vehículos en millas por galón (MPG) y comparar la performance de los modelos.


## Tools & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook


## Descripción del Dataset

El conjunto de datos Auto MPG fue proporcionado por la biblioteca CMU StatLib y es ampliamente utilizado con fines didácticos. Los datos contienen información sobre vehículos y sus características, registrando valores como cilindrada, potencia y peso, entre otros.

**Link al dataset:** [Auto MPG - UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/dataset/9/auto+mpg) 


## Variables

| Variable        | Tipo              | Descripción                                         |
|-----------------|-------------------|-----------------------------------------------------|
| **mpg**         | Numérico continuo | Consumo de combustible (target variable)            |
| **cylinders**   | Numérico entero   | Número de cilindros del motor                       |
| **displacement**| Numérico continuo | Cilindrada total del motor                          |
| **horsepower**  | Numérico continuo | Potencia del motor                                  |
| **weight**      | Numérico continuo | Peso total del vehículo en libras                   |
| **acceleration**| Numérico continuo | Aceleración del vehículo                            |
| **model_year**  | Numérico entero   | Año del modelo del vehículo                         |
| **origin**      | Numérico entero   | Origen del vehículo (código numérico)               |
| **car_name**    | Categórica        | Nombre del vehículo (ID no utilizado en el modelo)  |


## Objetivo del Proyecto

El proyecto busca entrenar y evaluar modelos de regresión lineal para predecir la variable **mpg** (consumo de combustible). Se implementan modelos de:

- **Regresión Lineal Simple**: Usando una única variable predictora para explicar mpg.
- **Regresión Lineal Múltiple**: Utilizando múltiples features para predecir mpg, mejorando la precisión del modelo.

Comparamos la performance de los modelos usando el **Mean Squared Error (MSE)** y el **coeficiente de determinación (R²)**.


## Project Workflow

1. **Data Loading**
   - Importación del dataset Auto MPG.

2. **Data Cleaning**
   - Conversión de la variable `horsepower` a tipo numérico.
   - Eliminación de registros con valores faltantes.
        - Se decide prescindir de estos registros dado que son sólo 6 filas.  

3. **Exploratory Data Analysis (EDA)**
   - Estadísticas descriptivas.
   - Análisis de distribución de variables.
   - Identificación y tratamiento de outliers usando **IQR clipping**.
        - Las variables `horsepower` y `acceleration` mostraron un pequeño número de valores atípicos. En lugar de eliminar observaciones, se aplicó un **recorte (clipping)** para limitar los valores extremos al rango aceptable.

4. **Correlation Analysis**
   - Matriz de correlación entre variables numéricas.
   - Identificación de las features con mayor relación con `mpg`.

5. **Model Training**
   - Regresión lineal simple utilizando:
     - `weight`
     - `displacement`
     - `horsepower`
   - Regresión lineal múltiple utilizando:
     - `weight`
     - `displacement`
     - `horsepower`

6. **Model Evaluation**
   - Comparación de modelos utilizando:
     - Mean Squared Error (MSE)
     - Coefficient of Determination (R²)


### Correlation Matrix

![Correlation Matrix](images/correlation_matrix.png)

### Actual vs Predicted MPG

![Weight vs MPG](images/predicted_vs_real_values.png)


## Resultados

| Model | Features | MSE | R^2 |
|------|------|------|------|
| Simple Linear Regression | weight | 19.98 | 0.6784 |
| Simple Linear Regression | displacement | 19.90 | 0.6796 |
| Simple Linear Regression | horsepower | 21.18 | 0.6591 |
| Multiple Linear Regression | weight + displacement + horsepower | 18.54 | 0.7016 |

## Conclusiones

- El proyecto muestra que la regresión lineal múltiple mejora la precisión de la predicción en comparación con los modelos de regresión simple. 
- Se observa que características como weight, displacement y horsepower son predictores significativos del consumo de combustible.


## Author

- [Ayelen Alvarez](https://github.com/alvarezayelen11)


## Feedback

Si tenes sugerencias o comentarios sobre este proyecto, no dudes en ponerte en contacto conmigo.
