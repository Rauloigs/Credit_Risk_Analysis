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



Now, here you can see two *Imbalanced Classification Reports* in the programming I did. Under the **Summary** you will find the results explanation: 


**SMOTEEEN** | *Combination Undersampling and Oversampling*

<img width="658" alt="smoteenn" src="https://user-images.githubusercontent.com/84519822/166726594-76581465-4113-43f3-9953-f4ab5e1b3ca2.png">



**Easy Ensemble** | *Combination Undersampling and Oversampling*

<img width="433" alt="easyensemble" src="https://user-images.githubusercontent.com/84519822/166726632-57d91e47-741c-48f6-8bab-e429b30ba71d.png">


*If you like to go to the programming files to take look of the complete results go [here](https://github.com/Rauloigs/Credit_Risk_Analysis)*


## Summary:

We will start by evaluating the first 4 models of the table above. As you may realized, the resampling models (first 4 in the table) perform pretty similar regarding the three variables exposed (accuracy, precision & recall). 

- The accuracy of those 4 models goes from *0.54* to *0.66* which might not be a bad value, nevertheless it doesn´t tell us much so we will review the performance of the model in precision and sensitivity. 
- The precision of those 4 was *0.01* which tells us: If there is a high risk how possible is it that it is indeed a high risk. There are low chances that even if the result is *high risk* the result is *high risk*.
- The recall was better for SMOTEENN and Oversampling with *0.72*. so from those low risk evaluations we know *72%* may be actually correctly judged. 
- The F1 values are also not remarkably good for low risk thay are maximum *0.72* among the four models which is not bad, and for high risk below 0.1.

Finally lets go over the last two models, the **Ensemble Learners**. 

- They both show an accuracy above *0.99*, which is way better than the resampling models, but the main difference between the ensemble models is in the precision and the recall. 
- The precision is better in the Random Forest than in the Easy Ensemble but in the recall outputs the Easy Ensemble is better (take a glance at the table). This is telling us the following: The Easy Ensemble tells us that of those high risk detected, *36%* of them will be judged correctly. Random Forest, means that if it is a high risk detected, there's a *95%* of chances that the output is high risk.

The recommendation for which model to use in this case is a Random Forest, because of its higher precision obove the other models and the best F1 results  0.52 high risk and 1.0 low risk.
