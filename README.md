# Credit_Risk_Analysis

For this challenge, we are building models that will help us assess the financial risk associated with each customer. We are using data from LendingClub, but will have to rebalance the data with SciKit in order to build a model properly with data to test afterwards.

We will balance and implement the following models, and evaluate their effectiveness based on accuracy scores confusion matrices and overall classification reports.
• Oversample data using SMOTE
• Undersample data using Cluster Centroid algorithm
• Combination SMOTEENN

## Analysis
Naïve random oversampling
The accuracy score is .65 but the precision score for high risk scores is minimal at .01 compared to the much higher precision score for low risk. This indicates over fitting for the low risk scores.

SMOTE
![smote](/Resources/SMOTE.png)
The accuracy score is .63 and the model has similar issues as Naïve random oversampling, with slightly different recall scores that are still middling.

Undersampling
Similar issues with overfitting towards low risk, with an accuracy score of .63. Recall scores remain middling

SMOTEENN
Scores remain overfitted, and middling accuracy and recall scores.

Overall, no strong models with models that do not correctly identify high risk applicants. Additionally, accuracy and recall scores are average.

Random Forest
Incremental improvement to accuracy score (.73) and high risk precision at .03, but overall still not an effective model.

EasyEnsemble
Strong accuracy scores with high precision scores for both low risk and high risk scores (1.00 and .92). While recall score for high risk is middling at .47, the F1 score is .62. Overall, this is the strongest model.
