# Unit 10—A Yen for the Future

![Yen Photo](https://media.istockphoto.com/photos/financial-succes-japanese-yen-bills-and-progress-chart-picture-id175198866)

Executive Summary


 Various time-series tools are tested to determin if they could be used to predict future movements in the value of the Japanese yen versus the U.S. dollar.

 Tasks:

1. Time Series Forecasting
2. Linear Regression Modeling


- - -

### Files


[Time-Series Notebook](Starter_Code/time_series_analysis.ipynb)

[Linear Regression Notebook](Starter_Code/regression_analysis.ipynb)

[Yen Data CSV File](Starter_Code/yen.csv)

- - -


#### Time-Series Forecasting

Analyzed historical Dollar-Yen exchange rate futures data by applying time series analysis and modeling to determine whether there is any predictable behavior.

Steps in the time-series 

1. Decomposition using a Hodrick-Prescott Filter (Decompose the Settle price into trend and noise).

![Hodricks](https://github.com/TaylorTucker/Time_Series/blob/main/Images/Hodrick_Settle.PNG?raw=true)
![Hodricks](https://github.com/TaylorTucker/Time_Series/blob/main/Images/Hodrick_Noise.PNG?raw=true)

---

2. Forecasting Returns using an ARMA Model.

![ARMA](https://github.com/TaylorTucker/Time_Series/blob/main/Images/ARMA_Results.PNG?raw=true)
![ARMA](https://github.com/TaylorTucker/Time_Series/blob/main/Images/ARMA_Chart.PNG?raw=true)

---

3. Forecasting the Settle Price using an ARIMA Model.

![ARIMA](https://github.com/TaylorTucker/Time_Series/blob/main/Images/ARIMA_Results.PNG?raw=true)
![ARIMA](https://github.com/TaylorTucker/Time_Series/blob/main/Images/ARMA_Chart.PNG?raw=true)

---

4. Forecasting Volatility with GARCH.

![GARCH](https://github.com/TaylorTucker/Time_Series/blob/main/Images/GARCH_Results.PNG?raw=true)
![GARCH](https://github.com/TaylorTucker/Time_Series/blob/main/Images/GARCH_Chart.PNG?raw=true)

---

### Conclusion

Based on the time series analysis, it does not appear to be a good time to buy the YEN. Though, the price is projected to increase, the retures are projected to decrease.  Also, an increase in volatility is projected meaning there is a possibility of increased future risk.

With all models missing the (P < 0.05) qualifier, I would not feel confident in using these models for trading.

---

#### Linear Regression Forecasting

Built Scikit-Learn linear regression model to predict Yen futures ("settle") returns with *lagged* Yen futures returns and categorical calendar seasonal effects (e.g., day-of-week or week-of-year seasonal effects).

Steps in the regression_analysis:

1. Data Preparation (Creating Returns and Lagged Returns and splitting the data into training and testing data)

![Lagged](https://github.com/TaylorTucker/Time_Series/blob/main/Images/Lagged_Returns.PNG?raw=true)
![Lagged](https://github.com/TaylorTucker/Time_Series/blob/main/Images/Lagged_Returns_2.PNG?raw=true)

---

2. Fitting a Linear Regression Model.

![Lagged](https://github.com/TaylorTucker/Time_Series/blob/main/Images/FIT.PNG?raw=true)

---

3. Making predictions using the testing data.

![Lagged](https://github.com/TaylorTucker/Time_Series/blob/main/Images/Predicted_Return.PNG?raw=true)
![Lagged](https://github.com/TaylorTucker/Time_Series/blob/main/Images/Predicted_Return_PLOT.PNG?raw=true)
![Lagged](https://github.com/TaylorTucker/Time_Series/blob/main/Images/Predicted_Return_PLOT_2.PNG?raw=true)

---

4. Out-of-sample performance.

![Lagged](https://github.com/TaylorTucker/Time_Series/blob/main/Images/OUT_RMSE.PNG?raw=true)

---

5. In-sample performance.

![Lagged](https://github.com/TaylorTucker/Time_Series/blob/main/Images/IN_RMSE.PNG?raw=true)

---

### Conclusion

 This model performs better on out-of-sample data compared to in-sample data given the lower RMSE.

- - -

### Hints and Considerations

* Out-of-sample data is data that the model hasn't seen before (Testing data).
* In-sample data is data that the model was trained on (Training data).

- - -

### Submission

* Create Jupyter Notebooks for the analysis and host the notebooks on GitHub.

* Include a Markdown that summarizes your models and findings and include this report in your GitHub repo.

* Submit the link to your GitHub project to Bootcampspot.
