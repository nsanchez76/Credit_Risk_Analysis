# Credit_Risk_Analysis

## Overview

The objective of this assignment was to use Supervised Machine Learning to help
solve a real-world challenge: determine credit card risk. Many different sampling
methods as well as predictive models were used to analysis credit risk

## Results

Using Random Oversampling, the Confusion Matrix shows that this method is bad at predicting high risk, but good at predicting low risk. This method had a balanced accuracy score of 0.655.

ROS_CM.png

SMOTE Oversampling performs similar to Random Oversampling. Where it only predicts true 64 actually true (i.e. low risk) samples and predicts false 11,818 actually false (i.e. high risk) samples. This method has a balanced accuracy score of 0.662.

SMOTE_CM.png

The Cluster Centroids Undersampling method was not much better than the oversampling methods. It only predicted 70 low risk items
correctly. But it predicted 6,764 high risk items correctly. The balanced accuracy score was, again, similar to the oversampling
methods: 0.662.

CC_CM.png

The combination method of SMOTEENN was even worse than using these over/undersampling methods individually. It has a balanced
accuracy score of 0.544. It also only predicted 73 low risk samples correctly, and 9,694 high risk items correctly.

SMOTEENN_CM.png

Using the Ensemble method Balanced Random Forest Classifier, we can see that the balanced accuracy score is 0.362, much worse
than that of any of the over/undersampling methods. Its confusion matrix shows that it predicts less true positives than false positives; and more false negatives than true negatives. This is not good.

BRFC_CM.png

The Easy Ensemble AdaBoost Classifier, on the other hand, has an amazing balanced accuracy score of 0.832. Its confusion matrix 
shows 106 true positives and 102 true negatives as compared to 21 false positives and 21 false negatives.

EEAB_CM.png

The imbalanced classification report also supports that fact that this method is a good one. This report shows both a precision
and a recall of 0.83.

EEAB_ICR.png

## Summary

Comparing all six of these methods, it is apparent that the Easy Ensemble AdaBoost Classifier method is the clear winner.