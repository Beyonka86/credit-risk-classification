# credit-risk-classification
Module 20 Asignment: Supervised Machine Learning

# Libraries used
* numpy
* pandas
* pathlib
* sklearn.metrics

# Introduction
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

# Split the Data into Training and Testing Sets
Open the starter code notebook and use it to complete the following steps:

Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.

# Displaying df_lending head of DataFrame

![Screenshot 2024-05-15 112409](https://github.com/Beyonka86/credit-risk-classification/assets/111611012/24c7e349-9d73-4a7a-b91f-8890698973e8)

# Diplaying df_lending tail of DataFrame

![Screenshot 2024-05-15 112523](https://github.com/Beyonka86/credit-risk-classification/assets/111611012/bab92fe9-4981-4075-a59a-760dcd0aaab5)


Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.

# Review of y variable Series

# y variable head

![Screenshot 2024-05-15 114048](https://github.com/Beyonka86/credit-risk-classification/assets/111611012/79ff61c1-30a8-4e40-b5c9-c59c9eefd06d)

# y variable tail

![Screenshot 2024-05-15 114058](https://github.com/Beyonka86/credit-risk-classification/assets/111611012/456b8341-37df-4751-ab8e-190bb326a160)


# Review of X variable DataFrame

X variable head
![Screenshot 2024-05-15 114109](https://github.com/Beyonka86/credit-risk-classification/assets/111611012/0f94b8ef-38cc-4414-9137-b4080b9cfe3a)

X variable tail

![Screenshot 2024-05-15 114124](https://github.com/Beyonka86/credit-risk-classification/assets/111611012/d59838b1-40c9-4bb3-9948-96176d04bcd1)

Split the data into training and testing datasets by using train_test_split.

# Classification report for the model

![Screenshot 2024-05-15 112914](https://github.com/Beyonka86/credit-risk-classification/assets/111611012/e3738c9f-06f2-433a-b13e-f476cc8287ca)

# Analysis of Precision Model

**Question:** How well does the logistic regression model predict both the `0` (healthy loan) and `1` (high-risk loan) labels?

**Answer:** Precision, measures the accutacy of positive predictions, that shows 0 (healthy loan) is 1.00 indicating that almost all predictions are correct. For 1 (high-risk loan), precision is 0.85 which indicates 85% of the instances predicted as 1 (high-risk loan) are actually 1 (high-risk loan).

Recall, measures the ability of the model to correctly identify positive instance, that shows 0 (healthy loan) at 99% of actual instances are correctly classified and 1 (high-risk loan) at 91% are correctly classified.

F1-score, wis the harmonic mean of precision and recall, is 1.00 for 0 (healthy loan) and 0.88 for 1 (healthy loan). 0 (healthy loan) indicates an excellent balance between precision and recall and 1 (high-risk loan) indicates reasonably good balance between precision and recall.

Support, is the number of actual occurrances of each class in the test dataset. 0 (healthy loan) has a support of 18765 which indicates a large number of instances and 1 (high-risk loan) has a support of 619 which indicates a relative smaller number of instances.

Accurary, measures the overall correctness of the model across all classes, which is 0.99 shows that this model is highly accurate in its predictions.

Summary: With this prediction model, 0 (healthy loan) seems to perform better overall due to the F1-scores. This conclusion is supported by a higher F1-scores which indicates a better balance between precision and recall for 0 (healthy loan) compared to 1 (high-risk loan).

Performance depends on correctly predicting the minority class which is 1 (high-risk loan) might be more crucial. This will help to focus on optimizing recall or F1-score for this minority class to miniimize false negative (missed detections).



