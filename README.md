# Diabetes prediction model

The objective of this project is to classify whether someone has diabetes or not using the SVM  and ensemble (Bagging) methods. The dataset consists of medical variables such as 'Pregnancies', 'Glucose', 'BloodPressure', 'SkinThickness', 'Insulin', 'BMI', 'DiabetesPedigreeFunction', and 'Age' as independent variables, and the 'Outcome' variable as the dependent variable.

The project was carried out in the following steps:

- Data import: The data was read from the 'Diabetes.csv' file using Pandas, and null values were checked in the dataframe.

- Dataset description: The meaning of each column in the dataset was provided.

- Data splitting: The data was grouped by the 'Outcome' column to visualize the distribution of the dependent variable. A count plot was created to visualize the distribution.

- Mean value calculation: The mean values for each feature were calculated based on the 'Outcome' column, distinguishing between diabetic and non-diabetic cases.

- Feature selection: To improve model performance and reduce computational cost, a heatmap was plotted to visualize the correlation between features, aiding in reducing the dataset size.

- Train-Test split: The dataset was split into training and testing sets using stratified sampling on the 'Outcome' variable to maintain the distribution of the dependent variable.

- SVM model: A Support Vector Machine (SVM) model was created and trained on the scaled training data. The model's accuracy was evaluated on both the training and test sets.

- Ensemble method - Bagging: A BaggingClassifier with a base estimator of DecisionTreeClassifier was created. The BaggingClassifier was fitted on the training data, and the out-of-bag score and test accuracy were checked.

- Grid search: Hyperparameter tuning was performed using GridSearchCV to find the best combination of hyperparameters and kernel for the SVM model.

- Experimentation: Predictions were made using both the SVM and Bagging models for an example input data to determine if the patient is diabetic or non-diabetic

- Evaluation and results: The classification report was displayed for both SVM and Bagging models.

## Advantages of SVM:

- Effective in high-dimensional spaces.
- Memory efficient due to using only a subset of training points (support vectors).
- Versatile as different kernel functions can be used.
- Disadvantages of SVM:

- Computationally intensive, especially with large datasets.
- Requires careful selection of kernel and regularization parameters.
- Not suitable for multi-class classification without additional strategies.

  
## Advantages of Bagging:

- Reduces overfitting and improves model generalization.
- Can be parallelized for faster training.
- Suitable for various base estimators.
- Disadvantages of Bagging:

- May not perform well with weak base estimators.
- Requires more memory due to training multiple models.

This summary provides an overview of the project and the steps taken to classify diabetes using SVM and ensemble (Bagging) methods. The results and evaluation of both models are included, along with discussions on their advantages and disadvantages.
