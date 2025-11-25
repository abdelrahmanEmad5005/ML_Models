#Linear Regression, Ridge, and Lasso Regression on Auto MPG Dataset

This notebook explores Linear Regression models on the UCI Auto MPG dataset, comparing Simple Linear Regression, Ridge Regression (L2), and Lasso Regression (L1). It demonstrates data preprocessing, model training, evaluation, and the use of polynomial features to understand model behavior.

#Dataset

Source: UCI Auto MPG dataset

Features: cylinders, displacement, horsepower, weight, acceleration, model year, origin

Target: mpg (miles per gallon)

Missing values in horsepower are replaced with median values.

car name column is dropped as it is non-numeric.

#Preprocessing

Convert non-numeric data to numeric.

Handle missing values.

Scale features using StandardScaler.

Visualize distributions and outliers.

Polynomial features (degree 2, interaction only) added to analyze feature interactions.

#Models Implemented
1. Simple Linear Regression

Fits a line minimizing the sum of squared errors.

Coefficients indicate contribution of each feature.

Baseline performance: R² ≈ 0.85 on test set.

2. Ridge Regression (L2 Regularization)

Adds L2 penalty to reduce overfitting.

Keeps all features, shrinks coefficients slightly.

Performance similar to linear regression: R² ≈ 0.85.

3. Lasso Regression (L1 Regularization)

Adds L1 penalty, encouraging sparsity.

Many coefficients set to zero, effectively performing feature selection.

Slightly lower R² (~0.83) but reduces number of features used.

Useful for dimensionality reduction.

#Polynomial Features Analysis

Polynomial features used to study feature interactions.

Ridge and Lasso applied on polynomial-transformed data.

Lasso eliminates irrelevant polynomial terms while maintaining high accuracy (~86% R²).

#Observations

Linear and Ridge regression perform similarly on scaled data.

Lasso reduces dimensions significantly while keeping competitive performance.

Feature selection via Lasso improves model interpretability.

Polynomial transformations help capture interactions between features.
