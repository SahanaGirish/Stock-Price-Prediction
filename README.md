Stock Price Prediction: Tesla and Microsoft
1. Background and History
This project utilizes the Kaggle dataset titled "Stock Market Data (NASDAQ, NYSE, S&P500)" to predict stock prices for Tesla and Microsoft. The dataset provides historical data on stock prices, trading volume, and other financial indicators from major stock exchanges between 1999 and 2022.

1.1 Literature Review
The dataset has been widely used in various studies for trend analysis and predictive modeling of stock prices. Past research has used methods like ARIMA, machine learning techniques, and deep learning models to forecast stock prices. Tesla and Microsoft were selected for this analysis due to their consistent and divergent performance trends: Tesla exhibited rapid growth, while Microsoft demonstrated steady growth, reflecting its mature market position.

1.2 Limitations of Previous Methods
Previous studies faced challenges such as:

Limited feature engineering
Ignoring nonlinear relationships
Overfitting/underfitting due to model selection issues
2. Project Overview
2.1 Objective
The objective of this project is to visualize stock performance indicators, analyze risk-return profiles, and forecast future stock prices using three machine learning models: ARIMA, KNN, and LSTM. The models are evaluated using performance metrics such as MAE, RMSE, and MAPE.

2.2 Dataset
The dataset used is from Kaggle and contains 5.6 million rows, covering data from the NASDAQ, NYSE, and S&P500. The dataset spans from November 1999 to December 2022 and includes parameters like 'Name', 'Date', 'Low', 'Open', 'Volume', 'High', 'Close', and 'Adjusted Close'. The analysis focuses on data from 2010 to 2022, with a specific subset on the top 10 stocks by trading volume.

2.3 Methodology
The following steps were applied:

Exploratory Data Analysis (EDA): To understand data characteristics, relationships, and trends.
Data Cleaning & Preprocessing: Handling missing values, outliers, and ensuring data consistency.
Modeling: Implementing ARIMA, KNN, and LSTM models for forecasting stock prices.
Evaluation: Assessing model performance using MAE, RMSE, and MAPE.
2.4 Evaluation Metrics
The models are evaluated using the following metrics:

Mean Absolute Error (MAE)
Root Mean Squared Error (RMSE)
Mean Absolute Percentage Error (MAPE)
2.5 Expected Results
The goal is to develop an accurate forecasting model, improving on previous studies by incorporating advanced feature engineering and suitable model selection. The project aims to enhance decision-making in stock market investments by providing actionable insights.

3. Results & Discussion
3.1 Dataset Compilation
Data from over 400 CSV files were combined to form a master dataset, then refined to focus on the years 2010–2022.

3.2 Streamlining Dataset for Analysis
The dataset was organized by stock name to focus on the top-selling stocks by volume. Visualizations were created to display opening and closing prices for the top 10 stocks.

3.3 Model Implementation
3.3.1 ARIMA
ARIMA (AutoRegressive Integrated Moving Average) is used to model time series data, considering past values and applying differencing to achieve stationarity. The model was applied to forecast stock prices for Tesla and Microsoft.

3.3.2 KNN (K-Nearest Neighbors)
KNN was used to predict stock prices by averaging the values of the k nearest neighbors based on past data. MinMaxScaler was applied for feature normalization, and GridSearchCV was used to optimize the number of neighbors.

3.3.3 LSTM (Long Short-Term Memory)
LSTM networks were implemented due to their ability to handle long-term dependencies in time series data. This model outperformed ARIMA and KNN in accuracy and error metrics.

3.4 Comparative Results
ARIMA:
Tesla: MAE: 70.03, MAPE: 8.95%, RMSE: 91.18
Microsoft: MAE: 42.57, MAPE: 21.19%, RMSE: 68.36
ARIMA performed better for Microsoft but showed relatively moderate error metrics.

KNN:
Tesla: MAE: 178.25, MAPE: 81.39%, RMSE: 205.44
Microsoft: MAE: 127.05, MAPE: 98.99%, RMSE: 154.66
KNN showed poor performance with high error values and negative R-squared, indicating poor fitting.

LSTM:
Tesla: MAE: 10.77, MAPE: 4.48%, RMSE: 13.20
Microsoft: MAE: 11.34, MAPE: 4.95%, RMSE: 14.55
LSTM outperformed both ARIMA and KNN, showing the lowest errors and best fit.

3.5 Conclusion
LSTM is the most effective model for stock price prediction, with superior accuracy and performance. ARIMA provides moderate results, while KNN is the least suitable for this task. The project demonstrates that LSTM is highly capable of capturing complex, non-linear patterns in stock price data, making it a valuable tool for financial forecasting.
