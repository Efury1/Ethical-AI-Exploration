

# AI Ethics Project: IDOOU Activity Recommender

## Overview

This project involves designing a machine learning model to predict user budgets for the IDOOU app, a personalized activity recommendation platform. The app aims to simplify the process of finding activities by considering user preferences, weather conditions, and budgets.

The project emphasizes fairness and ethical AI practices by exploring biases in demographic attributes like gender, age, and education level. Using tools like the IBM AIF360 library, fairness metrics are evaluated to address potential biases in the model's predictions.

<blockquote class="imgur-embed-pub" lang="en" data-id="a/z197Kxx"  ><a href="//imgur.com/a/z197Kxx"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>
---

## Features

- **Personalized Recommendations**: Predicts user budgets to offer tailored activity suggestions.
- **Fairness Analysis**: Incorporates fairness metrics (e.g., statistical parity, disparate impact) to ensure ethical AI practices.
- **Extensive Data Preprocessing**: Handles missing values, duplicate data, and categorization of key variables like age and budget.
- **Machine Learning Models**:
  - Logistic Regression
  - Gaussian Naive Bayes
- **Visualization**: Comprehensive visualizations for data exploration, fairness metrics, and model evaluation.

---

## Project Structure

- **Data Preprocessing**: Cleaning and categorizing the dataset, handling imbalances, and encoding categorical variables.
- **Model Training**:
  - Two models are trained using a train-test-validation split.
  - Metrics such as balanced accuracy and confusion matrices are used for evaluation.
- **Fairness Analysis**: Using IBM AIF360 toolkit to evaluate biases.
- **Interpretability**: Implementing tools like LIME to understand model predictions.

---

## Dataset

- **Source**: A synthetic dataset based on user experience studies with ~300,000 participants.
- **Attributes**:
  - Demographic: Age, Gender, Education Level
  - Activity: Recommended Activity, Budget
- **Preprocessing Steps**:
  - Removal of missing values and duplicates.
  - Categorization and binning of age and budget attributes.
  - One-hot encoding for categorical variables.

---

## Installation

1. Clone this repository:
   ```
   git clone <repository_url>
   ```
2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
3. Set up the dataset:
   - Place the dataset (`udacity_ai_ethics_project_data.csv`) in the `data/` directory.

---

## Usage

1. **Preprocess the dataset**:
   ```
   python preprocess.py
   ```
2. **Train models**:
   ```
   python train.py
   ```
3. **Evaluate fairness**:
   ```
   python fairness_analysis.py
   ```
4. **Visualize results**:
   ```
   python visualize.py
   ```

---

## Results

- **Model Metrics**:
  - Logistic Regression: Best Balanced Accuracy of 99.66%
  - Gaussian Naive Bayes: Best Balanced Accuracy of 99.37%
- **Fairness Metrics**:
  - Statistical Parity Difference: ~-0.98
  - Disparate Impact: ~0.01

Both models achieve high accuracy but show biases, particularly in education-based predictions. Strategies to mitigate bias are incorporated in the analysis.

---

## Ethical Considerations

- **Fairness**: Bias in demographic groups is addressed through data preprocessing and fairness-aware training.
- **Privacy**: User data is processed securely, and only essential attributes are used.
- **Transparency**: Interpretability tools like LIME provide insights into model predictions.

---

## Future Work

- **Enhanced Fairness**: Implement advanced bias-mitigation techniques.
- **Real-world Testing**: Validate the model using real-world datasets.
- **User Feedback**: Incorporate user feedback mechanisms to improve predictions and fairness.

---
