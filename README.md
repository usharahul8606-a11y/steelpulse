
Machine learning project for analysing steel production data and predicting production output using regression models.
### **SteelPulse: Understanding and Predicting Steel Production Through Machine Learning*  
 


## Author Information

| Field | Details |
|---|---|
| Author | Usha Rahul |
| Date | November 12, 2026 |
| University | Montanuniversität Leoben |
| Programme | MSc Industrial Data Science |
| Course | Applied Machine and Deep Learning |
| Domain | Machine Learning |
| Project Type | Individual Project |
| Semester | Winter Semester 2026/2027 |
| Project Title | SteelPulse: Understanding and Predicting Steel Production Through Machine Learning |
| Supervisor / Professor | Linus Nwankwo |

## 📑 Table of Contents

1. 🌟 [Project Overview](#project-overview)
2. 🎯 [Motivation and Objectives](#motivation-and-objectives)
3. 📚 [Related Work](#related-work)
4. 📊 [Dataset Description](#dataset-description)
5. 🔍 [Data Exploration and Analysis](#data-exploration-and-analysis)
6. 🛠️ [Data Preprocessing](#data-preprocessing)
7. 🤖 [Machine Learning Models](#machine-learning-models)
8. ⚙️ [Model Training and Hyperparameter Tuning](#model-training-and-hyperparameter-tuning)
9. 📈 [Model Evaluation and Comparison](#model-evaluation-and-comparison)
10. 🧪 [Data Augmentation](#data-augmentation)
11. 📉 [Influence of Training Data Size](#influence-of-training-data-size)
12. 🏆 [Key Findings and Discussion](#key-findings-and-discussion)
13. 🚀 [Future Work](#future-work)
14. 🧰 [Technologies Used](#technologies-used)
15. 👩‍💻 [Author Information](#author-information)
16. 📖 [References](#references)

---

# 🌟 SteelPulse: Understanding and Predicting Steel Production Through Machine Learning

## 1. Project Overview

SteelPulse is an individual machine learning project developed as part of the Applied Machine and Deep Learning course at Montanuniversität Leoben.

The project focuses on analysing steel-production data and developing machine learning models to predict a continuous target variable using numerical process-related input features.

The dataset contains 21 numerical input features (`input1` to `input21`) and one target variable (`output`). Different regression algorithms are investigated to understand their predictive performance and ability to generalise to unseen data.

The project includes data exploration, statistical analysis, preprocessing, model development, hyperparameter tuning, model evaluation, data augmentation, and training-size experiments.

The main aim is to investigate the potential and limitations of machine learning techniques for predicting steel-production output.

## 2. 🎯 Motivation and Objectives

### Motivation

Steel manufacturing involves complex production processes influenced by several parameters. Understanding the relationships between these parameters and production outcomes can help improve process analysis and support data-driven decision-making.

Machine learning provides methods for analysing historical production data, identifying patterns, and predicting continuous outcomes. Different algorithms can capture different types of relationships between input variables and target values.

This project explores how machine learning techniques can be applied to steel-production data while investigating challenges such as overfitting, data distribution differences, and model generalisation.

### Objectives

The main objectives of this project are:

- Explore and understand the available steel-production dataset.
- Perform statistical analysis and visualise the distributions of input features.
- Investigate correlations and relationships between input features and the target variable.
- Apply appropriate data preprocessing techniques.
- Develop multiple regression models.
- Perform hyperparameter tuning to investigate model improvements.
- Compare models using appropriate evaluation metrics.
- Investigate the effect of data augmentation on model performance.
- Evaluate how training dataset size influences predictive performance.
- Analyse model limitations and generalisation to unseen data.

---

## 🎯 2. Motivation and Objectives

### 💡 Motivation

Steel manufacturing involves complex production processes influenced by multiple parameters. Understanding the relationships between these parameters and production outcomes is important for analysing manufacturing performance and supporting data-driven decision-making.

Machine Learning (ML) provides powerful techniques for analysing historical production data, identifying hidden patterns, and predicting continuous outcomes.

**SteelPulse** explores the application of machine learning techniques to steel-production data, with a focus on predictive modelling, performance evaluation, and model generalisation.

### 🎯 Project Objectives

The main objectives of this project are:

| No. | Objective | Description |
|:---:|---|---|
| 01 | 📊 Data Exploration | Understand the dataset using descriptive statistics and visualisations. |
| 02 | 🔍 Statistical Analysis | Investigate feature distributions and correlations. |
| 03 | 🛠️ Data Preprocessing | Prepare the dataset for machine learning. |
| 04 | 🤖 Model Development | Implement different regression algorithms. |
| 05 | ⚙️ Hyperparameter Tuning | Investigate suitable model configurations. |
| 06 | 📈 Model Evaluation | Compare models using appropriate evaluation metrics. |
| 07 | 🧪 Data Augmentation | Investigate the effect of adding noise to training data. |
| 08 | 📉 Training Data Analysis | Evaluate the influence of training dataset size. |
| 09 | 🏆 Performance Analysis | Investigate model limitations and generalisation. |

### 🔬 Expected Outcome

The project aims to identify the strengths and limitations of different regression algorithms and understand how data characteristics and training strategies influence predictive performance.

---


---

## 📚 3. Related Work

Machine Learning (ML) has become an important tool in modern manufacturing. Researchers have investigated its use in production monitoring, quality prediction, process analysis, and the prediction of material properties.

### 🔬 Previous Research

**1. Machine Learning for Predictive Quality in Manufacturing (2022)**

Tercan and Meisen reviewed machine learning and deep learning applications in manufacturing quality assurance. Their research explains how production data and quality measurements can be combined to develop predictive models.

**Relevance to SteelPulse:** This research supports the use of data-driven machine learning methods to analyse manufacturing data and predict production-related outcomes.

[Read Research Paper](https://doi.org/10.1007/s10845-022-01963-8)

**2. Machine Learning-Based Performance Predictions for Steels (2024)**

Fang et al. reviewed machine learning approaches for predicting steel performance using manufacturing process parameters. The study discusses the relationships between manufacturing conditions and steel properties, along with challenges involving data characteristics, feature analysis, and model optimisation.

**Relevance to SteelPulse:** This research provides a direct connection to the use of machine learning for analysing steel-related data and predicting continuous outcomes.

[Read Research Paper](https://doi.org/10.1007/s42243-024-01179-5)

**3. Deep Learning Applications in Iron and Steel Making (2024)**

Tsutsui et al. reviewed deep learning applications across different stages of iron and steel production. Their research discusses neural networks and other deep learning techniques for process prediction, anomaly detection, and product evaluation.

**Relevance to SteelPulse:** This study demonstrates the potential of neural network approaches, including Multi-Layer Perceptrons (MLPs), for analysing industrial production data.

[Read Research Paper](https://doi.org/10.2355/isijinternational.ISIJINT-2024-098)

### 📌 Research Gap and Project Contribution

Previous research demonstrates the potential of machine learning and deep learning in manufacturing and steel-related applications.

Building on these studies, SteelPulse investigates and compares multiple regression algorithms using an available numerical steel-production dataset.

The project focuses on:

- Comparing different regression algorithms.
- Investigating relationships between input features and the target variable.
- Evaluating model performance using multiple metrics.
- Studying the influence of training data size and data augmentation.
- Examining the challenges of model generalisation to unseen data.

The project aims to provide a practical comparison of machine learning approaches and identify their strengths and limitations when applied to the available dataset.

### 📖 References

1. Tercan, H., & Meisen, T. (2022). *Machine learning and deep learning based predictive quality in manufacturing: A systematic review.* Journal of Intelligent Manufacturing, 33, 1879–1905. https://doi.org/10.1007/s10845-022-01963-8

2. Fang, W., Huang, J.-X., Peng, T.-X., Long, Y., & Yin, F.-X. (2024). *Machine learning-based performance predictions for steels considering manufacturing process parameters: A review.* Journal of Iron and Steel Research International, 31, 1555–1581. https://doi.org/10.1007/s42243-024-01179-5

3. Tsutsui, K., Namba, T., Kihara, K., Hirata, J., Matsuo, S., & Ito, K. (2024). *Current Trends on Deep Learning Techniques Applied in Iron and Steel Making Field: A Review.* ISIJ International, 64(11), 1619–1640. https://doi.org/10.2355/isijinternational.ISIJINT-2024-098

---

---

## 📊 4. Dataset Description

### 📁 Dataset Overview

The dataset used in this project contains numerical data related to steel production. It is used to investigate relationships between process-related input variables and a continuous target variable.

The dataset is divided into separate training and testing files.

### 📌 Dataset Information

| Property | Description |
|---|---|
| Dataset Type | Numerical |
| Training Samples | 7,642 |
| Testing Samples | 3,337 |
| Total Samples | 10,979 |
| Input Features | 21 |
| Target Variable | `output` |
| Machine Learning Task | Supervised Regression |
| Data Format | CSV |
| Feature Names | `input1` to `input21` |

### 🔢 Dataset Structure

The dataset contains 22 columns:

- **Input Features:** `input1`, `input2`, ..., `input21`
- **Target Variable:** `output`

The 21 input features are used by the machine learning models to predict the continuous target variable `output`.

*Note: The physical meanings and units of the individual input features are not provided in the available dataset documentation.*

### 📂 Dataset Files

| File Name | Description |
|---|---|
| `train_data.csv` | Dataset used for model training and validation. |
| `test_data.csv` | Separate dataset reserved for final model evaluation. |

### 🔍 Initial Data Characteristics

- All columns contain numerical values.
- All values are within the range of 0 to 1.
- No missing values were identified during the initial inspection.
- No constant features were identified.
- No duplicate rows were identified within either dataset.

### 🔗 Dataset Source

The dataset was provided through the university course resources.

[Access the University Dataset](https://cloud.cps.unileoben.ac.at/index.php/s/xtsCHycaSiHsqHT)

---


---

## 🔍 5. Data Exploration and Analysis

Exploratory Data Analysis (EDA) was performed to understand the structure, distribution, and relationships within the steel-production dataset before applying machine learning algorithms.

### 📊 5.1 Descriptive Statistical Analysis

Descriptive statistics were used to understand the numerical characteristics of the dataset.

The analysis included:

- Mean and median values.
- Standard deviation.
- Minimum and maximum values.
- First and third quartiles.
- Distribution of input features and target variable.

### 📈 5.2 Feature Distribution Analysis

Histograms were used to visualise the distributions of the 21 input features and the target variable (`output`).

This analysis helps identify:

- Distribution patterns.
- Concentration of values.
- Skewness in numerical features.
- Differences in the range and spread of variables.

### 🔗 5.3 Correlation Analysis

Pearson correlation analysis was performed to investigate linear relationships between the input features and the target variable.

The strongest observed correlations with the target variable in the training dataset were:

| Feature | Pearson Correlation |
|---|---:|
| `input4` | -0.271 |
| `input3` | -0.209 |
| `input2` | -0.187 |
| `input1` | -0.143 |
| `input13` | +0.107 |
| `input20` | +0.106 |

The results indicate that most individual input features have relatively weak linear correlations with the target variable.

However, weak individual correlation does not necessarily mean that a feature is unimportant for machine learning prediction.

### ⚠️ 5.4 Outlier Analysis

The Interquartile Range (IQR) method was used to identify potential outliers in the numerical variables.

The analysis identified 286 potential outliers in the training target variable.

These observations were not automatically removed because extreme values may represent valid production-related observations rather than data errors.

### 🔄 5.5 Feature Relationship Analysis

Correlation analysis between input features identified some strongly correlated pairs:

| Feature Pair | Pearson Correlation |
|---|---:|
| `input1` and `input6` | -0.955 |
| `input12` and `input21` | +0.868 |

These relationships indicate that some input variables contain overlapping linear information.

The features were retained for subsequent model development.

### 📌 5.6 Key Observations

- The dataset contains numerical features with values between 0 and 1.
- Several input features show weak individual linear relationships with the target.
- Some input features are strongly correlated with each other.
- Potential outliers were identified using the IQR method.
- Further analysis is required to understand differences between the training and testing datasets.

---

---

## 🛠️ 6. Data Preprocessing

Data preprocessing is an important step in preparing the dataset for machine learning. The objective is to ensure that the data is suitable for model development and evaluation.

### 🔍 6.1 Data Quality Checks

The following checks were performed:

- Checked the dataset structure and data types.
- Identified missing values.
- Checked for duplicate observations.
- Identified constant features.
- Examined the numerical ranges of the variables.

No missing values, duplicate rows within either dataset, or constant features were identified.

### 🎯 6.2 Feature and Target Separation

The dataset was separated into input features and the target variable.

- **X:** 21 input features (`input1` to `input21`).
- **y:** Target variable (`output`).

The input features were used to train the regression models, while the target variable represented the values to be predicted.

### ✂️ 6.3 Training and Validation Split

The original training dataset was divided into two subsets:

| Dataset | Percentage | Observations |
|---|---:|---:|
| Training subset | 80% | 6,113 |
| Validation subset | 20% | 1,529 |
| Original test dataset | Separate | 3,337 |

A random split was performed using `random_state=42` to ensure reproducibility.

The validation dataset was used for model comparison and model selection.

The separate test dataset was reserved for final evaluation.

### 📏 6.4 Feature Scaling

StandardScaler was applied to models that are sensitive to the scale of input features.

The scaling transformation was incorporated into machine learning pipelines to ensure that the scaler was fitted using training data only and then applied to validation and test data.

Random Forest Regression was used without standard scaling because tree-based models do not generally require feature standardisation.

### ⚠️ 6.5 Data Handling Considerations

Potential outliers were investigated but not automatically removed.

The original test dataset was kept separate during model training and hyperparameter tuning to avoid data leakage.

Differences between the training and test feature distributions were also investigated as part of the model generalisation analysis.

---

---

## 🤖 7. Machine Learning Models

Four supervised machine learning regression algorithms were implemented to investigate their ability to predict the target variable (`output`) using the 21 numerical input features.

### 7.1 Linear Regression

**Linear Regression** is a statistical learning algorithm that models the relationship between input features and a continuous target variable using a linear equation.

It was selected as a baseline model to understand how well a simple linear approach can predict steel-production output.

**Key Characteristics:**
- Simple and interpretable.
- Assumes a linear relationship between features and target.
- Provides a baseline for comparison with more complex models.

### 7.2 Random Forest Regression

**Random Forest Regression** is an ensemble learning algorithm that combines multiple decision trees to generate predictions.

Each tree produces a prediction, and the final output is calculated by averaging the predictions from all trees.

**Key Characteristics:**
- Captures nonlinear relationships.
- Can model complex feature interactions.
- Reduces dependence on a single decision tree.
- May overfit if model complexity is not controlled.

### 7.3 Support Vector Regression (SVR)

**Support Vector Regression (SVR)** is based on Support Vector Machines and is designed to predict continuous numerical values.

An RBF (Radial Basis Function) kernel was used to capture potentially nonlinear relationships between the input features and target variable.

**Key Characteristics:**
- Can model nonlinear relationships using kernels.
- Uses a margin-based approach to regression.
- Sensitive to parameter selection and feature scaling.

### 7.4 Multi-Layer Perceptron (MLP)

**Multi-Layer Perceptron (MLP)** is a feedforward artificial neural network consisting of an input layer, hidden layers, and an output layer.

The MLP model was implemented with two hidden layers containing 64 and 32 neurons, respectively.

**Key Characteristics:**
- Learns complex nonlinear relationships.
- Uses interconnected neurons and activation functions.
- Requires suitable training parameters.
- May require more data and tuning to achieve good generalisation.

### 📋 7.5 Model Configuration

| Model | Configuration |
|---|---|
| Linear Regression | StandardScaler + LinearRegression |
| Random Forest | 100 trees, random_state=42 |
| SVR | StandardScaler + RBF kernel |
| MLP | StandardScaler + hidden layers (64, 32), max_iter=1000, early_stopping=True |

### 🎯 7.6 Model Selection Strategy

The four algorithms were selected to compare different approaches to regression:

- Linear Regression provides a simple baseline.
- Random Forest captures nonlinear patterns using decision trees.
- SVR investigates kernel-based regression.
- MLP explores neural-network-based prediction.

Their performance was compared using consistent validation data and evaluation metrics.

---

---

## ⚙️ 8. Model Training and Hyperparameter Tuning

The selected regression models were trained using the training subset and evaluated using the validation subset.

### 8.1 Model Training

The four regression algorithms were trained using the same training-validation split to ensure a fair comparison.

The models were:

- Linear Regression
- Random Forest Regression
- Support Vector Regression (SVR)
- Multi-Layer Perceptron (MLP)

### 8.2 Cross-Validation

Five-fold cross-validation was performed to obtain a more reliable estimate of model performance.

The training data was divided into five folds. In each iteration, four folds were used for training and the remaining fold was used for validation.

This process was repeated five times, with each fold used once for validation.

The mean and standard deviation of the evaluation metrics were calculated to compare model performance and consistency.

### 8.3 Hyperparameter Tuning

RandomizedSearchCV was applied to the Random Forest model to investigate whether different hyperparameter combinations could improve predictive performance.

The search evaluated 30 parameter combinations using five-fold cross-validation.

The following hyperparameters were investigated:

- `n_estimators`
- `max_depth`
- `min_samples_split`
- `min_samples_leaf`
- `max_features`

### 8.4 Best Hyperparameters

The best parameter combination identified by RandomizedSearchCV was:

| Hyperparameter | Selected Value |
|---|---:|
| `n_estimators` | 300 |
| `max_depth` | 20 |
| `min_samples_split` | 10 |
| `min_samples_leaf` | 1 |
| `max_features` | 0.7 |

The best cross-validation RMSE was approximately 0.0606.

### 8.5 Baseline vs Tuned Random Forest

| Metric | Baseline Random Forest | Tuned Random Forest |
|---|---:|---:|
| Validation MAE | 0.0455 | 0.0457 |
| Validation RMSE | 0.0619 | 0.0621 |
| Validation R² | 0.4231 | 0.4203 |

The tuned Random Forest did not improve validation performance compared with the baseline model.

Therefore, the baseline Random Forest was retained for final model evaluation.

### 📌 Key Observation

Hyperparameter tuning does not always improve model performance. In this experiment, the baseline Random Forest achieved slightly better validation results than the tuned version.

---

---

## 📈 9. Model Evaluation and Comparison

The performance of the four regression models was evaluated using standard regression metrics. The evaluation was conducted on the validation dataset to compare their predictive capabilities.

### 9.1 Evaluation Metrics

The following metrics were used:

| Metric | Description |
|---|---|
| MAE | Measures the average absolute prediction error. |
| MSE | Measures the average squared prediction error. |
| RMSE | Measures prediction error in the original target scale, with larger errors penalised more heavily. |
| R² Score | Measures how much target variation is explained by the model relative to a mean-prediction baseline. |

Lower MAE, MSE and RMSE values indicate better predictive accuracy. Higher R² values generally indicate better performance.

### 9.2 Validation Performance

The following table presents the validation results obtained from the four regression models.

| Model | MAE | MSE | RMSE | R² |
|---|---:|---:|---:|---:|
| Linear Regression | 0.0590 | 0.0059 | 0.0770 | 0.1090 |
| Random Forest | 0.0455 | 0.0038 | 0.0619 | 0.4231 |
| SVR | 0.0560 | 0.0054 | 0.0734 | 0.1907 |
| MLP | 0.0654 | 0.0075 | 0.0867 | -0.1295 |

### 9.3 Cross-Validation Results

Five-fold cross-validation was used to investigate the consistency of model performance.

| Model | Mean R² | Mean RMSE | Mean MAE |
|---|---:|---:|---:|
| Linear Regression | 0.1733 | 0.0757 | 0.0585 |
| Random Forest | 0.4699 | 0.0606 | 0.0453 |
| SVR | 0.2477 | 0.0723 | 0.0562 |
| MLP | -0.0822 | 0.0866 | 0.0659 |

### 9.4 Final Test Performance

After selecting the baseline Random Forest model, it was retrained using the complete original training dataset and evaluated on the separate test dataset.

| Metric | Test Result |
|---|---:|
| MAE | 0.1347 |
| MSE | 0.0259 |
| RMSE | 0.1610 |
| R² | -1.8975 |

### 9.5 Performance Analysis

The Random Forest model achieved the best validation performance among the four algorithms, with a validation R² score of 0.4231.

However, its final test performance was considerably worse, with an R² score of -1.8975.

A negative R² score indicates that the model performed worse than a baseline that predicts the mean of the actual test targets.

This difference suggests that the model did not generalise well to the supplied test dataset.

Further investigation identified substantial differences between the training and test feature distributions. These differences may contribute to the poor test performance.

### 🏆 Overall Observation

Random Forest was the strongest model during validation and cross-validation. However, its poor test performance highlights the importance of investigating dataset characteristics and generalisation before drawing conclusions about model reliability.

---
