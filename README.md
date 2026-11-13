# SteelPulse: Understanding and Predicting Steel Production Through Machine Learning

**Individual Project – Applied Machine and Deep Learning**  
Montanuniversität Leoben  
MSc Industrial Data Science  
Winter Semester 2026/2027

**Student:** Usha Rahul  
**Supervisor / Course Instructor:** Linus Nwankwo  
**Date:** November 2026

---

## 1. Project Overview

SteelPulse is an individual machine learning project focused on analysing steel-production data and predicting a continuous target variable using supervised regression techniques.

The project uses a dataset containing 21 numerical input features (`input1` to `input21`) and one continuous target variable (`output`).

The main goal is to investigate how different machine learning regression models perform on the dataset, compare their predictive capabilities, and understand the factors affecting model performance.

The project includes data exploration, preprocessing, model development, hyperparameter tuning, cross-validation, model evaluation, data augmentation, and training dataset size analysis.

## 2. Motivation

Steel production involves complex processes in which multiple input variables can influence production outcomes.

Machine learning can help identify patterns in process-related data and develop predictive models. This project explores whether regression models can learn useful relationships between the available input features and the target variable.

Since the physical meanings and units of the input features are not provided, the project focuses on statistical and predictive analysis rather than direct interpretation of individual steel-production parameters.

## 3. Project Objectives

The main objectives are:

- Explore and understand the dataset through statistical analysis and visualisation.
- Identify missing values, duplicates, outliers, and correlations.
- Clean and preprocess the combined dataset.
- Apply appropriate feature normalization.
- Develop and compare different regression models.
- Perform hyperparameter tuning and cross-validation.
- Evaluate model performance using suitable regression metrics.
- Investigate the influence of training dataset size.
- Examine whether data augmentation using Gaussian noise improves prediction performance.
- Analyse residuals and feature importance.
- Discuss model limitations and possible future improvements.

## 4. Dataset Description

The dataset was provided through the university cloud platform.

**Dataset source:**  
https://cloud.cps.unileoben.ac.at/index.php/s/xtsCHycaSiHsqHT

The original dataset consisted of two CSV files:

| Dataset | Number of observations | Number of columns |
|---|---:|---:|
| Original training data | 7,642 | 22 |
| Original testing data | 3,337 | 22 |
| Combined dataset | 10,979 | 22 |

### Dataset features

- **Input features:** `input1` to `input21`
- **Target variable:** `output`
- **Problem type:** Supervised regression
- **Data type:** Numerical

The original training and testing files were combined before preprocessing, following the project instructions. The combined dataset was subsequently divided into new training, validation, and testing subsets.

## 5. Exploratory Data Analysis (EDA)

Exploratory data analysis was performed to understand the dataset's structure, distribution, and relationships.

The following analyses were conducted:

- Dataset information and descriptive statistics.
- Target variable distribution using histograms.
- Input feature distribution analysis.
- Pearson correlation analysis between input features and the target.
- Feature-to-feature correlation analysis.
- IQR-based outlier detection.
- Data quality checks for missing values, duplicates, infinite values, and invalid numerical values.

### Key observations

- No missing values or duplicate rows were identified.
- All input features were numerical.
- All values were within the observed range of 0 to 1.
- Approximately 75.85% of target observations were between 0.4 and 0.6.
- Several input features showed strong correlations with other input features.

These observations were considered during preprocessing and model development.

## 6. Data Preprocessing

The following preprocessing workflow was implemented:

1. Loaded the original training and testing CSV files.
2. Combined both datasets into one dataset.
3. Inspected the combined data for missing values, duplicates, and invalid values.
4. Investigated statistical outliers using the Interquartile Range (IQR) method.
5. Separated the input features and target variable.
6. Split the combined dataset into training, validation, and testing subsets.
7. Applied MinMaxScaler to the input features.

### Data splitting

| Subset | Samples | Percentage |
|---|---:|---:|
| Training | 7,685 | 70% |
| Validation | 1,647 | 15% |
| Testing | 1,647 | 15% |
| Total | 10,979 | 100% |

The scaler was fitted only on the training data and then applied to the validation and testing data to prevent data leakage.

The target variable was kept on its original scale to maintain interpretable regression results.

Statistical outliers were investigated but not automatically removed because extreme values are not necessarily data errors.

