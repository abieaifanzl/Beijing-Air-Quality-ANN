# Beijing-Air-Quality-ANN
ANN-based classification of Beijing air quality into Safe and Hazardous categories using multi-site environmental monitoring data.


# Beijing Air Quality ANN

## Overview

This project applies **Artificial Neural Network (ANN)** and **Logistic Regression** to classify air quality using the Beijing Multi-Site Air Quality Dataset.

The main objective is to predict whether the air quality is **Safe** or **Hazardous** based on environmental and air pollutant measurements.

## Project Objective

The project aims to:

* Analyse air quality data collected from multiple monitoring stations in Beijing.
* Perform data cleaning and preprocessing.
* Explore relationships between environmental variables and air quality.
* Develop an Artificial Neural Network (ANN) classification model.
* Compare the ANN model with Logistic Regression.
* Evaluate model performance using accuracy, precision, recall, and F1-score.

## Dataset

**Dataset:** Beijing Multi-Site Air Quality Dataset
**Source:** UCI Machine Learning Repository

The dataset contains air quality and meteorological measurements collected from multiple monitoring stations in Beijing.

## Target Classification

The air quality target is created based on PM2.5 concentration:

* **Safe:** PM2.5 ≤ 75
* **Hazardous:** PM2.5 > 75

## Features Used

The model uses the following features:

* PM10
* SO2
* NO2
* CO
* O3
* Temperature (TEMP)
* Pressure (PRES)
* Dew Point (DEWP)
* Rain (RAIN)
* Wind Speed (WSPM)

PM2.5 is excluded from the input features to prevent target leakage.

## Methodology

The project follows these steps:

1. Load and merge data from multiple monitoring stations.
2. Handle missing values.
3. Create the Safe/Hazardous target variable.
4. Perform exploratory data analysis.
5. Split the data using a temporal split:

   * 70% Training
   * 15% Validation
   * 15% Testing
6. Standardize the input features using `StandardScaler`.
7. Train a Logistic Regression baseline model.
8. Train several ANN configurations.
9. Apply class weights to address class imbalance.
10. Evaluate and compare the models.

## ANN Model

The ANN models use:

* Dense layers
* ReLU activation
* Dropout
* L2 regularization
* Adam optimizer
* Binary cross-entropy loss
* Early stopping
* Learning-rate reduction
* Class weighting

Several ANN architectures were tested to identify the best-performing configuration.

## Evaluation

The models are evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

The ANN model is compared against Logistic Regression to determine its effectiveness for air quality classification.

## Technologies Used

* Python
* Google Colab
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* TensorFlow / Keras

## Project File

```text
Beijing_Air_Quality_ANN.ipynb
```

The notebook contains the complete data preprocessing, exploratory analysis, model development, training, and evaluation process.

## Future Improvements

Future work could include:

* Testing additional machine learning algorithms.
* Using more recent air quality data.
* Applying time-series or recurrent neural network models.
* Improving feature selection.
* Deploying the model as a real-time air quality prediction system.
* Adding air quality predictions for multiple future time periods.
