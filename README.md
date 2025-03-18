# Energy Data Modeling and Analysis  

## Overview  
Energy consumption and efficiency are critical in understanding economic and environmental sustainability. This project explores energy data using machine learning models to predict energy-related metrics. Various regression models were trained and evaluated to determine their performance and feature importance.  

---  

## Workflow and Methodology  

### 1. **Data Preprocessing: Scaling with Min-Max Scaler**  
To standardize the dataset, the **MinMaxScaler** was applied, scaling all features between 0 and 1. This ensures that the models perform optimally without being affected by differences in feature magnitudes.  

### 2. **Model Selection and Training**  
The dataset was split into training and testing sets using **train_test_split**, and cross-validation was applied using **cross_validate** to ensure robust performance evaluation.  

The following regression models were trained:  
- **Linear Regression** (Baseline model)  
- **Ridge Regression** (L2 regularization to reduce overfitting)  
- **Lasso Regression** (L1 regularization for feature selection, α = 0.001)  

### 3. **Evaluation Metrics**  
To assess the model performance, the following metrics were used:  
- **Mean Absolute Error (MAE)** – Measures the average absolute error between predictions and actual values.  
- **Mean Squared Error (MSE)** – Penalizes larger errors more significantly.  
- **R² Score** – Indicates how well the model explains variance in the dataset.  

### 4. **Feature Importance Analysis**  
Feature weights were extracted from the **Linear Regression** and **Lasso Regression (α = 0.001)** models to determine:  
- The **highest and lowest weighted** features.  
- Features with **non-zero weights** in Lasso Regression, identifying the most influential variables in the dataset.  

### 5. **Model Performance Comparison**  
| Model                 | RMSE Score |  
|----------------------|------------|  
| **Linear Regression** | **0.088**  |  
| **Ridge Regression**  | **0.088**  |  
| **Lasso Regression (α=0.001)** | **0.094**  |  

- The **Linear and Ridge Regression models** performed similarly with an RMSE of **0.088**.  
- The **Lasso Regression model** had a slightly higher RMSE (**0.094**) but provided insights into feature selection.  

---

## Key Takeaways  
- **Feature Scaling** improves model performance by standardizing input values.  
- **Regularization Techniques** (L1 and L2) help in managing overfitting and selecting important features.  
- **Linear and Ridge Regression** performed equally well, while **Lasso Regression** was useful for feature selection despite a slightly higher error.  

---
