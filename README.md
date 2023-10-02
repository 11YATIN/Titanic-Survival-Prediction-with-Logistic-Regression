# Titanic-Survival-Prediction-with-Logistic-Regression
## Project Description

This Python script aims to predict the survival status of passengers on the Titanic using logistic regression. The project involves data preprocessing, model training, testing, and generating final predictions for a test dataset.

## Key Steps in the Code

1. **Data Preprocessing**
    - Reading the training dataset from "Train.csv" and removing unnecessary columns like "Name" and "Ticket."
    - Handling missing data: Filling missing values in "SibSp" and "Parch" columns with their respective means.
    - Creating a new feature "Family_member" by combining "SibSp" and "Parch" to represent the family size.
    - Converting the "Sex" column to binary values (1 for female, 0 for male).
    - Handling the "Cabin" column by marking presence (1) or absence (0).
    - Filling missing values in the "Age" and "Embarked" columns with their means.
    - Encoding the "Embarked" column with numeric values (0, 1, 2).

2. **Data Splitting**
    - Splitting the dataset into features (x_train) and the target variable (y) for model training.
    - Using the `train_test_split` function to create training and testing sets for model evaluation.

3. **Model Training**
    - Utilizing logistic regression with specific configurations, such as "newton-cg" solver, a large number of iterations, and regularization strength (C).
    - Fitting the model with the training data.

4. **Model Evaluation**
    - Making predictions (y_pred) on the test data.
    - Calculating the accuracy of the model by comparing predictions to the actual values in the test dataset.

5. **Final Predictions**
    - Reading the test dataset from "Test.csv" and performing similar preprocessing steps.
    - Applying the trained logistic regression model to predict survival on the test dataset (y_final_predictions).
    - Saving the final predictions to a CSV file named "Final_Predictions.csv."

## Performance

The code reports a maximum accuracy of 83%, indicating that the logistic regression model successfully predicts the survival status of Titanic passengers. The accuracy score serves as a measure of the model's effectiveness in classifying passengers as survivors or non-survivors based on the provided features.

Overall, this project demonstrates the application of logistic regression in predicting outcomes, making it valuable for tasks involving binary classification like survival prediction. The provided code can serve as a foundation for similar predictive modeling tasks.
