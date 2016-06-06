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

###Results:
- With  a  seasonable  ARIMA  model, the prediction plot of sales was obtained for the first half of year 2015. 
- Click [here](https://github.com/nirbhayph/Sales-Forecast-of-Automobile-Cars-using-R/blob/master/Result/Sales_Forecast_Output_Plots.pdf) to view the results and plots obtained according to the steps stated above.

###Conclusions:
- ARIMA  time  series  are  useful  models  to  predict  the  sales  of  automobile cars  for  this  company.  From  this project, we can conclude that ARIMA and Regression models can be used by other businesses for planning. 

###Also you can click [here](https://github.com/nirbhayph/Sales-Forecast-of-Automobile-Cars-using-R/tree/master/Data_Dump) to view the data dump for years 2013-2014. 

###Software Requirements

- R

  To install R for your operating system click [here](https://cran.rstudio.com/).
  
- R Studio 
  
  To install R Studio for your operating system click [here](https://www.rstudio.com/products/rstudio/download/).
  
###Package Requirement

- Forecast

###To install a package to your computer

- Method 1: Install from source

  Download the add-on R package, say mypkg, and type the following command in Unix console to install it to /my/own/R-packages/:

  $ R CMD INSTALL mypkg -l /my/own/R-packages/

- Method 2: Install from CRAN directly

  Type the following command in R console to install it to /my/own/R-packages/ directly from CRAN:

  install.packages("mypkg", lib="/my/own/R-packages/") 

###To Load the library

- library("mypkg", lib.loc="/my/own/R-packages/")


