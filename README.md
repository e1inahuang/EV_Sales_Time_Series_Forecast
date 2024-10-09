# EV_Sales_Time_Series_Forecast

This repository contains the code and analysis for forecasting U.S. electric vehicle (EV) sales using various time series and multivariate forecasting techniques. The project explores a variety of predictive models to capture both short- and long-term trends in the rapidly growing EV market.

### Project Overview

The primary objective of this project is to predict future EV sales in the United States using a combination of traditional time series models and advanced machine learning techniques. We focus on several key factors influencing EV sales, including the cost of owning petrol cars, petrol prices, historical sales from leading EV companies, the number of drivers, energy prices, and availability of EV charging spots.

### Models Implemented

1. **Benchmark Univariate Models: Exponential Smoothing (ETS) and ARIMA (AutoRegressive Integrated Moving Average)**
   - Simple, Double, and Triple Exponential Smoothing models were used to capture seasonality, trend, and level components in the time series.
   - We employed ARIMA models to handle autocorrelation and non-stationarity in the time series data.

2. **Multivariate Models**
   - **Random Forest Regression**: Used to capture non-linear relationships and interactions between the various features.
   - **Principal Component Analysis (PCA)**: Dimensionality reduction technique to handle multicollinearity among predictors.
   - **Bagging & Boosting**: Ensemble techniques to improve the accuracy of regression models.

### Evaluation Metrics

We use the following metrics for backtesting and model evaluation:
- **Root Mean Squared Error (RMSE)**
- **Mean Absolute Error (MAE)**
- **Mean Absolute Percentage Error (MAPE)**

### Key Features

The model considers a variety of factors impacting EV sales:
- **Cost of Owning Petrol Cars**
- **Petrol Prices**
- **Past Sales Data of Leading EV Companies**: Tesla, Volkswagen, Ford, etc.
- **Number of Drivers in Pennsylvania**
- **Uber/Lyft Driver Trends**
- **Energy Prices**
- **Number of Charging Spots for EV Cars**

### Conclusion

In this project, we compared univariate models with multivariate models. The multivariate models outperformed ARIMA in terms of prediction accuracy and generalization ability. Additionally, they were more effective in addressing overfitting issues that ARIMA tends to face. Overall, multivariate models provide a more robust approach to forecasting EV sales compared to univariate methods.
