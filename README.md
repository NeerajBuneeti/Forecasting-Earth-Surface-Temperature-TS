# Forecasting Earth Surface Temperature

## Why We Did This Project

Climate change has emerged as one of the most pressing global challenges. Understanding and forecasting Earth's surface temperature is critical to mitigating its effects, such as extreme weather events, sea level rise, and shifts in agricultural productivity. Accurate predictions can:
- Aid policymakers in formulating effective climate policies.
- Help industries adapt to changes.
- Contribute to global mitigation efforts by offering valuable insights into future temperature trends.

## What This Project Is About

Our project leverages historical temperature data spanning two centuries (1743 to 2013) to forecast Earth's surface temperature. Using statistical and machine learning models, we analyzed:
- Long-term trends and seasonal patterns in the data.
- The impact of these factors on accurate forecasting.

The goal was to compare and select the best model to provide reliable temperature predictions, emphasizing the importance of accounting for seasonality and trend components.

## How We Did It

### Data Exploration and Preparation
- **Dataset Details:** Monthly temperature records from 159 countries and several cities, including metrics like:
  - Average Temperature
  - Uncertainty in Temperature
  - Geographic Details (City, Country)
- **Exploratory Data Analysis (EDA):** Identified trends, seasonality, and patterns through visualizations and statistical decomposition.
- **Stationarity Tests:** Performed unit root tests to confirm the stationarity of the dataset.

### Model Experimentation
- **ARIMA (Autoregressive Integrated Moving Average):**
  - Focused on understanding dependencies and short-term fluctuations.
  - Best Model: ARIMA(2, 0, 3) with AIC = 14503.18.
- **SARIMA (Seasonal ARIMA):**
  - Extended ARIMA to account for seasonality.
  - Best Model: SARIMA(1, 1, 2)x(0, 0, 0, 12) with AIC = -2.69.

### Model Evaluation
- **Residual Analysis:** Ensured the model captured underlying data patterns.
- **Performance Metrics:**
  - ARIMA: MSE = 123.55, RMSE = 11.115.
  - SARIMA: MSE = 48.33, RMSE = 6.95.
- SARIMA outperformed ARIMA in both accuracy and residual error analysis.

## Challenges and How We Overcame Them
- **Challenge:** Capturing subtle seasonal patterns and ensuring stationarity.
  - **Solution:** Used decomposition techniques to isolate trend, seasonal, and residual components.
- **Challenge:** Selecting the best model parameters among many combinations.
  - **Solution:** Conducted exhaustive grid searches and optimized using AIC metrics.
- **Challenge:** Ensuring the model assumptions were valid.
  - **Solution:** Validated with rigorous residual analysis and stationarity checks.

## Results
SARIMA demonstrated superior performance compared to ARIMA, making it the more reliable model for temperature forecasting. The project highlights the importance of incorporating both seasonal and trend components in time series modeling.

## Future Enhancements
- Integrate external factors such as greenhouse gas emissions, solar activity, and ocean currents.
- Implement ensemble modeling techniques combining multiple forecasting models.
- Account for long-term trends like global warming to improve forecast accuracy.

---

Thank you for exploring our project! If you have questions or suggestions, feel free to contribute to this repository or reach out.
