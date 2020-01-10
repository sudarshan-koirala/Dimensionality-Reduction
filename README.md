# Dimensionality-Reduction

Using Principal Component Analysis (PCA) and Linear Discriminant Analysis (LDA) on same dataset and analyzing the best one. Both PCA and LDA are the feature extraction model.

- PCA extracts p ≤ m new independent variables from m independent variables that explains the most variance of the dataset regardless of the dependent variable (unsupervised model)

- LDA extracts p ≤ m new independent variables from m independent variables that separate the most classes of dependent variable (supervised model)

## Business Problem

Which wine to recommend to which segment of customers ?

## Dataset

The Wine dataset consists 178 rows and 13 dependent variables which gives the different chemical components in one specific wine. The dependent variable consists 3 different clusters(1, 2, 3) of customers who preferred specific wines.
[Initial dataset link](https://archive.ics.uci.edu/ml/datasets/Wine). Modifications is done in the datasets present in this project.


## Solution

Logistic regression is used for this problem. As, the wine have 13 different features, dimensionality reduction is used to find 2 features that have the most variance.
The confusion matrix and the classification report after applying PCA is shown below.

![cm_pca](https://user-images.githubusercontent.com/14214659/71826377-742c8300-30a6-11ea-9b52-aca6d2b57e6f.png)

![pca_classification_report](https://user-images.githubusercontent.com/14214659/71826869-b0acae80-30a7-11ea-9c17-0d110aadc593.png)

Similarly, the confusion matrix and the classification report after applying LDA is shown below.

![cm_lda](https://user-images.githubusercontent.com/14214659/71826360-6545d080-30a6-11ea-94a8-91611e05265e.png)

![lda_classification_report](https://user-images.githubusercontent.com/14214659/71827113-33ce0480-30a8-11ea-8a96-5aecef217774.png)

It shows that the logistic regression classifies the data very accurately as it has 97% accuracy with PCA and 100% accuracy. Without any other parameter tuning, just with the above result it shows that LDA is best than PCA for this data.
