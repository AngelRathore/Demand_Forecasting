# Demand Forecasting Case Study

## Overview

The objective is to forecast weekly demand for every **Supermarket–SKU** combination **8 weeks ahead** using historical sales data and promotional information.

The solution includes data preprocessing, exploratory data analysis, feature engineering, baseline forecasting models, Gradient Boosting, recursive multi-step forecasting, and walk-forward validation.

---

## Problem Statement

The demand planning team needs accurate forecasts to maintain the right inventory levels.

The forecasting model should:

- Predict demand **8 weeks ahead**
- Forecast each **Supermarket–SKU** combination
- Use only information available at the forecasting date
- Reduce stock-outs and over-production

---

## Dataset

### demand.csv

Daily historical demand from **January 2019 – September 2021**

Columns

- date
- supermarket
- sku
- demand

### promotions.csv

Weekly promotion periods for selected supermarket–SKU combinations.

Columns

- promotion_date
- supermarket
- sku

---

## Project Workflow

1. Data Cleaning
   - Missing value handling
   - Outlier treatment (IQR)
   - Weekly aggregation

2. Exploratory Data Analysis
   - Demand trends
   - Seasonality
   - Promotion impact

3. Feature Engineering
   - Lag features
   - Rolling statistics
   - Trend feature
   - Seasonal encoding (sin/cos)
   - Promotion indicator

4. Baseline Models
   - Naive Forecast
   - Seasonal Naive Forecast

5. Machine Learning Model
   - Gradient Boosting Regressor

6. Forecasting Strategy
   - Recursive 8-week forecasting
   - Walk-forward validation

7. Evaluation
   - MAE
   - RMSE
   - SMAPE

---

## Features Used

- Lag Demand (1, 2, 4, 8, 13, 26, 52 weeks)
- Rolling Mean
- Rolling Standard Deviation
- Trend
- Promotion Indicator
- Week Seasonality
- Month Seasonality
- Supermarket Encoding
- SKU Encoding

---

## Repository Structure

```
Demand-Forecasting-System/
│
├── Demand_Forecasting.ipynb
├── requirements.txt
└── README.md
```

---

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## Results

The notebook compares the proposed Gradient Boosting model against baseline forecasting methods using walk-forward validation.

The final model generates recursive 8-week demand forecasts for each supermarket–SKU combination while avoiding future data leakage.

---

## How to Run

1. Install the required packages

```bash
pip install -r requirements.txt
```

2. Open the notebook

```
Demand_Forecasting.ipynb
```

3. Upload

- demand.csv
- promotions.csv

4. Run all cells sequentially.

---