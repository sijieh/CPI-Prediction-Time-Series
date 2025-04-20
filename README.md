# 📈 U.S. CPI Forecasting with Time Series Models (2000–2025)

This project applies a suite of time series models to forecast the **Consumer Price Index (CPI)** for All Urban Consumers in the United States using monthly data from **2000 to 2025**. Our goal was to uncover inflation trends and assess the predictive power of various univariate and multivariate models — ultimately guiding more accurate economic forecasting.

---

## 🎯 Objective

To analyze and forecast CPI trends using statistical time series techniques, identifying the best-performing model for inflation forecasting based on historical data and economic indicators.

---

## 🗂 Data Summary

- **Source:** [FRED](https://fred.stlouisfed.org/series/CPIAUCNS) (CPIAUCNS)
- **Frequency:** Monthly (Jan 2000 – Jan 2025)
- **Target Variable:** Consumer Price Index (Urban Consumers)
- **External Variable:** M2 Money Supply Growth Rate (used in multivariate models)

---

## 📊 Models Applied

### Univariate Models:
- 🔹 **Linear Regression**: Baseline trend and seasonality  
- 🔹 **ARIMA**: Captures autocorrelation and seasonal dependencies  
- 🔹 **GARCH**: Models time-varying volatility

### Multivariate Models:
- 🔹 **Reg-ARIMA**: Regression with ARIMA errors using M2 as external regressor  
- 🔹 **VAR (Vector AutoRegression)**: Captures dynamic interactions between CPI and M2

---

## 🧪 Results (RMSE Comparison)

| Model             | RMSE     |
|------------------|----------|
| Linear Regression| 26.14    |
| ARIMA            | 2.67     |
| GARCH            | 2.18     |
| Reg-ARIMA        | 3.03     |
| **VAR**          | **0.81** |

📌 **VAR** was the best-performing model, effectively capturing the joint behavior of CPI and M2 money supply changes.

---

## 📌 Key Insights

- Inflation shows strong trend and seasonal patterns, but is also influenced by macroeconomic shocks.
- ARIMA models improve over basic regression by modeling temporal dependencies.
- GARCH helps understand volatility but is not optimal for long-term CPI forecasting.
- Including external variables (M2) significantly improves predictive power — especially in the **VAR model**.