## 7. Machine Learning Models

Three regression model families were developed and evaluated.

### Model I: Random Forest Regression

Random Forest is an ensemble learning method that combines predictions from multiple decision trees.

Experiments included:

- Initial Random Forest model.
- Hyperparameter tuning using RandomizedSearchCV.
- Five-fold cross-validation.
- Training dataset size experiments.

Best parameters:

```python
{
    'n_estimators': 300,
    'max_depth': 20,
    'min_samples_split': 5,
    'min_samples_leaf': 2,
    'max_features': 0.9
}
```

### Model II: Gradient Boosting Regression

Gradient Boosting is an ensemble learning method that builds decision trees sequentially, with each new tree attempting to correct errors made by previous trees.

Experiments included:

- Initial Gradient Boosting model.
- Hyperparameter tuning using RandomizedSearchCV.
- Five-fold cross-validation.
- Final model selection and independent test evaluation.
- Feature importance analysis.

Best parameters:

```python
{
    'subsample': 0.7,
    'n_estimators': 500,
    'min_samples_split': 15,
    'min_samples_leaf': 4,
    'max_features': 0.7,
    'max_depth': 5,
    'learning_rate': 0.05
}
```

### Model III: Support Vector Regression (SVR)

Support Vector Regression was implemented using an RBF kernel to capture nonlinear relationships between input features and the target variable.

Experiments included:

- Initial SVR model.
- Hyperparameter tuning using RandomizedSearchCV.
- Five-fold cross-validation.
- Validation performance evaluation.

Best parameters:

```python
{
    'C': 10,
    'epsilon': 0.05,
    'gamma': 'scale'
}
```

## 8. Model Evaluation

Model performance was evaluated using the following regression metrics:

- **Mean Absolute Error (MAE):** Measures the average absolute difference between actual and predicted values.
- **Mean Squared Error (MSE):** Measures the average squared prediction error.
- **Root Mean Squared Error (RMSE):** Represents the square root of MSE and penalises larger errors.
- **Coefficient of Determination (R²):** Measures the proportion of target variance explained by the model.

Five-fold cross-validation was used to compare the final three model families.

### Cross-validation results

| Model | Mean MAE | Mean RMSE | Mean R² |
|---|---:|---:|---:|
| Random Forest | 0.05054 | 0.06736 | 0.48246 |
| Gradient Boosting | 0.05007 | 0.06669 | 0.49259 |
| SVR | 0.05493 | 0.07282 | 0.39530 |

Gradient Boosting achieved the best average cross-validation results among the three models.

## 9. Final Model and Test Results

Gradient Boosting was selected as the final model based on its cross-validation performance.

The selected model was retrained using the combined training and validation data, containing 9,332 observations, and evaluated once on the independent test set containing 1,647 observations.

### Final test performance

| Metric | Result |
|---|---:|
| MAE | 0.04829 |
| MSE | 0.00434 |
| RMSE | 0.06587 |
| R² | 0.46689 |

The model achieved better performance than a simple mean-prediction baseline.

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Mean Baseline | 0.06901 | 0.09024 | -0.00065 |
| Gradient Boosting | 0.04829 | 0.06587 | 0.46689 |

Compared with the baseline, Gradient Boosting reduced MAE by approximately 30.02% and RMSE by approximately 27.01%.

An R² of 0.46689 indicates that the model explains approximately 46.7% of the variance in the test target values. It does not represent prediction accuracy as a percentage.

## 10. Data Augmentation

Data augmentation was investigated by adding Gaussian noise to the training input features.

Three noise levels were tested:

- 0.01
- 0.03
- 0.05

The original training observations were combined with their noisy copies, while the target values remained unchanged.

Experiments were repeated using five random seeds.

### Average results across five seeds

| Experiment | Mean MAE | Mean RMSE | Mean R² |
|---|---:|---:|---:|
| Original Data | 0.04758 | 0.06430 | 0.48515 |
| Noise 0.01 | 0.04743 | 0.06396 | 0.49053 |
| Noise 0.03 | 0.04800 | 0.06481 | 0.47687 |
| Noise 0.05 | 0.04832 | 0.06505 | 0.47292 |

A small noise level of 0.01 produced a modest improvement in average RMSE and R². Higher noise levels reduced performance.

