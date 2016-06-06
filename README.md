##Sales Forecast of Automobile Cars using R programming.

###Objectives

- To  forecast  the  sales  made  by  an  an automobile  company  every  month.  
- To  show  the  use  of  ARIMA  model in forecasting. 

###Method:

The  data  used  to  forecast  were  from  the  total  sale  of  bolero cars  for  each  end  of  the  month  from  2013  to  
2014. The statistical forecasting method used is the ARIMA time series with the regression model. 

####Step 1:
- Plot tractor sales data as time series.

####Step 2:
- Difference data to make data stationary on mean (remove trend).
- This to remove the upward trend through 1st order differencing the series using the following formula: Y_{t}^{'}=Y_t-Y_{t-1} 

####Step 3:
- log transform data to make data stationary on variance.
- The following equation represents the process of log transformation mathematically: Y_{t}^{new}=log_{10}(Y_t) 

####Step 4:
- Difference log transform data to make data stationary on both mean and variance.
- Formula:  Y_{t}^{new'}=log_{10}(Y_t) -log_{10}(Y_{t-1}) 

####Step 5: 
- Plot ACF and PACF to identify potential AR and MA model.
- Autocorrelation factor (ACF) and Partial autocorrelation factor (PACF) plots are used to identify patterns in the data obtained from step 4 which is stationary on both mean and variance. 
- The idea is to identify presence of AR and MA components in the residuals.

####Step 6:
- Identification of best fit ARIMA model.
- Auto arima function in forecast package in R helps us identify the best fit ARIMA model on the fly.
- The best fit model is selected based on Akaike Information Criterion (AIC) , and Bayesian Information Criterion (BIC) values.
- The idea is to choose a model with minimum AIC and BIC values.

####Step 7:
- Forecast sales using the best fit ARIMA model.
- Also don't forget to plot ACF and PACF for residuals of ARIMA model to ensure no more information is left for extraction.

