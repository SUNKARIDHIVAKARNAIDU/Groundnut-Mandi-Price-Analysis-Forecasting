# Groundnut Mandi Price Analysis and Forecasting – Andhra Pradesh

## 1. Project Overview

This project analyzes groundnut market prices in Andhra Pradesh using daily commodity price data from 2025.

The analysis focuses on Kurnool mandi and compares prices across selected markets. It also explores monthly price trends, price volatility, and simple machine learning approaches for price forecasting.

## 2. Project Objectives

- Analyze daily groundnut modal prices in Kurnool.
- Identify monthly price trends.
- Study monthly price volatility.
- Compare prices across Kurnool, Yemmiganur, and Cuddapah markets.
- Build and evaluate baseline and machine learning forecasting models.

## 3. Dataset

**Source:** [Daily Commodity Prices in India – Kaggle](https://www.kaggle.com/datasets/khandelwalmanas/daily-commodity-prices-india)

- Dataset period used: 2025
- Commodity: Groundnut
- State: Andhra Pradesh
- Primary market: Kurnool

The dataset contains market information, commodity details, arrival dates, and minimum, maximum, and modal prices.

**Note:** The dataset does not contain arrival quantity data. Therefore, this project focuses on price analysis and forecasting rather than arrival-to-price impact analysis.

The raw CSV file is not included in this GitHub repository because of its large size. Download the 2025 dataset from Kaggle and place it at:

`dataset/raw/2025.csv`

## 4. Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- VS Code

## 5. Project Structure

```text
Groundnut-Mandi-Price-Analysis-Forecasting/
├── dashboard/
├── dataset/
│   └── raw/
├── models/
├── notebooks/
│   └── 01_data_exploration.ipynb
├── src/
├── visualizations/
│   ├── actual_vs_predicted.png
│   ├── kurnool_price_trend.png
│   ├── model_comparison.csv
│   ├── monthly_average_price.png
│   └── monthly_price_volatility.png
├── .gitignore
└── README.md
```

## 6. Key Findings

- Kurnool recorded an average groundnut modal price of approximately ₹5,557.
- July had the highest monthly average modal price in the selected Kurnool data.
- November had the lowest monthly average modal price.
- September showed the highest monthly price volatility.
- Among the three selected markets, Kurnool had the highest average modal price.

These findings describe the selected 2025 dataset and should not be interpreted as general market-wide conclusions.

## 7. Forecasting Models

The following approaches were evaluated:

- Constant-price baseline
- Linear Regression using date
- Random Forest using calendar features
- Previous-price prediction
- Lag-based Linear Regression

The constant-price baseline achieved the lowest reported MAE and RMSE in the initial comparison. The lag-based Linear Regression was the strongest of the machine learning approaches by the reported error metrics.

The lag model uses a rolling one-step-ahead evaluation, where actual previous prices become available before the next prediction. Its results should therefore be interpreted separately from forecasts that use a fixed prediction throughout the test period.

## 8. Visualizations

The `visualizations/` folder contains:

- Kurnool daily price trend
- Monthly average price
- Monthly price volatility
- Actual versus predicted prices
- Model comparison results

## 9. Limitations and Future Improvements

- The current analysis uses only 2025 data.
- Arrival quantity is not available in the selected dataset.
- Only selected Andhra Pradesh markets are compared.
- Forecasting performance can be improved by testing additional time-series models and conducting a consistent rolling evaluation.

Future improvements may include:
- Adding more years of historical data.
- Exploring additional mandi markets.
- Testing more forecasting techniques.
- Developing an interactive dashboard.
- Incorporating arrival quantity data if a reliable source becomes available.

## 10. Author

Created as a Data Science learning project using Python and machine learning.
