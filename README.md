# Customer-churn-prediction
Problem Statement¶
Here we have telecom company offering mobile services to there customer. They have noticed that some long time customers leaving for compititors. We need to identify

Why this problem happening ?
How we can prevent this problem ?
How much churn rate is going to happen ?
Importance of customer churn prediction
Predicting and analysing customer churn is a crucial for telecom company
It allows them to identify which customer at rick of leaving and take step to retain them
By doing so , we can reduce revenue loss, maintain customer loyalty and even gain a compatitve edge in the market


## Data overview
Data Overview

Number of rows: 
 667
Number of features: 
 20
List of features: 
 ['State', 'Account length', 'Area code', 'International plan', 'Voice mail plan', 'Number vmail messages', 'Total day minutes', 'Total day calls', 'Total day charge', 'Total eve minutes', 'Total eve calls', 'Total eve charge', 'Total night minutes', 'Total night calls', 'Total night charge', 'Total intl minutes', 'Total intl calls', 'Total intl charge', 'Customer service calls', 'Churn']
Number of categorical features: 
 3
Number of numberical features: 
 17
Descriptive for of the data: 
        Account length   Area code  Number vmail messages  ...  Total intl calls  Total intl charge  Customer service calls
count      667.000000  667.000000             667.000000  ...        667.000000         667.000000              667.000000
mean       102.841079  436.157421               8.407796  ...          4.527736           2.764948                1.563718
std         40.819480   41.783305              13.994480  ...          2.482442           0.758167                1.333357
min          1.000000  408.000000               0.000000  ...          0.000000           0.000000                0.000000
25%         76.000000  408.000000               0.000000  ...          3.000000           2.320000                1.000000
50%        102.000000  415.000000               0.000000  ...          4.000000           2.840000                1.000000
75%        128.000000  415.000000              20.000000  ...          6.000000           3.255000                2.000000
max        232.000000  510.000000              51.000000  ...         18.000000           4.940000                8.000000

[8 rows x 16 columns]
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 667 entries, 0 to 666
Data columns (total 20 columns):
 #   Column                  Non-Null Count  Dtype  
---  ------                  --------------  -----  
 0   State                   667 non-null    object 
 1   Account length          667 non-null    int64  
 2   Area code               667 non-null    int64  
 3   International plan      667 non-null    object 
 4   Voice mail plan         667 non-null    object 
 5   Number vmail messages   667 non-null    int64  
 6   Total day minutes       667 non-null    float64
 7   Total day calls         667 non-null    int64  
 8   Total day charge        667 non-null    float64
 9   Total eve minutes       667 non-null    float64
 10  Total eve calls         667 non-null    int64  
 11  Total eve charge        667 non-null    float64
 12  Total night minutes     667 non-null    float64
 13  Total night calls       667 non-null    int64  
 14  Total night charge      667 non-null    float64
 15  Total intl minutes      667 non-null    float64
 16  Total intl calls        667 non-null    int64  
 17  Total intl charge       667 non-null    float64
 18  Customer service calls  667 non-null    int64  
 19  Churn                   667 non-null    bool   
dtypes: bool(1), float64(8), int64(8), object(3)
memory usage: 99.8+ KB
None
Number of missing values: 
 0
Number of unique values: 
 State                      51
Account length            179
Area code                   3
International plan          2
Voice mail plan             2
Number vmail messages      37
Total day minutes         562
Total day calls           100
Total day charge          562
Total eve minutes         557
Total eve calls            94
Total eve charge          528
Total night minutes       568
Total night calls          96
Total night charge        453
Total intl minutes        132
Total intl calls           17
Total intl charge         132
Customer service calls      9
Churn                       2
dtype: int64

## Conclusion on XGBoost Classifier 

- **Accuracy and Cross-Validation:**

The model demonstrates a high level of accuracy, with an average score of approximately **0.9266** across five-fold cross-validation. This indicates that the model is capable of making accurate predictions on the given dataset.

- **Confusion Matrix and Classification Report:**

The confusion matrix and classification report provide a detailed breakdown of the model's performance. It exhibits a strong ability to correctly classify instances, particularly for the **False** class. 
- However, there's some room for improvement in terms of recall for the **True** class.

- Generalization and Stability:

The cross-validation scores indicate that the model's performance is consistent across different subsets of the dataset, suggesting good generalization and stability. This is an important characteristic for a reliable machine learning model.

- Future Improvements:

While the model's performance is strong, there is an opportunity to further enhance its precision and recall, particularly for the **True** class. - - This can be achieved through feature engineering, hyperparameter tuning, or exploring more advanced machine learning algorithms.


- Robust Evaluation:

The use of cross-validation ensures that the model's performance is not overfitted to the specific dataset, making the evaluation robust and reliable.

## Machine Learning 
- This repository contains machine learning algorithm for customer churn prediction implimented by jupyter notebook and Python
## Algorithma used:
- XGBoot Classifier
