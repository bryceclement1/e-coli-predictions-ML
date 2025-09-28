# e-coli-predictions-ML

In this project, we implemented ML models to predict E. coli concentrations in 2 Great Lakes sites.<br/>
We replicated the USGS study on E. coli level predictions: https://www.sciencebase.gov/catalog/item/5fe22dead34e30b9123f09b5. We created models for Beach 6 and Huntington Beach. We used an 80/20 train-test split on the data and a 5-fold cross-validation on the training data. We tested Ridge, LASSO, SGDRegressor, and PolyRidge models. GridSearchCV was used to tune hyperparameters.

## Beach 6 model
Features for Beach 6 included: turbidity, relative humidity, water temperature, number of birds, lake level change, wind speed, and rainfall.
Ridge(alpha=30) was the best-performing model for Beach 6. The R-squared value on the test data was 0.488726.

## Huntington Beach model
Features for Huntington Beach included: lake temperature, lake turbidity, wave height, lake level change, and rainfall.
PolyRidge(degree=2, ridge__alpha=10) was the best performing model for Huntington beach. The R-squared value on the test data was 0.565904.
