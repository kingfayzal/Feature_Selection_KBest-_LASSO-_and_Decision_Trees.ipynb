# Feature Selection Techniques: KBest, LASSO, and Decision Trees

This document demonstrates feature selection using KBest, LASSO, and Decision Trees on two datasets: Iris (categorical target) and Diabetes (numeric target).

## Iris Dataset - Categorical Target

### KBest with Chi-Square
- Utilizes `SelectKBest` with the Chi-Square scoring function.
- Selects top 2 features from the Iris dataset.
- **Selected features**: `petal length (cm)`, `petal width (cm)`.

### Decision Tree Classifier
- Trains a Decision Tree Classifier on the Iris dataset.
- Calculates feature importances based on the trained model.
- **Feature importances**:
  - `sepal length (cm)`: 0.013
  - `sepal width (cm)`: 0.0
  - `petal length (cm)`: 0.564
  - `petal width (cm)`: 0.423

## Diabetes Dataset - Numeric Target

### KBest with F-Regression (ANOVA)
- Utilizes `SelectKBest` with the F-Regression (ANOVA) scoring function.
- Selects top 5 features from the Diabetes dataset.
- **Selected features**: `bmi`, `bp`, `s3`, `s4`, `s5`.

### LASSO (Least Absolute Shrinkage and Selection Operator)
- Applies LASSO regression for feature selection.
- Uses regularization to identify important features.
- **Selected features**: `sex`, `bmi`, `bp`, `s1`, `s3`, `s5`, `s6`.

### Decision Tree Regressor
- Trains a Decision Tree Regressor on the Diabetes dataset.
- Calculates feature importances based on the trained model.
- **Feature importances**:
  - `age`: 0.047
  - `sex`: 0.010
  - `bmi`: 0.234
  - `bp`: 0.078
  - `s1`: 0.084
  - `s2`: 0.054
  - `s3`: 0.065
  - `s4`: 0.016
  - `s5`: 0.344
  - `s6`: 0.069

## Conclusion

This analysis illustrates the application of various feature selection techniques, highlighting their effectiveness in identifying significant features from different types of datasets. KBest, LASSO, and Decision Trees each have unique advantages:

- **KBest** is straightforward and useful for selecting a fixed number of top features.
- **LASSO** provides a method to perform both feature selection and regularization, particularly useful when dealing with high-dimensional data.
- **Decision Trees** offer insights into feature importance through model training, which can be particularly beneficial for understanding feature contributions in complex datasets.

By using these techniques, one can enhance model performance and interpretability, making them essential tools in the data scientist's toolkit.
