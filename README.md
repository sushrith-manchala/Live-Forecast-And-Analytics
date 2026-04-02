# Forecast Accuracy & Demand Bias Analytics Framework

## Overview

This project presents a **Forecast Accuracy and Demand Bias Analytics Framework** developed using historical sales data. The primary objective is to forecast future demand while simultaneously evaluating **forecast accuracy, bias, and deviation** to support informed business decision-making.

The framework combines data preprocessing, exploratory analytics, time-series forecasting, and interactive visualization to replicate **real-world demand planning and sales forecasting workflows** commonly used in retail, supply chain, and revenue analytics.

The solution enables stakeholders to understand not only *what demand will be*, but also *how reliable the forecast is* and *where systematic bias may exist*.

---

## Business Questions Addressed

1. Which product categories and strategies generate the highest revenue?
2. Which regions consistently outperform or underperform expectations?
3. How does customer demand vary across time, segments, and regions?
4. Are there systematic forecast biases such as over-forecasting or under-forecasting?
5. How large are deviations between actual and predicted demand?
6. Can future demand be forecasted with high accuracy and consistency?

---

## Framework Components

- Data preprocessing and feature engineering  
- Exploratory demand and sales analytics  
- Time-series forecasting using machine learning  
- Forecast accuracy and deviation analysis  
- Demand bias identification  
- Interactive Tableau dashboards for business insights  

---

## Dataset Description

The dataset contains historical sales transaction data including order dates, shipping dates, product categories, customer segments, regional information, and sales values. The multi-year span allows analysis of trends, seasonality, and demand behavior.

---

## Data Preprocessing

- Imputed missing Postal Codes using city-level mode  
- Converted Order Date and Ship Date to datetime format  
- Optimized categorical variables  
- Removed redundant columns  
- Applied log transformation to sales values  
- Engineered time-based features (year, month, weekday)

---

## Exploratory Data Analysis (EDA)

EDA revealed strong demand trends, seasonal behavior, and category-level variations, validating the use of time-series forecasting techniques.

---

## Forecasting Model Development

Forecasting was implemented in `Sales_Analytics_MyView.ipynb` using a Prophet-based time-series model. The trained model was saved as:

```
prophet_model.pkl
```

---

## Loading the Trained Forecast Model

```python
from fbprophet import Prophet
import pickle

with open('prophet_model.pkl', 'rb') as model_file:
    loaded_model = pickle.load(model_file)
```

---

## Forecast Accuracy & Demand Bias Analysis

Forecasted demand was compared against actual sales to identify deviations and assess bias across time periods and regions.

---

## Tableau Storybook

Two interactive dashboards were developed:

### Dashboard 1: Regional Demand & Contribution
- Highlights top and bottom performing regions
- Shows percentage contribution to total sales

### Dashboard 2: Forecast Accuracy & Deviation
- Compares predicted vs actual demand
- Displays high deviation periods
- Model performance: R² = 0.996

---

## Tools & Technologies

- Python (Pandas, NumPy)
- Prophet
- Jupyter Notebook
- Tableau
- GitHub

---

## Limitations & Future Enhancements

- Add MAE, RMSE, MAPE metrics
- Quantify demand bias percentage
- Compare multiple forecasting models
- Integrate external drivers (promotions, macroeconomic data)

---

## Conclusion

This project delivers a complete **Forecast Accuracy & Demand Bias Analytics Framework**, demonstrating how forecasting, analytics, and visualization can be combined to support effective demand planning and business decision-making.
