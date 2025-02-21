## Chapter 4: Judgmental forecast
When this forecast use to be used: 
- Lack of historical data,
- new products are launched
- new competitors enter to the market,
- completely new and unique market conditions

## Chapter 5: Regression Models
Concepts:
- Forecast variable y, dependent pr explained variable,
- Predictor variable x: regressors, independent or explanatory variables.

### Simple models
Linear Regression

Multiple linear regression
- In this case we have multiple predictors and the coefficients measure the *marginal effects* of the predictor variables.

To estimate the coefficients we use least squares principles minimising the sum of the squared errors. This is called least squares estimation.

### Goodness of fit

R²: Coefficient of determination, the square of the correlation between the observed y values and the predicted y values. It reflects the proportion of variation in the forecast variable that is accounted for (or explained) by the regression model. 
0 above R² above 1, if the predictions are close to the actual values R² will be closer to 1, if not it will be closer to 0.

### Standard error of the regression

This is related to the size of the average error that the model produces. We can compare this error to the sample mean of y to gain some perspective of the accuracy of the model. This is also used to create the confidence intervals.

## Evaluating the regression model

Residuals are the impredictable component of the associated observation.

### ACF plot of residuals

#### Breush-Godfrey test (LagrangeMultiplyier test fro serial correlation)

It is used to test the joint hypothesis that there is no autocorrelation in the residuals up to a recatin specified order. A small p-value indicates ther is significant autocorrelation remaining in the residuals.

This test is similar to Ljung-box test but designed to work with series.

#### Histogram of the residuals

It is important to check if the residuals are normally distributed

#### Residual plots against predictors
 You can plot the residuals against the predictors and if everthing is ok there must not be a pattern there. In other case, some non linear relationship will remain in the data and must be corrected. 
 You can also plot residuals against some variable that is not included in the model and if this shows a pattern you could try to include it in the model maybe in a non linear way.
 
####

