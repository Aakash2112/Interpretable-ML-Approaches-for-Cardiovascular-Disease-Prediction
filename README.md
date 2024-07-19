# Interpretable-ML-Approaches-for-Cardiovascular-Disease-Prediction
This repository aims to predict which patient is more prone to cardiovascular diseases using different machine learning algorithms, ensemble methods and neural networks while also interpreting these models using techniques such as SHAP, Permutation Importance and Lime to find out which features have the most importance in the model’s predictions.

---
#Pre-Processing#
---
In the study, plenty of pre-processing steps are carried out on dataset, based on the EDA performed. During the data exploration, Oldpeak and RestingBP was found to exhibit right skewed data distribution, thus the RobustScaler was used for the normalization process since the features contains non positive values. Rest of the numerical features like Age, Cholesterol, MaxHR was found to be normally distributed, hence StandardScaler was utilized to scale down and standardize the data. The categorical features of the dataset were also preprocessed using the Label Encoder and standardized since they were normally or continuously distributed. The manual splitting of the dataset was also done to ensure that the model was trained and evaluated on a diverse set of data. For this paper, 70% of the data was used for training purposes and the rest 30% was used for testing in the both the approaches done.

![image](https://github.com/user-attachments/assets/9d84b196-a9ce-4aed-81d0-bf730a0d010a)
