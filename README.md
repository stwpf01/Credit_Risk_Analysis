# Credit_Risk_Analysis

## Overview

The purpose of this analyis is to determine how successful various models are at assessing credit risk. This was tested through the use of Resampling, Over-,Under-, a combination of Over- and Undersampling, and two forms of Ensemble Classifiers. The full code for these various models can be found in the files named [credit_risk_resampling](https://github.com/stwpf01/Credit_Risk_Analysis/blob/main/credit_risk_resampling.ipynb) and [credit_risk_ensemble](https://github.com/stwpf01/Credit_Risk_Analysis/blob/main/credit_risk_ensemble.ipynb). Results using the various models and images of code are below.   


## Results

### Naive Oversampling

![naiveoversampling](https://github.com/stwpf01/Credit_Risk_Analysis/blob/main/Images/naiveoversampling.png)

- The accuracy score is 0.629. Converted to a percentage that is 62.9%. 62.9% is a poor accuracy score.
- The confusion matrix has more correct predicted values than incorrect predicted values, however the incorrect predicted values are too numerous to treat this model as reliable.
- The output of the confusion matrix is reflected in the precision and recall scores.


### SMOTE Oversampling

![smoteoversampling](https://github.com/stwpf01/Credit_Risk_Analysis/blob/main/Images/smoteoversampling.png)

 - Accuracy score is 0.627, or 62.7%. This means the SMOTE Oversampling model fares worse than the Naive Oversampling model.
 - The precision score remains the same, but the recall score is worse due to lower scoring in the `low_risk` category. 


### Undersampling

![undersampling](https://github.com/stwpf01/Credit_Risk_Analysis/blob/main/Images/undersampling.png)

 - Accuracy score is 0.529, or 52.9%. Undersampling is not better than either Naive Oversampling or SMOTE Oversampling.
 - Similar to the two previous models, the precision score is the same while the recall score suffers due to the `low_risk` category. Undersampling did not find many True Negatives.


### Over- and Undersampling Combination

![combination](https://github.com/stwpf01/Credit_Risk_Analysis/blob/main/Images/combination.png)

- Accuracy score is 0.641, or 64.1%. Combining the Over- and Undersampling models improved the accuracy, but still not significantly enough to use viably.
- Recall score improved for the `high_risk` category but not for the `low_risk` category. Recall score for `low_risk` was only better when compared to the Undersampling model. Precision score remained the same.

### BalancedRandomForest Classifier

![balancedrandomforest](https://github.com/stwpf01/Credit_Risk_Analysis/blob/main/Images/balancedrandomforest.png)

- Accuracy score is 0.787, or 78.7%. While greatly improved compared to the previous models, this model is still too unreliable to use to assess credit risk.
- The recall score improved dramatically for `low_risk` but worsened, when compared to the combination model, in the `high_risk` category. The precision score continues to be unchanged.


### EasyEnsemble Classifier

![easyensemble](https://github.com/stwpf01/Credit_Risk_Analysis/blob/main/Images/easyensemble.png)

- Accuracy score is 0.925, or 92.5%. The EasyEnsemble Classifier is the best performing model of the six.
- Like the accuracy score, the recall and precision scores are the best compared to any of the other models.


## Summary

 Of the six models made, the best model used to assess credit risk is the EasyEnsemble Classifier. It had the most True Positives and True Negatives and the least False Positives and False Negatives. That being said, unless a model was absolutely needed to be rolled out, I would be hestitant to use the EasyEnsemble Classifier as is. A    92.5% accuracy score is high, but a model for assessing something like credit risk should be more accurate. Until a model is made with an accuracy score of 96% or, ideally, higher, I wouldn't recommend any of them be used.   



