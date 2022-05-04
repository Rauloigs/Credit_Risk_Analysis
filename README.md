# Credit_Risk_Analysis

## Overview of the loan prediction risk analysis:

For this challenge I was required to employ different techniques to train and evaluate models with unbalanced classes. You will see the imbalanced-learn and scikit-learn libraries to build and evaluate those models using resample. The evaluation will be about **credit risk**, where it is an unbalanced classification problem, due that good loans outnumber risky loans. 


I will start by oversampling the data with the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, I’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. I will also compare two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. At the end, I’ll evaluate the performance of these models and make a conclusion on whether they should be used to predict credit risk.

## Results:

To provide a better overview of the models' results I'm providing a table where you can observe results for each Machine Learning model of: 

- Balance Accuracy Score 
- Precision
- Recall


| ML Model | Balance Accuracy Score | Precision | Recall |
| ------------- | ------------- | ------------- | ------------- |
| Random Oversampling  | 0.65473  | 0.01 | 0.72 |
| SMOTE Oversampling  | 0.66201  | 0.01 | 0.63 |
| Cluster Centroids Undersampling | 0.54473 | 0.01 | 0.69 |
| SMOTEENN Combination | 0.66657 | 0.01 | 0.72 |
| Random Forest C. | 0.99610 | 0.95 | 0.36 |
| Easy Ensemble C. | 0.94228 | 0.09 | 0.92 |


Now, here you can see two *Imbalanced Classification Reports* in the programming i did. Under the **Summary** you will find the results explanation: 


**SMOTEEEN** | *Combination Undersampling and Oversampling*

<img width="658" alt="smoteenn" src="https://user-images.githubusercontent.com/84519822/166726594-76581465-4113-43f3-9953-f4ab5e1b3ca2.png">



**Easy Ensemble** | *Combination Undersampling and Oversampling*

<img width="433" alt="easyensemble" src="https://user-images.githubusercontent.com/84519822/166726632-57d91e47-741c-48f6-8bab-e429b30ba71d.png">


*If you like to go to the programming files to take look of the complete results go [here](https://github.com/Rauloigs/Credit_Risk_Analysis)*


## Summary:

There is a summary of the results (2 pt)
There is a recommendation on which model to use, or there is no recommendation with a justification (3 pt)
