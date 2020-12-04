# Unit-10

## Time-Series Forecasting

Inital patterns of the yen futures settle prices indicate significant rises in the dot-com era and following the financial crisis of 2008/2009. The yen decreased in the years 1996-1998 and following 2012. To further analyse the data, we perform a Hodrick-Prescott filter decomposition as well as ARMA and ARIMA modeling.

Unfortunately, we were not able to get a sufficient model for returns with ARMA. Due to the poor autocorrelation and partial autocorrelation, even an order of (2, 1) shows significantly large p-values (greater than 0.05) for our coeffecients. This also held true with ARIMA modeling for the settle prices. We had poor p-values using an order of (5,1,1). Our model however in general predicted a rise in the yen-usd exchange, about four yen over five days.

Using GARCH, we modeled the volatility. The p-values from our analysis of order (2,1) were favorable, but order (1,1) would have produced a better fit. As we can see from the large fluctuation in yen-usd trading price earlier, it makes sense that our model predicted a rise in volatility.

## Regression

A Linear Regression Model was created to train and test the returns of the yen-usd exchange. As noted in the workbook, the out-of-sample root mean squared error (0.4155) is lower than the in-sample root mean squared error (0.5964). While this normally should strike us as odd, keep in mind that the data we're working with is normally quite noisy, and our training/testing data is sparse since we're only looking at a daily basis. To improve a regression analysis, I would first look to increase the frequency of data to either minutes or even seconds.