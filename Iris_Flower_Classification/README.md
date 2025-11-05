# Iris Flower Classification

This project implements a machine learning model to classify Iris flowers into three species based on flower measurements.

## Project Overview

The goal is to predict the species of an Iris flower using four numerical features:

* Sepal Length (cm)
* Sepal Width (cm)
* Petal Length (cm)
* Petal Width (cm)

The dataset contains three Iris species:

* *Iris-setosa*
* *Iris-versicolor*
* *Iris-virginica*

## Model Used

**Random Forest Classifier**

Random Forest was selected due to its:

* High performance on small and structured datasets
* Robustness against overfitting
* No need for feature normalization

## Dataset

The dataset contains 150 samples, 50 per species.

| Column        | Description        |
| ------------- | ------------------ |
| Id            | Sample index       |
| SepalLengthCm | Sepal length in cm |
| SepalWidthCm  | Sepal width in cm  |
| PetalLengthCm | Petal length in cm |
| PetalWidthCm  | Petal width in cm  |
| Species       | Flower species     |

The `Id` column was dropped as it provides no predictive meaning.

## Steps Performed

1. Loaded dataset from CSV
2. Dropped `Id` column
3. Separated features (X) and target (y)
4. Split data into training and testing
5. Trained Random Forest model
6. Evaluated model using accuracy and classification report
7. Visualized results:

   * Confusion Matrix
   * Pairplot

## Model Performance

* **Accuracy: 100%**

### Classification Report

All species achieved precision, recall, and F1-score of 1.00.

This is expected because the Iris dataset is clean, well-separated, and small.

## Visualizations

### Confusion Matrix

Displays the correct prediction count for each species.

### Pairplot

Shows the distribution of features colored by species.
Clear separation is visible, especially in petal measurements.

## Additional Analysis

* Histogram plots for feature distributions
* Boxplots to check for outliers

The dataset shows minimal outliers and well-defined feature distributions.
Normalization was not necessary because Random Forest is scale-independent.

## Requirements

```
pandas
numpy
scikit-learn
matplotlib
seaborn
```

## Learning Outcomes

* Understanding classification problems
* Working with structured datasets
* Train-test split methodology
* Model evaluation metrics
* Data visualization & exploration

## Future Improvements

* Try other models: SVM, Logistic Regression
* Apply hyperparameter tuning
* Deploy as a simple web app

---

### Author
Kenzy Mohammed
Machine Learning | Data Science Enthusiast
Gmail: kenzy.m.shehate@gmail.com 