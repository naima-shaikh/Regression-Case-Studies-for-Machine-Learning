## Random Forest Regressor 

 Hyperparameters to Tune:
- n_estimators: Number of trees in the forest.
- max_depth: Maximum depth of individual trees.
- min_samples_split: Minimum samples required to split an internal node.
- min_samples_leaf: Minimum samples required to be at a leaf node.
- max_features: Number of features to consider for the best split.

Tuning Method: RandomizedSearchCV is generally preferred due to the larger hyperparameter space.

## Decision Tree Regressor

 Hyperparameters to Tune:

- max_depth: Limits tree depth.
- min_samples_split: Minimum samples for splitting a node.
- min_samples_leaf: Minimum samples at a leaf.
- max_features: Features to consider for splitting.

Tuning Method: GridSearchCV is suitable given the smaller hyperparameter space.

## Feature Selection-Based Modeling:

1- Identify Top 5 Features: Use feature_importances_ from the tuned Random Forest.
2- Retrain Models: Retrain Linear Regression, Decision Tree (optimized), and Random Forest (optimized) with only these top 5 features.
3- Compare Results: Compare performance metrics (R-squared, MAE, RMSE) before and after feature selection.

 ## Handling Multicollinearity in Linear Regression 

  Detection:
 - Correlation Matrix: Look for high correlation coefficients between independent variables.

## Addressing (if detected):
- Feature Removal: Remove highly correlated features.
- Feature Combination: Create new features from correlated ones.
- Regularization: Ridge or Lasso regression (though not explicitly requested, they handle multicollinearity).
 

