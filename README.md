# GlobalAI-Akbank-Machine-Learning

# # Heart Disease Classification | Machine Learning

 machine learning project developed as part of the **Akbank Machine Learning Bootcamp**, using the 2020 CDC Behavioral Risk Factor Surveillance System (BRFSS) dataset to classify heart disease status.

## Project Overview

The objective of this project is to investigate how machine learning algorithms can identify patterns associated with heart disease using health-related and lifestyle data.

This is an educational classification project. Its results should not be interpreted as a clinically validated diagnostic tool.

## Dataset

- **Source:** [Personal Key Indicators of Heart Disease — Kaggle](https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease)
- **Dataset size:** 319,795 observations
- **Number of features:** 18, as reported in the original project documentation
- **Target variable:** `HeartDisease`
- **Target encoding:** `0` — No; `1` — Yes

## Methodology

### 1. Data Preprocessing
- Encoding categorical variables
- Standardizing numerical features

### 2. Feature Engineering

Additional features were created to represent health and lifestyle patterns, including:

- `BMI_Category`
- `UnhealthyScore`
- `RiskyLifestyle`

These features were designed to explore whether engineered variables could improve classification performance.

### 3. Model Development

Three tree-based machine learning algorithms were evaluated:

- Random Forest
- XGBoost
- LightGBM

### 4. Class Imbalance Handling

Class imbalance was addressed using techniques such as:

- `class_weight='balanced'`
- `scale_pos_weight`

The specific configuration may vary by algorithm.

## Model Evaluation

The following presents a comparison of the models' performance on the test dataset.

| Model         | Accuracy | Recall | F1 Score |
|---------------|----------|--------|----------|
| Random Forest | 0.83     | 0.56   | 0.35     |
| XGBoost       | 0.75     | 0.76   | 0.35     |
| LightGBM      | 0.74     | 0.79   | 0.34     |

### Interpretation

Random Forest achieved the highest reported accuracy, while LightGBM achieved the highest recall.

In a health-related classification task, recall is important because it measures the proportion of actual positive cases correctly identified by the model. However, higher recall alone does not establish that a model is suitable for clinical use.

The results should be interpreted alongside precision, F1-score, confusion matrices, and the consequences of false-positive and false-negative predictions.

## Future Improvements

Potential directions for further development include:

- **Model explainability:** Applying SHAP or LIME to investigate feature contributions and model predictions.
- **Pipeline development:** Building a reproducible preprocessing and training pipeline.
- **Deployment:** Developing a web interface using Streamlit or Flask for educational demonstration.
- **Additional models:** Evaluating other approaches, such as multilayer perceptrons, where justified by the data and experimental results.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- LightGBM
- Matplotlib
- Seaborn

## Project Links

- **GitHub Repository:** [GlobalAI-Akbank-Machine-Learning](https://github.com/ozl3m3r/GlobalAI-Akbank-Machine-Learning)

## Disclaimer

This project was developed for educational purposes. It is not intended to diagnose heart disease, replace professional medical evaluation, or support clinical decisions.
 
