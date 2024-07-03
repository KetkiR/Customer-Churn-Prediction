# Credit Card Customer Churn Prediction

This project aims to predict customer churn for a credit card company using a neural network model implemented in TensorFlow and Keras.

## Project Overview

Customer churn is a significant issue for businesses, particularly in the financial sector. Predicting which customers are likely to leave (churn) can help companies take proactive measures to retain them. This project uses historical customer data to build a predictive model for churn using a neural network.

## Dataset

The dataset used for this project is the "Churn_Modelling.csv" file, which contains information about 10,000 credit card customers. The dataset includes the following features:

- RowNumber: Row index
- CustomerId: Unique identifier for each customer
- Surname: Customer's surname
- CreditScore: Customer's credit score
- Geography: Country of the customer
- Gender: Gender of the customer
- Age: Age of the customer
- Tenure: Number of years the customer has been with the bank
- Balance: Account balance
- NumOfProducts: Number of products the customer has with the bank
- HasCrCard: Does the customer have a credit card (1=Yes, 0=No)
- IsActiveMember: Is the customer an active member (1=Yes, 0=No)
- EstimatedSalary: Estimated annual salary of the customer
- Exited: Has the customer exited (1=Yes, 0=No)

## Project Steps

1. **Data Loading and Exploration**: 
    - Load the data using pandas.
    - Explore the dataset to understand the structure and distribution of the data.

2. **Data Preprocessing**:
    - Drop unnecessary columns (`RowNumber`, `CustomerId`, `Surname`).
    - Handle categorical variables using one-hot encoding (`Geography`, `Gender`).
    - Split the data into training and test sets.
    - Standardize the features using `StandardScaler`.

3. **Model Building**:
    - Build a neural network model using TensorFlow and Keras.
    - The model has three dense layers:
        - First layer with 11 neurons and ReLU activation.
        - Second layer with 11 neurons and ReLU activation.
        - Output layer with 1 neuron and sigmoid activation.

4. **Model Training**:
    - Compile the model using binary cross-entropy loss and Adam optimizer.
    - Train the model on the training data for 100 epochs, with a validation split of 20%.

5. **Model Evaluation**:
    - Evaluate the model's performance on the test data.

## Requirements

- Python 3.x
- Pandas
- NumPy
- Scikit-learn
- TensorFlow
- Keras

## Usage

To run the project, ensure you have the required libraries installed. You can install them using pip:

```bash
pip install pandas numpy scikit-learn tensorflow
