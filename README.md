# credit-risk-classification
Week 20 Assignment


# Table of Contents

1. [Challenge Overview](#challenge-overview)

2. [Prerequisties](#prerequisites)
-   [Installation](#installation)
-   [Repository Setup](#repository-setup)
-   [Git Bash Command Example](#git-bash-command-example)

3. [Repository Structure](#repository-structure)

4. [Challenge Instructions](#challenge-instructions)

5. [Credit Risk Analysis](#credit-risk-analysis)

6. [Split and Train Data Code Example](#split-and-train-data-code-example)

7. [Acknowledgements](#acknowledgements)

8. [Author](#author)


# Challenge Overview

This challenge involves building a machine learning model to predict the creditworthiness of borrowers based on historical lending data. Specifically, we aim to identify whether a loan is likely to be healthy (low risk) or high risk (default). The purpose of this analysis is to provide insights that can help a peer-to-peer lending services company better assess loan risk and make informed lending decisions.

We used logistic regression as the machine learning model to classify the loans into healthy (0) and high-risk (1) categories. The performance of the model was evaluated using key metrics such as accuracy, precision, recall, and the confusion matrix.


# Prerequisites
For the Credit Risk Classification Challenge, ensure you complete the following requirements:

## Installation 
- Install Visual Studio Code, and Python on your machine (can use Jupyter Notebook)
- Install the Pandas, Scikit-learn, and Numpy libraries
  - Windows installation process:
  ``` 
      pip install pandas
      pip install numpy 
      pip install scikit-learn
   ```
- Create a new repository called 'Credit-Risk-Classification' in GitHub with README and .gitignore file.

## Repository Setup:
  - Create a new repository called 'credit-risk-classification' in GitHub with a README file
  - Copy the SSH key in GitHub
  - Clone SSH key in directory
  - Navigate into the challenge directory 
  - Create a folder title 'Credit_Risk'
  - Navigate into the 'Credit_Risk' folder
   - Add the StarterCode file and Resources folder in the 'Credit_Risk' folder 
  - Git add, commit, and push changes into the repository


## Git Bash Command Example
Navigate into a working directory. 
```
git clone (add you ssh key)
cd 'Credit-risk-classification'
mdkir Credit_Risk
cd Credit_Risk
git add .
git commit -m "Pushing challenge work"
git push 
```


# Repository Structure
- Credit-Risk-Classification
    - Credit_Risk
        - Resources 
            - lending_data.csv
        - credit_risk_classification.ipynb
    - gitignore
    - README.md


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

    - Healthy Loans (0): the score is 1: 00 illustrating a perfect model to identify healthy loans with less chance of incorrectly labeling the loan status as high-risk. 

    - High-risk Loans (1): the score is 0.87 illustrating that the model predicted 87% of the loans as high-risk correctly with a few false positives. 

- Recall: 

    - Healthy Loans (0): the score is 1.00, signifying that the model correctly identified 100% of all healthy loans. 

    - High-risk Loans (1): the score is 0.95, signifying the model successfully identified 95% of the high-risk loans.


Summary:

The logistic regression model performed well in predicting the loan status, especially for healthy loans with perfect precision and recall. With a high f1-score for both classes, it illustrated the overall prediction to be well-balanced. The confusion matrix highlighted that the model misclassified 32 actual high-risk loans as healthy loans and 86 healthy loans as high-risk. Although the number of misclassifications for both classes is low, there is room for improvement. The better-performing model is the logistic regression which gives a 99% accuracy with no misclassified loan status. Since, the company wants to identify high-risk loans, reducing false positives for high-risk loans would help improve the overall performance of the model. 


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
