# Mall_Customers-LogisticRegression-DecisionTreeC
Customer Gender Prediction Analysis

This project uses Logistic Regression and Decision Tree classification models to predict customer gender based on their age, annual income, and spending score. The dataset used is Mall_Customers.csv, which contains demographic and spending data for mall customers.

Table of Contents

Dataset Overview

Data Preprocessing

Model Implementation

Performance Evaluation

Dependencies

How to Run the Project

Dataset Overview

The dataset contains 200 records with the following columns:

CustomerID: Unique ID assigned to each customer (not used in modeling).

Gender: Gender of the customer (Male/Female).

Age: Age of the customer.

Annual Income (k$): Annual income of the customer in thousand dollars.

Spending Score (1-100): Score assigned to the customer based on their spending behavior.

Data Preprocessing

Encoding Categorical Variables:

The Gender column is encoded to numerical values using LabelEncoder:

Male: 1

Female: 0

Feature Selection:

Features used for modeling:

Age

Annual Income (k$)

Spending Score (1-100)

Target variable: Gender

Train-Test Split:

The dataset is split into training (90%) and testing (10%) sets using train_test_split.

Standardization:

Features are scaled using StandardScaler to normalize the values and improve model performance.

Model Implementation

1. Logistic Regression

A logistic regression model is trained using the standardized training data.

It predicts the probability of a customer being male or female.

2. Decision Tree

A decision tree classifier with a maximum depth of 5 is used to predict gender.

The tree structure is visualized using the plot_tree function from sklearn.tree.

Performance Evaluation

Logistic Regression Results

Accuracy: 50%

Classification report:

            precision    recall  f1-score   support

         0       0.50      0.80      0.62        10
         1       0.50      0.20      0.29        10

  accuracy                           0.50        20
 macro avg       0.50      0.50      0.45        20

weighted avg       0.50      0.50      0.45        20


### Decision Tree Results
- **Accuracy**: 65%
- Classification report:

          precision    recall  f1-score   support

       0       0.59      1.00      0.74        10
       1       1.00      0.30      0.46        10

accuracy                           0.65        20

macro avg       0.79      0.65      0.60        20
weighted avg       0.79      0.65      0.60        20


### Heatmaps
- Confusion matrices for both models are visualized using heatmaps.

---

## Dependencies

- Python 3.9+
- Required libraries:
- `pandas`
- `numpy`
- `scikit-learn`
- `matplotlib`
- `seaborn`

---

## How to Run the Project

1. Clone the repository:
 ```bash
 git clone <repository-url>
 cd <repository-folder>

Install dependencies:

pip install -r requirements.txt

Place the Mall_Customers.csv file in the working directory.

Run the script:

python main.py

View results, including classification reports and heatmaps, in the terminal and plots displayed during execution.
