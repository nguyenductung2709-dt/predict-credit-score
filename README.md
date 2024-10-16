

# Predict Credit Score Using Machine Learning

## Goal
For a bank, classifying customers’ credit scores is essential for managing risks and making informed
loaning decisions. However, this process can often be multidimensional and complex, presenting
significant decision-making challenges. With the development of Machine Learning algorithms, automating credit score classification has become a viable solution to enhance accuracy and efficiency.
This Machine Learning project aims to create a categorical classification algorithm that utilizes supervised learning techniques on credit-related factors to classify customers’ credit scores into three classes:
good, standard, and poor.

## Datasets
The [Dataset for Credit Score Classification]([url](https://www.kaggle.com/datasets/ayushsharma0812/dataset-for-credit-score-classification/data?select=Credit_score_cleaned_data.csv)) from Kaggle contains basic bank details and credit related
information of 100,000 customers with 32 variables. Variables include age, occupation, annual income,
monthly inhand salary, number of bank accounts, etc.

## Method 1: Random Forest Classifier
![image](https://github.com/user-attachments/assets/a744b5f3-a77d-4564-a488-777a4f5bebc5)

With all metrics (accuracy, weighted precision, weighted recall, and
weighted F1-score) around 82% in the test result, Random Forest Classifier
demonstrates a more robust and consistent performance. Notably, it classified 83.62% of individuals with
bad credit correctly, outperforming that number for the good (78.18%) and standard (82.57%) credit
categories. This demonstrates the model’s effectiveness in identifying high-risk clients, which is crucial
for minimizing potential losses. It also has very few severe misclassifications, with only 0.38% instances
of ”Poor” being classified as ”Good” and 0.28% instances of ”Good” being classified as ”Poor”.

## Method 1: Logistic Regression
![image](https://github.com/user-attachments/assets/8f3c760e-768f-4ff6-a733-91c1cc267f4f)

All metrics of the model remain below
70%, indicating that there is significant room for improvement. While it correctly classifies 84.86% of
individuals with good credit, it only manages to classify 66.79% of individuals with bad credit correctly.
Additionally, the model misclassifies 15.34% of individuals with bad credit as having good credit. For a
bank or financial organization, this suggests that the model is insufficient for reliable risk assessment.

## Comparison
Looking at the average metrics of the two models, it is clear that the Random Forest Classifier outperforms Logistic Regression in all 4 metrics. This indicates the overall efficiency of the Random Forest
model in handling the classification task, making it a more robust choice. However, there is one aspect
in which Logistic Regression performed better than Random Forest Classifier, which is identifying individual with good credit score correctly. While Random Forest Classifier can identify 78.18% of good
credit individuals, that number of Logistic Regression is 84.85%, significantly higher.

After evaluating all these factors, we chose the Random Forest Classifier as our final machine learning
method due to its superiority in overall performance compared to Logistic Regression, achieving a final
test accuracy of 82%.

## Acknowledgement
This is a pair project that was done with the instruction of the professor and teaching assistants of the course _CS-C3240 - Machine Learning D_ at Aalto University.

Other contributor: [Tung Nguyen]([url](https://github.com/nguyenductung2709-dt))
