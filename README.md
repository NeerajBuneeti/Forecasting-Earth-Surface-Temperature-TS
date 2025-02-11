# Forecasting Earth Surface Temperature

Earth Temperature Forecast

## Project Overview

This project leverages historical temperature data spanning two centuries (1743 to 2013) to forecast Earth's surface temperature. Using advanced statistical models, we analyze long-term trends and seasonal patterns to provide accurate temperature predictions.

## Motivation

Climate change is one of the most pressing global challenges. Accurate temperature forecasts are crucial for:

- Aiding policymakers in formulating effective climate policies
- Helping industries adapt to changes
- Contributing to global mitigation efforts

## Dataset

- **Time Range**: 1743 to 2013
- **Geographic Coverage**: 159 countries
- **Key Metrics**:
  - Average Temperature
  - Temperature Uncertainty
  - Geographic Details (City, Country)

## Methodology

1. **Data Exploration and Preparation**
   - Exploratory Data Analysis (EDA)
   - Stationarity Tests (Unit Root Tests)

2. **Model Experimentation**
   - ARIMA (Autoregressive Integrated Moving Average)
     - Best Model: ARIMA(2, 0, 3)
     - AIC: 14503.18
   - SARIMA (Seasonal ARIMA)
     - Best Model: SARIMA(1, 1, 2)x(0, 0, 0, 12)
     - AIC: -2.69

3. **Model Evaluation**
   - Residual Analysis
   - Performance Metrics Comparison

## Results

| Model  | MSE    | RMSE   |
|--------|--------|--------|
| ARIMA  | 123.55 | 11.115 |
| SARIMA | 48.33  | 6.95   |

SARIMA outperformed ARIMA in both accuracy and residual error analysis, demonstrating superior performance for temperature forecasting.

## Challenges and Solutions

| Challenge | Solution |
|-----------|----------|
| Capturing subtle seasonal patterns | Used decomposition techniques |
| Selecting optimal model parameters | Conducted exhaustive grid searches |
| Validating model assumptions | Performed rigorous residual analysis |

## Future Enhancements

- Integrate external factors (e.g., greenhouse gas emissions, solar activity)
- Implement ensemble modeling techniques
- Account for long-term trends like global warming

## Installation and Usage

```bash
git clone https://github.com/NeerajBuneeti/earth-temperature-forecast.git
cd earth-temperature-forecast
pip install -r requirements.txt
python run_forecast.py
```
## 📧 Let’s Connect!
If you're excited about Machine Learning, AI, or data-driven innovation, I’d love to connect! Whether it’s brainstorming ideas, collaborating on projects, or just geeking out over cool models, feel free to reach out.

📬 Email: neerajvardhanbuneeti@gmail.com

Let’s build something amazing together! 🚀🤖
