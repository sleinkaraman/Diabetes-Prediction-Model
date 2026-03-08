# 📊 Diabetes Prediction Model

This project aims to develop a machine learning model to predict whether individuals have diabetes using a dataset from a diabetes study conducted on Pima Indian women. Before training the model, a comprehensive data analysis and feature engineering process was carried out.

## 📁 About the Dataset

The dataset was collected by the National Institute of Diabetes and Digestive and Kidney Diseases in the United States. It contains information about Pima Indian women aged 21 and older living in Phoenix, Arizona.

- **Total Number of Observations**: 768  
- **Independent Variables**: 8  
- **Target Variable**: `Outcome` (1: Diabetes Positive, 0: Negative)

### 🔍 Variables

| Variable                  | Description                                                              |
|---------------------------|--------------------------------------------------------------------------|
| `Pregnancies`             | Number of pregnancies                                                    |
| `Glucose`                 | Glucose level                                                            |
| `BloodPressure`           | Blood pressure (Diastolic)                                               |
| `SkinThickness`           | Skin thickness                                                           |
| `Insulin`                 | Insulin level                                                            |
| `BMI`                     | Body mass index                                                          | 
| `DiabetesPedigreeFunction`| Likelihood of diabetes based on family history                           |
| `Age`                     | Age                                                                      |
| `Outcome`                 | Target variable – Diabetes diagnosis (1: Positive, 0: Negative)          |


## 🛠 Technologies and Libraries Used

The main technologies and libraries used in this project include:

- **Python**: The primary programming language used for data analysis, modeling, and visualization.

- **pandas**: Used to load, clean, and transform the dataset. Its `DataFrame` structure allows efficient data manipulation and analysis.

- **numpy**: Used for mathematical computations, particularly for processing numerical features in the dataset. It enables fast and efficient numerical operations required for model training.

- **matplotlib** ve **seaborn**: Used for data visualization. `matplotlib` was used to create basic plots, while `seaborn` was preferred for more aesthetic and informative visualizations such as distribution plots and heatmaps.

- **scikit-learn**: Used for machine learning modeling. During the model training and evaluation process, particularly:
  - **RandomForestClassifier**: DUsed to build the diabetes prediction model by combining multiple decision trees to create a strong classification model.
  - **StandardScaler**: Used to standardize numerical features so that variables with different scales can be learned more effectively by the model.
  - **LabelEncoder**: Used to convert categorical variables into numerical values so the model can process them properly.


## 📌 Project Steps

### 1. KExploratory Data Analysis (EDA)

- The structure of the dataset was examined.
- Variable types were identified (numerical & categorical).
- Distributions, outliers, and missing values were analyzed.
- Relationships with the target variable (`Outcome`) were investigated.
  
### 2. Data Preprocessing

- Distinctive missing values were identified and properly transformed.
- The impact of outliers was analyzed.
- Numerical variables were standardized using `StandardScaler`.

### 3. Feature Engineering

- New variables were created (for example, age and BMI groups).
- Interactions between variables such as `Pregnancies`, `Age` and `Glucose` were examined.
- Categorical transformations and feature encoding were applied when necessary.

### 4. Modeling and Evaluation

- The `RandomForestClassifier` algorithm was used.
- The dataset was split using `train_test_split` and the model was trained.
- Performance metrics: Accuracy, Precision, Recall, F1 Score, ROC-AUC.
- The model’s accuracy and generalization capability were evaluated.

