# 🔋 Electric Vehicle Range Prediction (2025)

This project predicts the range (in kilometers) of Electric Vehicles (EVs) using their technical specifications such as battery capacity, motor power, and torque. It includes data cleaning, exploratory data analysis (EDA), feature engineering, and predictive modeling using various regression algorithms.

---

## 📁 Dataset

**Source:** [Electric Vehicle Specifications Dataset 2025](https://www.kaggle.com/datasets/urvishahir/electric-vehicle-specifications-dataset-2025)

**Size:** 1100+ rows × ~20 columns  
**Target Column:** `range_km`

**Key Features Used:**
- `battery_capacity` (kWh)
- `motor_power` (kW)
- `torque` (Nm)
- `fast_charge_time` (min)
- `top_speed` (km/h)
- `seat`, `segment`, `car_body_type`

---

## 🧹 Data Cleaning

- Removed columns with more than **40% missing values**
- Filled missing values in `torque` using the **mean**
- Converted necessary columns to numeric
- Removed irrelevant or highly missing features
- Checked for and addressed outliers and data inconsistencies

---

## 📊 Exploratory Data Analysis (EDA)

- Visualized distributions of numerical features
- Correlation heatmap revealed:
  - `battery_capacity`, `motor_power`, and `torque` strongly impact `range_km`
- Outliers identified in `motor_power`, `torque`, and `fast_charge_time`
- Missing value matrix plotted using Seaborn and `missingno`

---

## 🤖 Predictive Modeling

| Model                  | R² Score | Mean Squared Error |
|------------------------|----------|--------------------|
| Linear Regression      | 0.89     | 1111.76            |
| **Random Forest**      | **0.9556** | **435.33**         |

**Best Model:** Random Forest Regressor

---

## 📈 Feature Importance

The most influential features in predicting EV range:
1. `battery_capacity`
2. `motor_power`
3. `torque`
4. `top_speed`

Bar chart included in `outputs/feature_importance.png`.

---

## 🧪 Model Evaluation

- Plotted Actual vs Predicted values
- High alignment shown on regression line
- Random Forest minimized errors and explained over **95%** of variance in the data

---
