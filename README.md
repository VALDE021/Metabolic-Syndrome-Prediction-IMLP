# Metabolic Syndrome Prediction IMLP
Authored by: Eric N. Valdez
 
## Assignment:
My task here was to predict metabolic syndrome based on common risk factors. I used the dataset [Metabolic Syndrome Prediction - dataset by informatics-edu](https://data.world/informatics-edu/metabolic-syndrome-prediction), which came from the data.world.

## Permutation Importance

Started looking at the Plotting the Permutation Importance

![Permutation Importance](https://github.com/VALDE021/Metabolic-Syndrome-Prediction-IMLP/assets/134979886/5ad851d3-ffb6-4ff8-8112-e227cc6599b8)


Looked closer at Blood Glucose(blood shugar/source of energy) and HDL(cholesterol)

![Comparison of Blood Glucose and HDL by Metabolic Syndrome](https://github.com/VALDE021/Metabolic-Syndrome-Prediction-IMLP/assets/134979886/869c0215-807c-46ed-80c7-c18aa4f26807)

Taking a closer look you can see Blood Glucose is high and should be below 100 mg anything above starts you as prediabetica and can lead to metabolism syndrome, when you look at the HDL, you will see that its below 40 mg which is normal.

## Feature Engineering

Two methods of feature engineering were chosen. First I used Principal Component Analysis (PCA) to reduce the number of features. Then procceded with a forward selection wrapper to narrow down the features to 10.

## Neural Networks 

Created a sequential neural network model. Manually adjusting several iterations, most often attacking variance to increase the model accuracy. Utilizing Keras Tuner and Reducing Neurons to compare the models

## Models
Created several Models Using:
- KNN
- Smote
- KNN w/PCA to help trasform my features
- KNN w/Filter: this included the selection wrapper
- Neural Networks
- Keras Tuned Neural Networks

KNN
 Classification Metrics: Test Data
----------------------------------------------------------------------
              precision    recall  f1-score   support

           0       0.79      0.87      0.83       397
           1       0.69      0.56      0.62       204

    accuracy                           0.77       601
   macro avg       0.74      0.72      0.72       601
weighted avg       0.76      0.77      0.76       601


Smote
 Classification Metrics: Test Data
----------------------------------------------------------------------
              precision    recall  f1-score   support

           0       0.86      0.89      0.87       397
           1       0.76      0.72      0.74       204

    accuracy                           0.83       601
   macro avg       0.81      0.80      0.81       601
weighted avg       0.83      0.83      0.83       601

Smote with Wrapper
 Classification Metrics: Test Data
----------------------------------------------------------------------
              precision    recall  f1-score   support

           0       0.93      0.89      0.91       397
           1       0.80      0.86      0.83       204

    accuracy                           0.88       601
   macro avg       0.86      0.88      0.87       601
weighted avg       0.88      0.88      0.88       601

**KNN w/PCA**
Class Model-1 Test 

              precision    recall  f1-score   support

           0       0.86      0.91      0.89       397
           1       0.80      0.72      0.76       204

    accuracy                           0.85       601
   macro avg       0.83      0.81      0.82       601
weighted avg       0.84      0.85      0.84       601

**Keras Tuner**
Class Model-2 Test 

              precision    recall  f1-score   support

           0       0.88      0.90      0.89       397
           1       0.79      0.75      0.77       204

    accuracy                           0.85       601
   macro avg       0.83      0.82      0.83       601
weighted avg       0.85      0.85      0.85       601


**Reducing Neurons**
Class Model-3 Test 

              precision    recall  f1-score   support

           0       0.87      0.89      0.88       397
           1       0.78      0.74      0.76       204

    accuracy                           0.84       601
   macro avg       0.82      0.82      0.82       601
weighted avg       0.84      0.84      0.84       601


**RMSPROP Optimizer**
Class Model-4 Test 

              precision    recall  f1-score   support

           0       0.87      0.89      0.88       397
           1       0.78      0.74      0.76       204

    accuracy                           0.84       601
   macro avg       0.83      0.82      0.82       601
weighted avg       0.84      0.84      0.84       601

## Out of Models this was the result
<u>Precision	Recall	F1 Score	Accuracy</u>

***Model Name***				

Class Model-1 Train	0.861831	0.807443	0.833751	0.889444

**Class Model-1 Test	0.803279	0.720588	0.759690	0.845258**

Class Model-2 Train	0.855670	0.805825	0.830000	0.886667

**Class Model-2 Test	0.792746	0.750000	0.770781	0.848586**

Class Model-3 Train	0.839527	0.804207	0.821488	0.880000

**Class Model-3 Test	0.778351	0.740196	0.758794	0.840266**

Class Model-4 Train	0.849573	0.804207	0.826268	0.883889

**Class Model-4 Test	0.782383	0.740196	0.760705	0.841930**
