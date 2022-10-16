# Credit_Risk_Analysis

## Overview

The objective of this assignment was to use Supervised Machine Learning to help
solve a real-world challenge: determine credit card risk. Many different sampling
methods as well as predictive models were used to analysis credit risk

## Results

Using Random Oversampling, the Confusion Matrix shows that this method is bad at predicting high risk, but good at predicting low risk. This method had a balanced accuracy score of 0.655.

![ROS_CM](https://user-images.githubusercontent.com/106849689/196012429-a6c5b0ae-038c-47b8-ae4a-ee6549a8594a.png)

SMOTE Oversampling performs similar to Random Oversampling. Where it only predicts true 64 actually true (i.e. low risk) samples and predicts false 11,818 actually false (i.e. high risk) samples. This method has a balanced accuracy score of 0.662.

![SMOTE_CM](https://user-images.githubusercontent.com/106849689/196012434-27e1fd7b-d09e-4709-b4fb-a7deeb5b3136.png)

The Cluster Centroids Undersampling method was not much better than the oversampling methods. It only predicted 70 low risk items
correctly. But it predicted 6,764 high risk items correctly. The balanced accuracy score was, again, similar to the oversampling
methods: 0.662.

![CC_CM](https://user-images.githubusercontent.com/106849689/196012443-b327b36e-22e2-48d8-98e4-d001df4ba8e8.png)

The combination method of SMOTEENN was even worse than using these over/undersampling methods individually. It has a balanced
accuracy score of 0.544. It also only predicted 73 low risk samples correctly, and 9,694 high risk items correctly.

![SMOTEENN_CM](https://user-images.githubusercontent.com/106849689/196012451-a159ed37-8bb0-42bf-80c1-88bda57e9b2f.png)

Using the Ensemble method Balanced Random Forest Classifier, we can see that the balanced accuracy score is 0.362, much worse
than that of any of the over/undersampling methods. Its confusion matrix shows that it predicts less true positives than false positives; and more false negatives than true negatives. This is not good.

![BRFC_CM](https://user-images.githubusercontent.com/106849689/196012462-1c9a3cc2-3f5d-4c14-88f4-57f17488b7df.png)

The Easy Ensemble AdaBoost Classifier, on the other hand, has an amazing balanced accuracy score of 0.832. Its confusion matrix 
shows 106 true positives and 102 true negatives as compared to 21 false positives and 21 false negatives.

![EEAB_CM](https://user-images.githubusercontent.com/106849689/196012468-109e693a-e3d2-41ce-b0c9-aa8c1b00ec92.png)

The imbalanced classification report also supports that fact that this method is a good one. This report shows both a precision
and a recall of 0.83.

![EEAB_ICR](https://user-images.githubusercontent.com/106849689/196012472-decf7720-6cd5-4fb1-a84e-2764035264c7.png)

## Summary

Comparing all six of these methods, it is apparent that the Easy Ensemble AdaBoost Classifier method is the clear winner.
