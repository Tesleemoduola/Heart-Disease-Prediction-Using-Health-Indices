# Heart Disease Prediction Using Health Indices

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset Overview](#dataset-overview)
- [Data Preprocessing](#data-preprocessing)
- [Model Building](#model-building)
- [Feature Importance](#feature-importance)
- [Model Evaluation](#model-evaluation)
- [Model Deployment](#model-deployment)


## Project Overview
Disease condition related with heart are some of the leading cause of morbidity and mortality. The purpose of this project was to develop an effective Machine Learning model 
to identify patient at risk of heart disease using some health indices and the patient's demography.. By applying advanced analytics and machine learning techniques to the 
provided dataset.

![Heart Picture](image_1.jpg)


## Dataset Overview
The dataset for this project contains features such as age, gender, chest pain type, resting blood pressure, cholestrol, and other features.
Below is ths Data Dictionary and screenshot of the dataset

- **Data Dictionary**
- age - age of the patient in years
- sex - (1= male; 0= female)
- cp - chest pain type (1= typical angina; 2= atypical angina; 3= non-anginal pain; 4= asymptomatic)
- trestbps - resting blood pressure (in mmHg)
- chol - serum cholesterol (in mg/dl)
- fbs - fasting blood sugar (value >120mg/dl)(1= true; 0= false)
- restecg - resting electrocardiogram (1= normal, 0= abnormal)
- thalach - maximum heart rate achieved (in beats/min)
- exang - exercise induced angina (1= yes; 0= no)
- oldpeak - ST depression induced by exercise relative to rest
- slope - the slope of the peak exercise ST segment (0= downsloping; 1= Flat; 2= upsloping)
- ca - number of major vessels (scored 0-3)
- thal - patient had thalassemia defect or not (1= normal; 2= fixed defect; 3= reversible defect)
- target - patient had the disease or not (1= yes; 0= no)

![Data Overview](image_3.jpg)


## Data Preprocessing
Data preprocessing was done to prepare the data for modelling
- **Handle missing values**: Ensured that all missing values in the dataset were properly addressed.
- **Remove duplicates**: Checked for duplicate values to avoid redundancy. 1 duplicate was found in the datasetand it was dropped
- **Scale numerical variables with outliers**: resting_blood_pressure, cholesterol, max_heart_rate_achieved, and thalassemia were scaled to ensure consistent scaling.


## Model Building
Eight machine learning classifiers:
- Logistic Regression
- SGD Classifier
- K-Nearest Neighbors (KNN)
- Random Forest Classifier
- Support Vector Machine (SVM)
- Naive Bayes
- Decision Tree 
- XGBoost were imported
The classifiers were trained on the training dataset, and evaluated on the test subset of the dataset.


## Feature Importance
The following table lists the importance scores of various features used in the model. Higher positive values indicate greater importance 
in the model's predictions, while negative values suggest a lesser contribution or inverse relationship.

![Feature Importance](image_5.jpg)

- **High Positive Scores**: Features like age, ST depression, and chest pain type are crucial for the model's predictions and should be prioritized in clinical settings.
- **Moderate Scores**: Number of major vessels and exercise-induced angina have a moderate impact and are important but not as critical as the top features.
- **Low or Negative Scores**: resting blood pressure, cholesterol, and fasting blood sugar have minimal impact on predictions and might be less significant for the model.

Overall, age, ST depression, and chest pain are the most influential, while resting blood pressure, cholesterol and fasting blood sugar have less impact or a negative influence.


## Model Evaluation
The performance of the models was evaluated on the test dataset using metrics such as accuracy, precision, recall, and F1-score.
Below is a screenshot of the evaluation reports and Naive bayes confusion matrix from the notebook:

![Evaluation Report](image_4.jpg)

![NB CM report](image_7.jpg)


## Model Deployment
The model was deployed using Streamlit

![Model Picture](image_8.jpg)
