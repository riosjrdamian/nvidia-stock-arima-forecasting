# NVIDIA Stock Price Forecasting with ARIMA (R)

## Overview
Time series analysis of NVIDIA's daily closing stock prices 
from 2020 to 2026 using ARIMA modeling in R. The goal was to 
identify the optimal model for forecasting future prices.

## Data
- **Source:** NVIDIA historical stock data (nvidia_stock.csv)
- **Period:** January 2020 – March 2026
- **Variable:** Daily closing price (USD)

## Methods
- Stationarity assessment using ACF and PACF plots
- First-order differencing to remove trend (d = 1)
- Manual ARIMA parameter estimation (p, d, q)
- Automated model selection using `auto.arima()` (AIC criterion)
- Model comparison across multiple ARIMA specifications
- 60-day price forecast with confidence intervals

## Key Findings
- NVIDIA stock prices showed strong non-stationarity, 
  requiring first-order differencing
- Optimal model: **ARIMA(3,1,1) with drift** 
  (AIC: 7119.3, RMSE: 2.38)
- Auto ARIMA outperformed manual ARIMA(1,1,0) 
  on both AIC and RMSE
- 60-day forecast suggests relatively stable prices 
  with widening uncertainty over time

## Tools & Libraries
R | `forecast` | `xts` | `tidyverse` | `anytime`
