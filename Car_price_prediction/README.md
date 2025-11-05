# Car Price Prediction with Machine Learning

## Project Overview
This project predicts the **selling price of cars** based on various attributes such as brand, present price, year, transmission type, and fuel type.  
The goal is to build a regression model that can accurately estimate car prices and explore which factors influence car value the most.

---

## Objectives
- Collect and preprocess car dataset features (brand, price, mileage, transmission, etc.)
- Perform **Exploratory Data Analysis (EDA)** to understand relationships and patterns
- Handle **skewed distributions**, **categorical encoding**, and **feature scaling**
- Train regression models (Linear Regression, Random Forest)
- Evaluate performance using R², MAE, and RMSE
- Visualize results and extract meaningful business insights

---

## Tech Stack
- **Python**
- **Pandas** – Data manipulation  
- **NumPy** – Numerical operations  
- **Matplotlib / Seaborn** – Visualization  
- **Scikit-learn** – Machine learning models and preprocessing  

---

## Project Structure
car-price-prediction/
│
├── data/
│ └── car_data.csv # Dataset file
│
├── notebooks/
│ └── Car_Price_Prediction.ipynb # Jupyter Notebook
│
├── README.md # Project documentation
└── requirements.txt # Python dependencies

---

## Workflow Steps

### 1. Data Loading & Cleaning
- Loaded dataset and inspected columns
- Extracted car brand from `Car_Name`
- Created new feature: **Car_Age = Current Year - Year**
- Dropped irrelevant columns like `Car_Name`

### 2. Exploratory Data Analysis (EDA)
- Checked data distribution (histograms)
- Identified outliers (boxplots)
- Explored categorical variables (`Fuel_Type`, `Transmission`, etc.)
- Visualized correlations using a **heatmap**

### 3. Feature Engineering
- Handled skewed data using **log transformation** (`np.log1p`)
- One-hot encoded categorical variables:
  - `Fuel_Type`
  - `Selling_type`
  - `Transmission`
- Standardized numeric features (`StandardScaler`)

### 4. Model Building
- Split data into training and testing sets (70% / 30%)
- Trained:
  - **Linear Regression**
  - **Random Forest Regressor**

### 5. Model Evaluation
| Model | R² Score | MAE | RMSE |
|--------|-----------|------|-------|
| Linear Regression | 0.83 | 1.20 | 2.06 |
| Random Forest | 0.82 | 0.98 | 2.12 |

Both models performed well — **Linear Regression** achieved slightly higher R², indicating a better general fit.

---

## Key Insights
- **Present_Price** has the highest correlation with selling price.  
- **Car_Age** is inversely related — older cars sell for less.  
- **Diesel cars** generally retain higher resale value.  
- Automatic cars are slightly more expensive on average.
- Log transformation and scaling significantly improved model performance.

---

## Visualizations
- **Heatmap** – Feature correlations  
- **Boxplot** – Price distribution by fuel and transmission type  
- **Scatterplot** – Actual vs Predicted prices  
- **Histogram** – Distribution after log transformation  

---

## Future Improvements
- Add new features: horsepower, mileage, engine size, etc.
- Test advanced models: **XGBoost**, **CatBoost**
- Hyperparameter tuning for better accuracy
- Deploy using **Streamlit** or **Flask**

---

## Author
Kenzy Mohammed
Machine Learning | Data Science Enthusiast
Gmail: kenzy.m.shehate@gmail.com 

🏷️ License
This project is open-source under the MIT License.

---