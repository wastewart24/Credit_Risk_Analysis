# Credit_Risk_Analysis

## Overview of Analysis
#### 
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. In this project, I employed different techniques to train and evaluate models with unbalanced classes. The client wanted to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

#### 
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, I oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then, I used a combinatorial approach of over and undersampling using the SMOTEENN algorithm. Next, I compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.

Lastly, I looked at the performance of these models and made a prediction if they are effective in assessing credit risk. 

## Results

### Oversampling
* Naive Random Oversampling
  * Accuracy Score - 0.6595
  * Imbalanced Classificaiton Report
  <img width="714" alt="Screen Shot 2023-02-03 at 10 33 15 PM" src="https://user-images.githubusercontent.com/43667985/216745967-ed901e97-4801-40f5-b278-932204c20890.png">
  
  
* SMOTE Oversampling
  * Accuracy Score - 0.6540
  * Imbalanced Classificaiton Report
  <img width="726" alt="Screen Shot 2023-02-03 at 10 33 41 PM" src="https://user-images.githubusercontent.com/43667985/216746063-8b0fb89c-3c7d-4921-b594-74d65d4c89c9.png">

  
### Undersampling
* ClusterCentroid Undersampling 
  * Accuracy Score - 0.5103
  * Imbalanced Classificaiton Report
  <img width="716" alt="Screen Shot 2023-02-03 at 10 33 49 PM" src="https://user-images.githubusercontent.com/43667985/216746068-6409d58e-c332-47b9-9140-235af08c63ba.png">

  
### Combined Over/Under Sampling
* SMOTEENN Sampling
  * Accuracy Score - 0.6375
  * Imbalanced Classificaiton Report
  <img width="709" alt="Screen Shot 2023-02-03 at 10 33 56 PM" src="https://user-images.githubusercontent.com/43667985/216746072-184d531c-c2e2-4cd8-ba59-5a7aa5b373c7.png">

  
### Ensemble Classification
* Balanced Random Forest Classifier
  * Accuracy Score - 0.9063
  * Imbalanced Classificaiton Report
  <img width="713" alt="Screen Shot 2023-02-03 at 10 34 08 PM" src="https://user-images.githubusercontent.com/43667985/216746075-a9e137bb-c35e-4eb1-a42d-2147ee49aab6.png">

  
* Easy Ensemble AdaBoost Classifier
  * Accuracy Score - 0.9426
  * Imbalanced Classificaiton Report
  <img width="717" alt="Screen Shot 2023-02-03 at 10 34 19 PM" src="https://user-images.githubusercontent.com/43667985/216746077-3beb5dc7-5f30-4f64-9d4f-05130b752e3f.png">

  

## Summary
####
The Ensemble classification models produced the highest accuracy scores that were both above 90%.  The precision is also at 99% for both models. Credit card companies would require machine learning models to be as accurate as possible, so they would most likely prefer the Easy Ensemble AdaBoost Classifier with an accuracy score of 94%. However, further optimization would need to be required for companies to trust the algorithm to run through millions of their customer's data.
