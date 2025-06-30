# walmart-sales-predictor

# 🛒 Store Sales Forecasting using Machine Learning

This project focuses on forecasting weekly retail sales at various store locations using historical data, external economic factors, and holiday indicators. The primary goal is to build a predictive model that can accurately estimate future sales while accounting for the impact of holidays, markdowns, temperature, and other regional features.

## 📊 Project Overview

Retailers like Walmart need to forecast sales at the store and department level to make informed inventory and staffing decisions. Using machine learning models — particularly **Random Forest** — this project explores different factors that influence sales and evaluates performance using **Weighted Mean Absolute Error (WMAE)** with higher weight given to holiday weeks.

## 🧠 Techniques Used

- Data Cleaning & Feature Engineering
- Exploratory Data Analysis (EDA)
- Time-Series Feature Enrichment (e.g., Days to Christmas/Thanksgiving)
- SHAP-based Feature Importance
- Model Training and Evaluation using:
  - Random Forest Regressor
  - LightGBM
  - XGBoost
  - CatBoost
- Evaluation using **RMSE** and **WMAE**
- Visualization with Plotly and Matplotlib

## 🗂️ Dataset

The dataset includes:

- `train.csv`: Weekly sales data by store and department
- `features.csv`: External features like fuel price, CPI, markdowns, etc.
- `stores.csv`: Store type and size
- `test.csv`: Data without sales values (for prediction)

> Note: This project is based on the [Walmart Kaggle dataset](https://www.kaggle.com/competitions/walmart-recruiting-store-sales-forecasting).

## 🧪 Model Evaluation

| Model       | RMSE        | WMAE        |
|-------------|-------------|-------------|
| RandomForest| **3283.72** | **1473.17** |
| ExtraTrees  | 3780.45     | —           |
| XGBoost     | 5512.70     | —           |
| CatBoost    | 5602.15     | —           |
| LightGBM    | 6950.97     | —           |

✅ The **Random Forest model** outperformed others in terms of both RMSE and WMAE, and its predictions closely matched the actual sales across weeks.

## 🔍 Key Findings

- Holidays significantly boost sales, especially Christmas and Thanksgiving.
- Markdown campaigns are closely tied to high sales weeks.
- Lower unemployment and higher CPI mildly correlate with higher sales.
- Temperature variations show some relationship with demand, likely due to seasonal factors.
