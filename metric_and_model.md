# ML Data Challenge 1 - Cargo Volume
Dominic Fernandez, University of San Francisco


<hr>

# Final Results (TLDR)

## Best Metric
The metric I am choosing to evaluate my model is `mean squared error (MSE)`. I am choosing MSE because it measures prediction errors well. At first, I was tempted to choose r-squared as my metric because it is easier and nicer to see a percentage as an accuracy score, but the objective of this challenge is to predict values for a test set that my model has not yet seen, so evaluating my model on prediction errors is of more value to me.

<b>My best MSE was <mark>(98.7996695985)^2 or 9761.374712765815</mark></b>

(For reference, my r-squared for the same model was <b>0.9498589744651128</b>)

## My Model
<b>My best performing model was a <mark>Random Forest Regressor</mark></b>.
- MSE: (98.7996695985)^2 or 9761.374712765815
- r-squared: 0.9498589744651128
- Execution time to predict target for test set: <b>0.19011902809143066 sec.</b>

### Models I explored in this challenge:
I explored  `linear regression` because there are some features I engineered that are pretty well correlated to the target variable (both negatively and positively, but more so positively correlated), so linear regression may be a suitable model. 

I explored `random forest regressor` because although there are some features that correlated with the target variable, not all of them do. Since random forest regressors are good at working with non-linear features, I am leveraging this model to account for the features I engineer that have a non-linear relationship with the target variable (and many likely will, since there are many more categorical features than continuous features in this dataset.  <b>Random forest regressor worked especially well after feature engineering values from 1 to N for each unique value in each categorical feature.</b>

## Output
See `dc1.csv` for the target variable predictions on the test set

<hr>