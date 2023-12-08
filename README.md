# Elastic-Net-regression-for-Marketing-Mix-Modelling
An example of how the Elastic Net Regression model works for Marketing Mix Modelling purposes.

Assuming we have a dataset of an ecommerce company and we want to evaluate the performance of sales through Marketing Mix Modelling.

This plot is often referred to as the "lambda plot" or "plot of cross-validated error versus lambda" and is particularly useful in Elastic Net models to identify the optimal value of lambda that minimizes the error. Here's what this plot represents:

*X-axis (lambda values): Lambda represents the penalty parameter that controls the strength of regularization in the Elastic Net model. The x-axis displays a range of lambda values.
*Y-axis (Cross-validated error): This axis represents the error metric (often mean squared error or another appropriate error metric) calculated through cross-validation for each corresponding lambda value on the x-axis.
![image](https://github.com/pantelisbart/Elastic-Net-regression-for-Marketing-Mix-Modelling/assets/93544369/df36ec9a-9c07-44c3-87ad-9f969bfc14a7)

The process of finding the optimal lambda value in an Elastic Net model involves using cross-validation to select the value that minimizes the error or achieves the best balance between bias and variance.
We retrieved the lambda value that corresponds to the minimum cross-validated error (lambda_optimal <- enet_model$lambda.min) from the glmnet package's built-in cross-validation process.
Also, we used K-fold cross validation which the method is like this, it divides the dataset into k subsets, iteratively uses k-1 subsets for training, and validates the model on the remaining subset. This process is repeated k times, rotating through each subset as the validation set


![image](https://github.com/pantelisbart/Elastic-Net-regression-for-Marketing-Mix-Modelling/assets/93544369/1593a600-08d3-44f9-b77d-9d1001ee0910)
Interpretation:

Intercept: This represents the baseline or starting value of the target variable (sales) when all predictor variables are zero.
Youtube: For every unit increase in spending on YouTube advertising, sales are estimated to increase by approximately 2.11 units, assuming other predictors remain constant.
Facebook: Similarly, for every unit increase in spending on Facebook advertising, sales are estimated to increase by approximately 1.34 units, assuming other predictors remain constant.
Instagram: Spending on Instagram advertising is associated with an estimated increase of approximately 0.96 units in sales for every unit increase in advertising spending, assuming other factors remain constant.
TikTok: Likewise, spending on TikTok advertising is associated with an estimated increase of approximately 0.74 units in sales for every unit increase in advertising spending, assuming other factors remain constant.
Website: For every unit increase in spending on the website, sales are estimated to increase by approximately 2.43 units, assuming other predictors remain constant.
Seasonality: The impact of seasonality on sales. The value of 471.64 indicates the change in sales attributed to different seasons.
Promotion: For every unit increase in promotion spending, sales are estimated to increase by approximately 4.69 units, assuming other predictors remain constant.
TV: Spending on TV advertising is associated with an estimated increase of approximately 3.08 units in sales for every unit increase in advertising spending, assuming other factors remain constant.
Print: Similarly, spending on print advertising is associated with an estimated increase of approximately 1.71 units in sales for every unit increase in advertising spending, assuming other factors remain constant.


![image](https://github.com/pantelisbart/Elastic-Net-regression-for-Marketing-Mix-Modelling/assets/93544369/4bd4d274-d88e-4a25-9dd0-a5e7742b57a2)