The physical validity of the generated noise could not be confirmed because the input variables' industrial meanings were unavailable.

## 11. Influence of Training Dataset Size

The influence of training dataset size was investigated using different fractions of the training data:

- 20%
- 40%
- 60%
- 80%
- 100%

The tuned Random Forest model was evaluated on the same validation dataset for each training size.

### Results

| Training Size | Number of Samples | MAE | RMSE | R² |
|---|---:|---:|---:|---:|
| 20% | 1,537 | 0.0546 | 0.0725 | 0.3454 |
| 40% | 3,074 | 0.0515 | 0.0690 | 0.4071 |
| 60% | 4,611 | 0.0493 | 0.0664 | 0.4515 |
| 80% | 6,148 | 0.0486 | 0.0656 | 0.4635 |
| 100% | 7,685 | 0.0474 | 0.0641 | 0.4877 |

The results indicate that increasing the training dataset size improved validation performance. However, the improvements became smaller as more training data was added.

## 12. Residual Analysis

Residual analysis was conducted to investigate the differences between actual and predicted target values.

The final Gradient Boosting model achieved a mean test residual of approximately 0.00151.

The model performed better in the dominant target range of 0.4–0.6, where most observations were concentrated.

Larger prediction errors occurred in the less frequent lower and upper target ranges. This suggests that the model has difficulty predicting extreme values when relatively few training examples are available.

## 13. Feature Importance

Two feature importance methods were investigated.

### Built-in Gradient Boosting Feature Importance

The five highest feature importance scores were:

1. `input6`
2. `input4`
3. `input19`
4. `input3`
5. `input2`

### Permutation Feature Importance

Permutation importance was calculated using the independent test dataset.

The five most influential features were:

1. `input6`
2. `input4`
3. `input1`
4. `input19`
5. `input2`

Both methods identified `input6` and `input4` as the most influential features.

However, correlations between input variables can affect individual importance rankings. The physical significance of these features cannot be determined without further information about the dataset.

## 14. Limitations

The project has several limitations:

- The physical meanings and measurement units of the input variables are unknown.
- The target distribution is concentrated mainly between 0.4 and 0.6, with few extreme observations.
- A random train-validation-test split was used instead of a time-based or production-batch-based split.
- Cross-validation was not nested, so model-selection performance estimates may be somewhat optimistic.
- The physical validity of Gaussian noise augmentation could not be confirmed.
- Further validation using representative industrial data is required before considering real-world deployment.

## 15. Future Work

Potential future improvements include:

- Obtaining physical descriptions and units for the input variables.
- Testing additional regression algorithms such as XGBoost, LightGBM, and neural networks.
- Collecting more representative data for extreme target values.
- Investigating SHAP values and partial dependence plots for improved model interpretation.
- Applying time-based or group-based validation if production timestamps or batch identifiers become available.
- Exploring physically meaningful data augmentation methods.
- Investigating nested cross-validation for more rigorous model selection.

## 16. Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## 17. Project Structure

```text
SteelPulse/
│
├── README.md
│
├── SteelPulse_ML_Project.ipynb
│
├── data/
│   ├── original_training_data.csv
│   └── original_testing_data.csv
│
└── results/
    ├── figures/
    └── tables/
```

*Note: The folder structure above is a suggested organisation. Adjust it to match the actual files in your repository.*

## 18. How to Run the Project

1. Clone or download the repository.
2. Install the required Python libraries.
3. Download the original dataset from the university cloud link.
4. Place the CSV files in the appropriate data directory.
5. Open `SteelPulse_ML_Project.ipynb` in Jupyter Notebook.
6. Run the notebook cells from beginning to end.

Install the required libraries using:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

## 19. References

- Tercan, H., & Meisen, T. (2022). Machine learning and deep learning based predictive quality in manufacturing: A systematic review.
- Fang, et al. (2024). Relevant research on machine learning applications in steel production and manufacturing.
- Tsutsui, et al. (2024). Relevant research on machine learning and data-driven approaches in materials and manufacturing.

---

**Project:** SteelPulse – Understanding and Predicting Steel Production Through Machine Learning  
**Course:** Applied Machine and Deep Learning  
**Institution:** Montanuniversität Leoben  
**Semester:** Winter Semester 2026/2027
