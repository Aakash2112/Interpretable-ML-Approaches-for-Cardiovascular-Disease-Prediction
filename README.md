# Interpretable-ML-Approaches-for-Cardiovascular-Disease-Prediction
This repository aims to predict which patient is more prone to cardiovascular diseases using different machine learning algorithms, ensemble methods and neural networks while also interpreting these models using techniques such as SHAP, Permutation Importance and Lime to find out which features have the most importance in the model’s predictions.

---
Pre-Processing
---
In the study, plenty of pre-processing steps are carried out on dataset(refer below diagram), based on the EDA performed. During the data exploration, Oldpeak and RestingBP was found to exhibit right skewed data distribution, thus the RobustScaler was used for the normalization process since the features contains non positive values. Rest of the numerical features like Age, Cholesterol, MaxHR was found to be normally distributed, hence StandardScaler was utilized to scale down and standardize the data. The categorical features of the dataset were also preprocessed using the Label Encoder and standardized since they were normally or continuously distributed. The manual splitting of the dataset was also done to ensure that the model was trained and evaluated on a diverse set of data. For this paper, 70% of the data was used for training purposes and the rest 30% was used for testing in the both the approaches done.

![image](https://github.com/user-attachments/assets/9d84b196-a9ce-4aed-81d0-bf730a0d010a)

---
Methodology
---
In the correlation matrix (Refer Below Diagram), it was found that Resting ECG and Resting BP were the two least (Including Positive and Negative Relationships) correlated features with values of 0.057 and 0.11. Hence, we decided to split the models into two types to simplify them and analyze the performance. In model 1, to verify the features being removed, further tests were conducted. The Anova test conducted to check how each numerical feature impacts the response variable and the Chi squared test conducted to check how each categorical feature are associated with target variable. Resting Bp and Resting ECG were removed during the training along with the target variable. In model 2, no features were removed and the data was trained as per the pre-processing done. For the sake of simplicity, the two different approaches will be addressed as model 1 and model 2 in the subsequent columns. The purpose of this was to observe the changes in our model's prediction rate during different scenarios and to see which method provides the best results.

![image](https://github.com/user-attachments/assets/e7466b4d-6f0f-4aa8-b462-cadd6d914e71)

---
Interpretable Models
---
The proposed approach in this study extends to also include the interpretation framework tools such Shapely added explanations (SHAP), Permutation Importance and Local Interpretable Model Agnostic Explanation (LIME) which is used for interpreting the three different machine learning models used in this paper. The predictions made by a model must be explained especially in this healthcare sector to help the patients as well as the physicians to decide whether an individual is likely to have a risk of attaining cardiovascular disease. Finding the characteristics or factors that affect predictions the most significantly can help in accomplishing this goal. These interpretations by the tools can offer explanations and insights into the predictions or choices the model makes.

![image](https://github.com/user-attachments/assets/56eb0405-3936-46d1-a1e1-2e3ba08897d4)

---
Future Works
---
The repository highlights the pertinence of SHAP, LIME and Permutation Importance methods for comprehending and interpreting the model’s predictions to pave the way for easier data driven decision by the experts. In the future, we explore the possibility of integrating these techniques and the interpretations into clinical practices to improve patient outcomes and aid in early detection of the cardiovascular diseases. We can also try to implement different hyperparameter tuning methods to see if the model responds well to the other methods as well compared to the Grid Search Cv
