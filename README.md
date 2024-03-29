## Boston Public Library-Energy Time Series Analysis
![Datascience logo](logo.png)
### This is a time regression analysis of the electrical energy consumption of the Boston Public Library.
### AutoRegressive Integrated Moving Average
Using a class of statistical models for analyzing and forecasting time series data
- AR: Autoregression A model uses the dependent relationship between an observation and some number of lagged observations
- I: Integrated. The use of differencing of raw observations (e.g. subtracting an observation from an observation at the previous time step) in order to make the time series stationary.
- MA: Moving Average. A model that uses the dependency between an observation and a residual error from a moving average model applied to lagged observations.

components are explicitly specified in the model as a parameter. A standard notation is used of ARIMA(p,d,q) 
- p: The number of lag observations included in the model, also called the lag order.
- d: The number of times that the raw observations are differenced, also called the degree of differencing.
- q: The size of the moving average window, also called the order of moving average.
A linear regression model is constructed including the specified number and type of terms, and the data is prepared by a degree of differencing in order to make it stationary, i.e. to remove trend and seasonal structures that negatively affect the regression model.

Differencing removes the changes in the level of a time series, eliminating trend and seasonality and consequently stabilizing the mean of the time series.
Seasonal Differencing, which involves computing the difference between an observation and the corresponding observation in the previous year.

ARIMA models are atheoretic models, so the usual rules of interpreting estimated regression coefficients do not strictly apply in the same way. ARIMA models have certain features to be aware of.

prediction is controlled by the daates chosen in the model call
predictions = model.predict('2018-01-05 14:00:00','2018-01-30 08:00:00',dynamic=True)
start time has to be between initial start time and next data time point
Stop time has to be after final data point time
