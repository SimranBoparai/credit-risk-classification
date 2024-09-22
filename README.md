# Credit Risk Classification 

# Table of Contents

- [Credit Risk Classification](#credit-risk-classification)
- [Table of Contents](#table-of-contents)
- [Challenge Overview](#challenge-overview)
- [Prerequisites](#prerequisites)
  - [Required Tools](#required-tools)
  - [Windows Installation Process](#windows-installation-process)
  - [Repository Setup](#repository-setup)
- [Repository Structure](#repository-structure)
- [Challenge Instructions](#challenge-instructions)
- [Credit Risk Analysis](#credit-risk-analysis)
- [Split and Train Data Code Example](#split-and-train-data-code-example)
- [Acknowledgements](#acknowledgements)
- [Author](#author)


# Challenge Overview

This challenge involves building a machine learning model to predict the creditworthiness of borrowers based on historical lending data. Specifically, we aim to identify whether a loan is likely to be healthy (low risk) or high risk (default). The purpose of this analysis is to provide insights that can help a peer-to-peer lending services company better assess loan risk and make informed lending decisions.

We used logistic regression as the machine learning model to classify the loans into healthy (0) and high-risk (1) categories. The performance of the model was evaluated using key metrics such as accuracy, precision, recall, and the confusion matrix.


# Prerequisites
For the Credit Risk Classification Challenge, ensure you complete the following requirements:

## Required Tools  
- Install Visual Studio Code, and Python on your machine (or Jupyter Notebook)
- Install the Pandas, Scikit-learn, and Numpy libraries

## Windows Installation Process 
  ``` 
      pip install pandas
      pip install numpy 
      pip install scikit-learn
   ```

## Repository Setup
  - Create a new repository called ```credit-risk-classification``` in GitHub with a README file
  - Clone the repository to your local machine: ```git clone https://github.com/your_username/credit-risk-classification.git```
  - Navigate into the repository folder and create a new folder titled ```Credit_Risk```
     - ```mkdir Credit_Risk```
     - ```cd Credit_Risk```
   - Add the starter file ```credit_risk_classification.ipynb``` and Resources folder ```Credit_Risk``` in the folder 
  - Push changes to your GitHub repository
```
git add .
git commit -m "Pushing updated notebook"
git push origin main 
```

# Repository Structure
```
- credit-risk-classification
    - Credit_Risk
        - Resources 
            - lending_data.csv
        - credit_risk_classification.ipynb
    - .gitignore
    - README.md
```


# Challenge Instructions 

Complete the following steps:

1. Split the Data into Training and Testing Sets

2. Create a Logistic Regression Model with the Original Data

3. Write a Credit Risk Analysis Report


# Credit Risk Analysis

Overview of the Analysis: 

- The purpose of this analysis is to build a logistic regression model to predict the loan status of customers, and determine whether their loans are healthy (0) or high-risk (1). By splitting and training the model on multiple features such as loan status and loan size, it evaluated its performance using the confusion matrix and classification report methods to predict the outcome(s). 

The Results:

- Accuracy: the model accurately classified 99% of all loans.

- Precision:
    -  Healthy Loans (0): the score is 1:00, illustrating a perfect model to identify healthy loans with less chance of incorrectly labeling the loan status as high-risk. 

    - High-risk Loans (1): the score is 0.87, illustrating that the model predicted 87% of the loans as high-risk correctly with a few false positives. 

- Recall: 
    - Healthy Loans (0): the score is 1.00, signifying that the model correctly identified 100% of all healthy loans. 
  
    - High-risk Loans (1): the score is 0.95, signifying the model successfully identified 95% of the high-risk loans.


Summary:

The logistic regression model did a great job at predicting loan status, especially for healthy loans, where it was perfect in identifying them with no mistakes. It also had high F1-scores for both healthy and high-risk loans, showing that the model's overall predictions were balanced.

From the confusion matrix, we can see that the model incorrectly predicted 32 high-risk loans as healthy and 86 healthy loans as high-risk. Although these misclassifications are small, there's still room for improvement.

The model's overall accuracy was 99%, which is excellent, but since the company is focused on finding high-risk loans, improving the model's ability to reduce false positives (wrongly labeling healthy loans as high-risk) would make it even better.


# Split and Train Data Code Example

```VS Code
# Import the train_test_learn module
from sklearn.model_selection import train_test_split

# Split the data using train_test_split
# Assign a random_state of 1 to the function
X_train, X_test, y_train, y_test = train_test_split(X,
                                                    y,
                                                    random_state=1,
                                                    stratify=y)
```


# Acknowledgements

I want to mention the following individuals and resources for their assistance and support throughout this assignment: 
- Xpert Learning Assistant and ChatGPT
- Class Activities 


# Author

For any questions or feedback, please contact:
- Name: Gursimran Kaur (Simran)
- Email: kaursimran081999@gmail.com
