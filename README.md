# credit-risk-classification

Machine learning methods are employed to examine a historical lending activity dataset obtained from a peer-to-peer lending company, with the aim of constructing a model capable of assessing the creditworthiness of borrowers.

# More about the analysis

Machine Learning Techniques: Refers to the use of advanced algorithms and statistical models to make predictions or decisions without being explicitly programmed. In this context, machine learning is a technology or methodology being used.

Analyze a Dataset: Means that the data collected from historical lending activities is being examined and processed. This could involve various data manipulation and analysis techniques to extract meaningful insights.

Historical Lending Activity: Refers to the past records of loans being issued or borrowed from the peer-to-peer lending service. This data likely includes information about who borrowed, how much, when, and what happened with those loans.


# Overview of the Analysis

Factors in the analysis included data on:

- the size of the loan as *loan_size*
- its interest rate as *interest_rate*
- the borrower's income as *borrower_income*
- the debt to income ratio as *debt_to_income*
- the number of accounts the borrower held as *num_of_accounts*
- derogatory marks against the borrower as *derogatory_marks*
- the total debt as *total_debt*

The dataset, consisting of 77,536 data points, underwent a division into training and testing subsets. The training subset served as the foundation for constructing an initial logistic regression model referred to as Logistic Regression Model 1, which was implemented using the LogisticRegression module from scikit-learn. Subsequently, Logistic Regression Model 1 was applied to the testing dataset with the goal of discerning whether loans to borrowers in the testing set were of low or high risk. The outcomes of this analysis are presented below.

Initially, this model drew upon a dataset comprising 75,036 instances of low-risk loans and 2,500 instances of high-risk loans. To ensure that the logistic regression model had an equivalent number of instances to draw from during training, the training data was subjected to resampling using the RandomOverSampler module from imbalanced-learn. This resampling process resulted in the creation of 56,277 instances each for low-risk (0) and high-risk (1) loans, aligning with the original dataset.

The resampled data was then utilized for constructing a new logistic regression model, referred to as Logistic Regression Model 2. The primary objective of Logistic Regression Model 2 remained the same: to ascertain whether loans to borrowers in the testing set were categorized as low or high risk. The findings from this analysis are summarized below.


# Findings

Logistic Regression Model 1:
- Precision: 93% 
- Accuracy: 94%
- Recall: 95%

Logistic Regression Model 2:
- Precision: 93% 
- Accuracy: 100%
- Recall: 100%

# Findings Summary and Recommendation
Logistic Regression Model 2 exhibits a reduced tendency to make incorrect negative predictions. Nevertheless, when examining the confusion matrices for both models, it becomes evident that Logistic Regression Model 2 made slightly more erroneous positive predictions, specifically classifying instances as low-risk when they were actually high-risk.

When the objective is to gauge the probability of high-risk loans, neither model achieves a precision rate exceeding 90%. In the context of overall prediction accuracy and recall for the testing data, Logistic Regression Model 2 outperforms by making fewer false predictions, making it the preferable model to use.
