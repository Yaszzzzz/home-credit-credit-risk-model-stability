# Project Overview
The project aims to build a predictive model for assessing credit risk using data provided by Home Credit. The model predicts the probability of default for each loan application based on various financial and personal attributes of the applicants.

# Table of Contents
1. [Overview](#overview)
2. [Project Structure](#project-structure)
3. [Dataset](#dataset)
4. [Feature Engineering](#feature-engineering)
5. [Model Training](#model-training)
6. [Evaluation](#evaluation)
7. [Submission](#submission)
8. [Environment Setup](#environment-setup)
9. [Dependencies](#dependencies)
10. [Usage](#usage)
11. [Contributing](#contributing)
12. [License](#license)
13. [Important Links](#important-links)

---

# Overview <a name="overview"></a>
The project involves developing a robust credit risk model using data from Home Credit. Various machine learning models are trained and evaluated to predict loan defaults accurately.

# Project Structure <a name="project-structure"></a>
.
├── README.md               # Overview and setup instructions
├── requirements.txt        # List of dependencies
├── train.py                # Main script for data preprocessing, modeling, and evaluation
├── utils.py                # Utility functions for data handling and feature engineering
├── data/
│   ├── train/              # Training dataset (parquet files)
│   └── test/               # Test dataset (parquet files)
├── models/                 # Saved model checkpoints
└── submissions/            # Submitted prediction files
# Dataset <a name="dataset"></a>
The dataset is provided in parquet format and includes multiple files from different sources related to loan applicants (e.g., static data, credit bureau records). Data preprocessing involves cleaning, aggregating, and transforming these files into a unified dataset suitable for modeling.

# Feature Engineering <a name="feature-engineering"></a>
Feature engineering involves creating new features from the raw dataset to enhance model performance. Steps include handling missing values, date variable transformations, aggregation features creation, and categorical variable encoding.

# Model Training <a name="model-training"></a>
The project trains several machine learning models including:
- CatBoostClassifier
- LGBMClassifier
- XGBClassifier
Models are trained using cross-validation with hyperparameter tuning and early stopping techniques to prevent overfitting.

# Evaluation <a name="evaluation"></a>
Model performance is evaluated using the Area Under the Receiver Operating Characteristic Curve (AUC-ROC) metric. Cross-validation provides estimates of model performance on unseen data partitions.

# Submission <a name="submission"></a>
Predictions for the test dataset are generated using trained models and saved as CSV files in the `submissions/` directory, formatted according to Kaggle competition submission requirements.

# Environment Setup <a name="environment-setup"></a>
To set up the environment:
1. Clone this repository.
2. Install dependencies listed in `requirements.txt`.
3. Ensure Python 3.x and necessary libraries are installed.

# Dependencies <a name="dependencies"></a>
Key Python libraries used:
- numpy
- pandas
- polars
- lightgbm, xgboost
- catboost
- scikit-learn
- seaborn, matplotlib

# Usage <a name="usage"></a>
To reproduce results:
1. Prepare the dataset as described in `train.py`.
2. Run `python train.py` to execute data preprocessing, model training, and evaluation.
3. Predictions for the test dataset will be generated and saved in the `submissions/` directory.

# Contributing <a name="contributing"></a>
Contributions to improve this project are welcome:
- Fork the repository.
- Make changes and submit a pull request.
- For major changes, open an issue first to discuss proposed modifications.

# License <a name="license"></a>
This project is licensed under the MIT License. See the LICENSE file for details.

# Important Links <a name="important-links"></a>
[Kaggle Competition - Home Credit Credit Risk Model Stability](https://www.kaggle.com/competitions/home-credit-credit-risk-model-stability)
