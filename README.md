# Intellihack_CODEON_Task04

# Stock Price Prediction using Machine Learning

This project demonstrates the use of machine learning to predict stock prices. The goal is to predict the stock's closing price 5 trading days into the future based on historical stock price data.

## Approach

The approach for this project involves several key steps:

1. **Exploratory Data Analysis (EDA)**:
   - The dataset was analyzed to identify relevant patterns and features such as daily returns, moving averages, and volatility.
   - Missing values were handled by forward filling.
   - Feature engineering was performed to add new features such as:
     - **Daily_Return**: The daily percentage change in stock price.
     - **10-Day_MA**: A 10-day moving average of the closing price.
     - **Volatility**: A rolling 10-day standard deviation of the closing price.

2. **Feature Engineering**:
   - Additional features like daily returns, 10-day moving averages, and volatility were created to help the model capture stock price patterns.
   - A new target variable, **Close_5_Days_Ahead**, was created by shifting the closing price by 5 days.

3. **Modeling**:
   - A Linear Regression model was selected for this prediction task.
   - The dataset was split into training and testing sets using an 80-20 split.
   - The model was trained on the scaled features and used to predict the closing price 5 days ahead.

4. **Model Evaluation**:
   - The model was evaluated using statistical metrics: Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE).
   - Simulated trading performance was assessed by comparing cumulative returns based on actual and predicted prices.

5. **Results**:
   - The model was able to predict the stock prices with a reasonable degree of accuracy, but further improvements could be made with more advanced models or feature engineering techniques.

## Key Findings

- **Model Performance**: 
  - The Linear Regression model performed decently in terms of predicting stock prices, with an RMSE that provides insight into prediction accuracy.
  
- **Trading Simulation**:
  - A simulated trading performance was generated by comparing cumulative returns from actual vs predicted closing prices. This gives a practical view of how well the model could be used in real trading scenarios.

- **Model Limitations**:
  - The model does not capture non-linear relationships in the stock market data.
  - More complex models such as ARIMA, LSTM, or Random Forest may improve prediction accuracy.
