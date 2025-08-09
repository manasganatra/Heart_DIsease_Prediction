# Heart Disease Prediction Using Machine Learning

A comprehensive machine learning project to predict heart disease using various classification algorithms. This project analyzes patient data and builds predictive models to identify individuals at risk of heart disease.

## 📋 Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Model Performance](#model-performance)
- [Methodology](#methodology)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

Heart disease is one of the leading causes of death worldwide. This project uses machine learning techniques to predict the likelihood of heart disease in patients based on various medical attributes. The analysis includes data exploration, visualization, feature engineering, and model comparison.

## 📊 Dataset

The project uses the `heart.csv` dataset containing medical records with the following characteristics:

- **Records**: 303 patient records
- **Features**: 14 attributes including demographic, clinical, and diagnostic measures
- **Target**: Binary classification (0 = No heart disease, 1 = Heart disease)

### Dataset Features

| Feature | Description | Type |
|---------|-------------|------|
| age | Age of the patient | Continuous |
| sex | Gender (0 = Female, 1 = Male) | Binary |
| cp | Chest pain type (0-3) | Categorical |
| trestbps | Resting blood pressure (mm Hg) | Continuous |
| chol | Serum cholesterol (mg/dl) | Continuous |
| fbs | Fasting blood sugar > 120 mg/dl | Binary |
| restecg | Resting ECG results (0-2) | Categorical |
| thalach | Maximum heart rate achieved | Continuous |
| exang | Exercise induced angina | Binary |
| oldpeak | ST depression induced by exercise | Continuous |
| slope | Slope of peak exercise ST segment | Categorical |
| ca | Number of major vessels colored by fluoroscopy | Categorical |
| thal | Thalassemia (3 = normal, 6 = fixed defect, 7 = reversable defect) | Categorical |
| target | Heart disease diagnosis | Binary |

## 🛠 Installation

### Prerequisites
- Python 3.7 or higher
- pip package manager

### Required Libraries
```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

Or install from requirements file:
```bash
pip install -r requirements.txt
```

### Requirements.txt
```
numpy>=1.21.0
pandas>=1.3.0
matplotlib>=3.4.0
seaborn>=0.11.0
scikit-learn>=1.0.0
```

## 🚀 Usage

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/heart-disease-prediction.git
cd heart-disease-prediction
```

2. **Ensure the dataset is in the project directory**
Make sure `heart.csv` is in the same directory as your script.

3. **Run the analysis**
```bash
python heart_disease_prediction.py
```

## 📈 Model Performance

The project evaluates three different machine learning algorithms:

| Algorithm | Best Parameters | Cross-Validation Accuracy |
|-----------|----------------|--------------------------|
| **K-Neighbors Classifier** | k=12 | ~87.5% |
| **Decision Tree Classifier** | max_depth=3 | ~82.1% |
| **Random Forest Classifier** | n_estimators=90 | ~85.2% |

*Note: Exact accuracies may vary due to random state in cross-validation*

## 🔬 Methodology

### 1. Data Exploration
- Dataset shape and structure analysis
- Data type identification
- Missing value detection
- Statistical summary generation

### 2. Data Visualization
- Histogram plots for all features
- Target variable distribution analysis
- Correlation heatmap for feature relationships

### 3. Feature Engineering
- **Categorical Encoding**: Applied one-hot encoding to categorical variables (sex, cp, fbs, restecg, exang, slope, ca, thal)
- **Feature Scaling**: Standardized continuous variables (age, trestbps, chol, thalach, oldpeak) using StandardScaler

### 4. Model Training & Evaluation
- **Cross-Validation**: Used 10-fold cross-validation for robust evaluation
- **Hyperparameter Tuning**: Grid search approach for optimal parameters
- **Performance Visualization**: Plotted accuracy scores across different parameter values

## 📊 Results

### Key Findings:
1. **Best Performing Model**: K-Neighbors Classifier with k=12 achieved the highest accuracy
2. **Feature Importance**: Correlation analysis revealed strong relationships between certain features and heart disease
3. **Balanced Dataset**: The target variable shows relatively balanced distribution


