# EV_Sales_Time_Series_Forecast

This repository contains the code and analysis for forecasting U.S. electric vehicle (EV) sales using various time series and multivariate forecasting techniques. The project explores a variety of predictive models to capture both short- and long-term trends in the rapidly growing EV market.

## Project Overview

The primary objective of this project is to predict future EV sales in the United States using a combination of traditional time series models and advanced machine learning techniques. We focus on several key factors influencing EV sales, including the cost of owning petrol cars, petrol prices, historical sales from leading EV companies, the number of drivers, energy prices, and availability of EV charging spots.

## Models Implemented

1. **Benchmark Univariate Models: Exponential Smoothing (ETS) and ARIMA (AutoRegressive Integrated Moving Average)**
   - Simple, Double, and Triple Exponential Smoothing models were used to capture seasonality, trend, and level components in the time series.
   - We employed ARIMA models to handle autocorrelation and non-stationarity in the time series data.

2. **Multivariate Models**
   - **Random Forest Regression**: Used to capture non-linear relationships and interactions between the various features.
   - **Principal Component Analysis (PCA)**: Dimensionality reduction technique to handle multicollinearity among predictors.
   - **Bagging & Boosting**: Ensemble techniques to improve the accuracy of regression models.

## Evaluation Metrics

We use the following metrics for backtesting and model evaluation:
- **Root Mean Squared Error (RMSE)**
- **R^2**
- **Mean Absolute Percentage Error (MAPE)**

## Key Features

The model considers a variety of factors impacting EV sales:
- **Cost of Owning Petrol Cars**
- **Petrol Prices**
- **Past Sales Data of Leading EV Companies**: Tesla, Volkswagen, Ford, etc.
- **Number of Drivers**
- **Uber/Lyft Driver Trends**
- **Energy Prices**
- **Number of Charging Spots for EV Cars**

## Conclusion

### Performance Summary

#### ARIMA and ETS Models:
- **ARIMA**:
  - **RMSE:** `9.19` *(Lowest)*
  - **MAE:** `6.82`
  - **MAPE:** `7.44%` *(Lowest)*

- **ETS Models (double add, triple add, single, double mul, triple mul):**
  - RMSE, MAE, and MAPE are all worse compared to ARIMA.

#### XGBoost Model:
- **Training Set:**
  - **RMSE:** `14.72` *(Reasonable fit)*
  - **R²:** `1.00` *(Perfect fit, possibly indicating overfitting)*
- **Test Set:**
  - **RMSE:** `1578.40` *(Extremely high, poor fit)*
  - **R²:** `0.10` *(Minimal explanatory power)*
  - **MAPE:** `25.60%` *(Poor accuracy)*

#### Random Forest Model:
- **Training Set:**
  - **RMSE:** `131.55`
  - **R²:** `0.97` *(Good fit)*
- **Test Set:**
  - **RMSE:** `1733.73` *(Extremely high, poor fit)*
  - **R²:** `-0.08` *(Negative value indicates poor model performance)*
  - **MAPE:** `29.81%` *(Worst accuracy among all models)*

### Best Predictive Model
- **ARIMA** is the best-performing model based on evaluation metrics. It achieved the lowest `RMSE`, `MAE`, and `MAPE`, demonstrating the best predictive accuracy on the test set.
- **XGBoost** and **Random Forest** models exhibit severe overfitting to the training data, resulting in poor generalization and unacceptable performance on the test set. Their high `RMSE` and `MAPE` values render them unsuitable for forecasting in this case.

### Recommendation
- **Use ARIMA** for predictions. It outperforms other models in both accuracy and generalization. While the results are promising, further refinements to the ARIMA model could potentially enhance its predictive performance.

