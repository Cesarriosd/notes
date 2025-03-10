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

### 5.1 Simple models
Linear Regression

Multiple linear regression
- In this case we have multiple predictors and the coefficients measure the *marginal effects* of the predictor variables.

To estimate the coefficients we use least squares principles minimising the sum of the squared errors. This is called least squares estimation.

### 5.2 Goodness of fit

R²: Coefficient of determination, the square of the correlation between the observed y values and the predicted y values. It reflects the proportion of variation in the forecast variable that is accounted for (or explained) by the regression model. 
0 above R² above 1, if the predictions are close to the actual values R² will be closer to 1, if not it will be closer to 0.

#### Standard error of the regression

This is related to the size of the average error that the model produces. We can compare this error to the sample mean of y to gain some perspective of the accuracy of the model. This is also used to create the confidence intervals.

### 5.3 Evaluating the regression model

Residuals are the impredictable component of the associated observation.

### 5.4 ACF plot of residuals

#### Breush-Godfrey test (LagrangeMultiplyier test fro serial correlation)

It is used to test the joint hypothesis that there is no autocorrelation in the residuals up to a recatin specified order. A small p-value indicates ther is significant autocorrelation remaining in the residuals.

This test is similar to Ljung-box test but designed to work with series.

#### Histogram of the residuals

It is important to check if the residuals are normally distributed

#### Residual plots against predictors
 You can plot the residuals against the predictors and if everthing is ok there must not be a pattern there. In other case, some non linear relationship will remain in the data and must be corrected. 
 You can also plot residuals against some variable that is not included in the model and if this shows a pattern you could try to include it in the model maybe in a non linear way.
 
#### Residual plots against fitted values

A plot of the residuals against the fitted values should also shon no pattern. If a pattern is observed the residuals may have heteroscedasticity, that means that the variance of the errors is not constant.
If this occurs some transfomation must be applied to the forscast variable as logaritmic or square root.

#### Outliers and influential observation

Outlier: An extreme value compared with the mayority of the data.
Influentia observation: Observations that have a large influence on the estimated coefficients.

#### Spurious regression

Non-stationary time series: it does not fluctuate around a constant mean or with constant variance.

High R² and high residual autocorrelation can be signs of spurious regression. 

#### Some usefull predictors 

- Trend: you can use a linear model to include trend.
- Dummy variables: You can add dummy variables to inlcude categorical variables. But you must to be aware about dummy variable trap. The number of dummies will be categories -1.
The intepretation of each of the coefficients associated with the dummy variables is that it is a measure of the effect of that category relative to the ommited category.


#### Intervention variables
It is often necessary to model interventions that may have affected the variable to be forecast. For example, competitor activuty, advertising expanditure
industrial action, and so on, can all have an effect.

Spike variable: When the effect lasts only for one period we use an spike variable. This is a dummy variable that takes value 1 in the period of intervention and zero elsewhere.
Step variable: We use this to capture immediate and permanet effect. This takes zero value before the interention and 1 after the intervention.

#### Trading days

The number of traiding day can vary significantly and can hace substantial effects on sales data. So 
you can include the number of trading days in the month or another features, for examle number of sundays in the month.

#### Distributed lags

It us often useful to include advertising expenditure as a predictor. However, since the effect of the advertising can last beyond the actual campaign, we need to includelagged values of advetising expenditure
So, the following predictors could be used.

- Advertising for the previous month;
- Advertising for two months previously.
- Advertising for m months previously.


#### Easter

In this case you must to include a dummy variable that will impact depending on the period of time in which the holiday occurs.

#### Fourier Series

Fourier terms: These are calculated in terms of sin and cosine, and are useful when you have a long seasonality period m, for example weekly data. 
Fourier shown that a series of cosine and sine terms of the right frecuencies can approximate any periodic function. In this terms, you can calculate a series of fourier terms as feautures.

If you use the first two Fourier terms, the seasonal pattern will follow simple sine wave. If a regression model contains fourier terms is often called harmonic regression because the sucessive Fourier terms represent harmonics of the first two Fourier terms.

### 5.5 Selecting predictors

- R² us bit a good measure of the predictive ability a model, beacause it measures the correlation, but not the actual errors.
Another problem is that R² tends to be higher if we include more predictors, even fi those predictors are irrelevant.
Optimize forecasting using R² will conduct to overfitting.
-  Minimising the Sum of Squared Errors is an equivalent of maximising R² and will always choss the model with the most variables.

An alternative which is designed to overcome these problems is the "adjusted R²"

#### Cross validation

For regression models, it is also possible to use classical leave-one-out cross-validation to select predictors.

#### Akaike's information criterion

action
If the number of observations is large minimising the AIC is equivalent to minimising the CV value.

#### Corrected Akaike's information criterion

For small number of observations 
AICc

#### Schwarz's Bayesian information criterion

BIC: minimising the BIC is inteded to give the best model. This criterion penalises the number of parameters morea heavily that the AIC.

#### Which measure should we use

They recommed AICc, AIC or CV


#### Best subset regression

If you fit all models possible using predictor variables you are using a best subset regression method. 

#### Stepwise regression 

If there are to many predictors best subset regression is not possible. So, you can use backwards stepwise regression.
Steps:
- Start with the model containing all potential predictors.
- Remove one predictor at a time. Keep the model if it improves the measure of predictive accuracy.
- Iterate until no further improvement.

If the number of potential predictors is too large, you can use forward stepwise regression.

Steps:

- Start with a model that includes only the intercept and predictors are added one at a time. and the one that most improves the measure of predictive accuracy is retained in the model.
- Iterate until no further improvement.

Alternatively you can use hybrid procedures:

Steps:
- Start with a model that include a subset of potential predictors. 
- Do backward or forward procedures.

### 5.6 Forecasting with regression

For this 



