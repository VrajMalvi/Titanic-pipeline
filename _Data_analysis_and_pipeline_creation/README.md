# Predicting Survival on the Titanic

## Introduction

This repository contains code for predicting survival on the Titanic using machine learning. The code utilizes a pipeline to preprocess the data, impute missing values, encode categorical variables, and build a predictive model using the Random Forest Classifier. The performance of the model is evaluated using accuracy and roc-auc metrics.

## Installation

Before running the code, make sure to install the required library by executing the following command:

```bash
pip install feature_engine
```

## Data

The dataset used for this project is available online and can be loaded using the following code:

```bash
import pandas as pd
data = pd.read_csv('https://www.openml.org/data/get_csv/16826755/phpMYEkMl')
```

## Data Preparation

The dataset is preprocessed to handle missing values, extract relevant information from variables, and drop unnecessary columns. The prepared data includes features such as 'pclass', 'sex', 'age', 'fare', 'cabin', 'embarked', and 'title'.

## Configuration

The configuration section defines the variables to be used in the pipeline's transformers, including numerical and categorical variables.

## Pipeline

The main pipeline includes a series of transformers and a Random Forest Classifier. The steps include imputation of missing values, extraction of the first letter from the 'cabin' variable, grouping of rare categories, one-hot encoding of categorical variables, and feature scaling.

## Model Training

The pipeline is trained using the training set, and the Random Forest Classifier is fitted to the data.

## Model Evaluation

The performance of the model is evaluated on both the training and test sets using roc-auc and accuracy metrics. The results indicate high roc-auc and accuracy on the training set, while the test set results provide insight into the model's generalization capabilities.

```text
rain roc-auc: 0.9967194744976816
train accuracy: 0.9770773638968482

test roc-auc: 0.835
test accuracy: 0.8015267175572519
```
