# Bitcoin Data Analysis and Price Prediction Report 💰💰

In this report, we present the data analysis and price prediction of Bitcoin using historical data. We used Python libraries such as Pandas, NumPy, Matplotlib, Scikit-learn, and TensorFlow to perform the analysis and build the prediction model.

## Data Description 📊
The dataset used in this analysis is the daily historical price data of Bitcoin, obtained from the CSV file "BTC-Daily.csv". The dataset contains the following columns:

- `unix`: timestamp in Unix format
- `date`: date of the record
- `open`: opening price of Bitcoin on that day
- `high`: highest price of Bitcoin on that day
- `low`: lowest price of Bitcoin on that day
- `close`: closing price of Bitcoin on that day
- `volume`: trading volume of Bitcoin on that day
- `market cap`: market capitalization of Bitcoin on that day
- `symbol`: symbol of Bitcoin (BTC)

## Data Preprocessing🧑🏻‍💻
We performed the following data preprocessing steps:

- Loaded the dataset into a Pandas DataFrame.
- Dropped the 'unix' and 'symbol' columns.
- Converted the 'date' column from Unix timestamp to a human-readable format.
- Applied feature scaling to the dataset using StandardScaler.
- Created a new DataFrame with the scaled data.
- Created a new column 'date' in the scaled DataFrame.
- Split the dataset into training and testing sets.

## Data Visualization 📈
We visualized the data using Matplotlib to plot the high, low, open, and close prices against the date.
#### Visualisation of High and Low prices against Date
![image](https://github.com/ShevindiRodrigo/Bitcoin-Prediction-Analysis/assets/36123591/c3151c8e-20df-472d-8f21-723a5c650315)

#### Visualisation of Open and Close prices against Date
![image](https://github.com/ShevindiRodrigo/Bitcoin-Prediction-Analysis/assets/36123591/25bac901-1a5b-4dab-b494-9fdeaf3f1e09)


## Price Prediction Model 🧑🏻‍💻
We used a Long Short-Term Memory (LSTM) model to predict the closing price of Bitcoin. We performed the following steps to build the model:

- Defined the target variable as the closing price.
- Created a new DataFrame with the first three columns as features and the closing price as the target variable.
- Applied feature scaling to the feature DataFrame using StandardScaler.
- Created a new DataFrame with the scaled feature data.
- Defined a function to create a windowed dataset for the LSTM model.
- Split the windowed dataset into training and testing sets.
- Created a new LSTM model with one LSTM layer and one Dense layer.
- Compiled the model with the mean absolute error loss function and the Adam optimizer.
- Trained the model on the training set.
- Predicted the closing price on the testing set.

## Results and Discussion 📊📈
Visualizations of the predicted stock prices and compare them with the actual prices.
![image](https://github.com/ShevindiRodrigo/Bitcoin-Prediction-Analysis/assets/36123591/0e28c202-3e03-416f-bc79-93f3c6efb1f3)

## Model Evaluation📈
We evaluated the model using the Root Mean Squared Error (RMSE) metric. The RMSE value for the LSTM model is 0.4332522009569052.

## Simple Moving Average Model 🧑🏻‍💻
We also implemented a Simple Moving Average (SMA) model for comparison. We calculated the 100-day moving average of the closing price and plotted it against the actual closing price. The Mean Squared Error (MSE) value for the SMA model is 2.065719208442753

## Conclusion 📈
In this report, we presented the data analysis and price prediction of Bitcoin using historical data. We used an LSTM model to predict the closing price and evaluated the model using the RMSE metric. We also implemented a SMA model for comparison. The LSTM model outperformed the SMA model with a lower RMSE value. However, the model still has room for improvement, and further tuning and optimization may be necessary to increase the accuracy of the predictions.
