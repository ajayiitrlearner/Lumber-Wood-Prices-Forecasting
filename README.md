# Lumber-Wood-Prices-Forecasting
This project forecasts lumber prices using time series models. It includes exploratory data analysis, ARIMA modeling, Meta's Prophet model, and model comparison. The analysis spans January 1947 to November 2023, revealing significant price fluctuations. The Naive Drift model outperforms others, providing a six-month forecast for lumber prices. 


## Summary of Analysis: Forecasting the Prices of Lumber Wood

### **Section 1 - Exploratory Data Analysis and Time Series Decomposition**

#### Data Overview
- **Source**: U.S. Bureau of Labor Statistics, Producer Price Index (PPI) program.
- **Timeframe**: January 1947 to November 2023 (monthly data).
- **Variables**: Date, Lumber Price (923 observations).

#### Key Insights
- **Price Variations**: Influenced by supply and demand, inflation, seasonal trends, pandemic, wildfires, and government tariffs.
- **Preliminary Examination**: Steady price increase from 1947 to 2020, with significant fluctuations in the last 4 years.

#### Visualization and Statistics
- **Trend Visualization**: Line chart showing lumber prices over time.
- **Summary Statistics**: Mean, median, mode, standard deviation, and range.
- **Box-Plot**: Indicating right-skewed data with outliers.

#### Time Series Decomposition
- **Components**: Trend, seasonal, and remainder components.
- **Seasonality Check**: Lag plot and box plot revealed no clear seasonal pattern.

#### Test-Train Split
- **Training Set**: 80% of the data.
- **Testing Set**: Remaining 20%.

### **Naive Forecasting**
- **Naive Forecast**: Based on the last observed value, showing steady trend.
- **Naive with Drift**: Considered the linear trend for better predictions.

### **Section 2 - ARIMA Modeling**

#### Stationarity Checks
- **KPSS Test**: Indicated non-stationarity in the original data.
- **Log Transformation**: Achieved mean and variance stationarity.

#### Model Identification
- **ACF and PACF Plots**: Suggested AR(2) or MA(1) process.
- **Model Selection**: Compared multiple ARIMA models based on AIC and BIC values.

#### Best Model
- **Selected Model**: ARIMA(2,1,4), confirmed by both manual and automated selection methods.
- **Residuals Check**: No significant autocorrelation (p-value > 0.05).

### **Section 3 - Meta Prophet Model**

#### Model Components
- **Basic Prophet Model**: Includes trend, seasonality, and holidays.
- **Decomposition**: Analyzed the trend and seasonal components.

#### Change Point Detection
- **Initial and Adjusted Change Points**: Identified significant change points affecting trend.

#### Model Flexibility
- **Changepoint Range and Prior Scale**: Adjusted to allow more or fewer change points for better flexibility.

#### Final Prophet Model
- **Forecasting**: Extended the forecast horizon with confidence in identified change points.

### **Conclusion**
The analysis demonstrated the complexity of lumber price forecasting due to various influencing factors and significant fluctuations in recent years. The ARIMA(2,1,4) model was identified as the best fit, and the Meta Prophet model provided additional insights through change point detection and flexible trend adjustments. These models collectively offer a robust approach to predicting future lumber prices, accounting for underlying trends and potential structural changes in the data.
