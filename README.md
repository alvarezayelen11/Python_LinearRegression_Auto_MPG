# Auto MPG - Análisis de Regresión Lineal

Este proyecto usa **Python** para realizar un análisis de regresión lineal simple y múltiple en el conjunto de datos **Auto MPG** de **UC Irvine Machine Learning Repository**. 

El objetivo principal es predecir el consumo de combustible de los vehículos en millas por galón (MPG) y comparar la performance de los modelos.

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

## Conclusiones

El proyecto muestra que la regresión lineal múltiple mejora la precisión de la predicción en comparación con los modelos de regresión simple. Se observa que características como weight, displacement y horsepower son predictores significativos del consumo de combustible.
## Authors

- [@alvarezayelen11](https://github.com/alvarezayelen11)


## Feedback

If you have any comments, please write to me
