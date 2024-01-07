# Overview
In this guide, we will explore various methods for imputing continuous numerical variables and illustrate the outcomes of each technique. Our focus will be on basic imputation approaches like mean and median imputation, as well as more complex strategies like K-nearest neighbors (KNN).

# About the Dataset
This dataset is originally from the National Institute of Diabetes and Digestive and Kidney Diseases. The objective of the dataset is to diagnostically predict whether a patient has diabetes, based on certain diagnostic measurements included in the dataset. Several constraints were placed on the selection of these instances from a larger database. All patients here are females at least 21 years old of Pima Indian heritage. Variables in the dataset include number of pregnancies, glucose, blood pressure, skin thickness, insulin, BMI, age, etc..

For a comprehensive exploratory analysis of the data, check out the **df_profile.html** file attached. 

# Variable to Impute
In our dataset, the primary variable we'll concentrate on for imputation is 'Insulin,' which quantifies the 2-hour serum insulin level in micro-units per milliliter (mu U/ml) and has 48% missing values.

# Summary of Results
In our examination of the dataset, we specifically looked to address the missing values in the 'Insulin' variable, which represents the 2-hour serum insulin levels. We employed two distinct imputation methods: simple imputation (utilizing mean and median values) and advanced imputation (leveraging KNN or K-nearest neighbors).

Initially, we assessed the impact of straightforward approaches like removing missing data or replacing them with central tendency measures—mean and median. Although quick and easy, these simple imputation methods introduced notable biases, particularly when the 'Insulin' variable had a significant amount of missing data. Such replacements can skew the variable's original distribution and adversely affect its correlation with other variables in the dataset.

Shifting to advanced imputation, we implemented the KNN method, which computes the missing value based on the most similar instances in the dataset. By using KNN, we integrated other variables from the dataset into our imputation process. By doing so, we found that addressing the missing values in the context of the entire dataset—considering the interdependencies among all variables—yielded a more precise and less biased imputation. This technique preserves the underlying structure and relationships within the data more effectively than simple mean or median replacements. The KNN approach produced a distribution for 'Insulin' that closely resembled its original, complete dataset distribution, with a reduced bias and a more realistic representation of the variable's relationship with other features.

In essence, while simple imputation methods are easy to implement, they often fall short in preserving the true characteristics of the data, especially in cases of extensive missingness. In contrast, advanced methods like KNN, though computationally heavier, provide a more sophisticated solution by utilizing the broader data context, which in turn results in a more accurate and reliable imputation.






