# kaggle-Competition-Binary-Classification-of-Machine-Failures
## Feature Engineering
* Create new features by performing operations such as multiplication and subtraction between features. For example, subtracting air temperature from processing temperature to obtain "Temperature Difference" or multiplying torque by rotation speed to obtain "Power."
* Encode the machine category (Type) and product ID using Label encoding.
* Replace outliers that fall outside the normal range with the feature's Q1-1.5*IQR and Q3+1.5*IQR values. Finally, standardize the data.

## Building Machine Learning Models
* Utilize 10 models, including XGBoost, three parameter variations of LightGBM, three parameter variations of Catboost, Random Forest, Logistic Regression, and Hist Gradient Boosting.

## Stratified Cross-Validation
* Set up stratified cross-validation with k=10 to confirm the accuracy of the models.

## Ensemble Model 
* Employ an ensemble model that weights the predictions from all models. The weights for each model are determined by optuna, which optimizes the weights based on the predictions of the training set.
