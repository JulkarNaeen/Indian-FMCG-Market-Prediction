# Indian-FMCG-Market-Prediction

 Volume Prediction
1. Loading and Preparing Data:
   - The code reads stock data from an Excel file (sheet 'Britania').
   - It creates a lagged volume feature to predict the current volume based on the previous volume.
   - Missing values created by the lagging operation are dropped.

2. Splitting Data and Training Model:
   - The data is split into training and testing sets.
   - A Linear Regression model is trained on the training set and used to predict the volume on the test set.

3. Plotting Predictions:
   - The actual and predicted volumes are plotted to visualize the model's performance.

 MACD (Moving Average Convergence Divergence) Calculation
1. Calculating MACD:
   - The code calculates the 12-period and 26-period Exponential Moving Averages (EMA) of the closing prices.
   - The MACD line is computed as the difference between these two EMAs.
   - A signal line (9-period EMA of the MACD) is also calculated.

2. Plotting MACD:
   - The MACD and Signal Line are plotted to visualize the stock's momentum.

 Anomaly Detection using IQR (Interquartile Range)
1. Detecting Anomalies:
   - The code calculates the IQR for the closing prices.
   - It identifies anomalies as those closing prices that fall outside 1.5 times the IQR from the lower and upper quartiles.

2. Plotting Anomalies:
   - The closing prices are plotted with anomalies highlighted as red dots.

 ARIMA Model for Demand Forecasting
1. Loading and Combining Data:
   - Data from multiple sheets in the Excel file is combined into a single DataFrame.
   - The date column is converted to datetime format and used as the index.

2. Aggregating Demand Data:
   - The data is grouped by date, and the total demand (sum of closing prices) is calculated.

3. Fitting and Forecasting with ARIMA:
   - An ARIMA model is fitted to the aggregated demand data.
   - The model forecasts demand for the next 365 days.

4. Plotting Forecast:
   - The historical demand and forecasted demand are plotted to visualize the expected future trend.

 Summary
The code performs the following tasks:
- Predicts stock volume using a Linear Regression model.
- Calculates and plots the MACD for stock momentum analysis.
- Detects and visualizes anomalies in stock closing prices using the IQR method.
- Forecasts future demand using an ARIMA model and plots the historical and forecasted demand.

