# Credit-Card-Fraud-Detetction

## Overview

The Credit Card Fraud Detection Problem revolves around creating a model based on historical credit card transactions, especially those that were confirmed as fraudulent. The objective is to design a system that can effectively distinguish whether a new transaction is a fraudulent one or not. 

## Dataset

The dataset used in this project is obtained from [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud). It consists of anonymized credit card transactions labeled as fraudulent or non-fraudulent.

## Model Used

Two outlier detection algorithms are implemented in this project:

- **Isolation Forest**: An ensemble method for anomaly detection that isolates observations by randomly selecting a feature and then randomly selecting a split value between the maximum and minimum values of the selected feature.
- **Local Outlier Factor (LOF)**: A density-based algorithm that computes the local density deviation of a data point with respect to its neighbors.

## Results

After training and evaluating the models, the following conclusions were reached:

- Both models achieved high overall accuracy, but their performance in detecting fraudulent transactions was suboptimal.
- Isolation Forest achieved an accuracy of approximately 99.75%, with a precision, recall, and F1-score for detecting fraud of 0.28.
- Local Outlier Factor achieved an accuracy of approximately 99.66%, with a precision, recall, and F1-score for detecting fraud of 0.02.

## Conclusion

While the models demonstrated high accuracy, their performance in detecting fraudulent transactions was limited by the highly imbalanced nature of the dataset. Further optimization and experimentation with different algorithms and techniques are required to improve fraud detection accuracy.

## Usage

1. Clone the repository and navigate to the project directory:

```bash
git clone https://github.com/KelvinPuyam/Credit-Card-Fraud-Detection.git
cd Credit-Card-Fraud-Detection
```

2. Download the creditcard.csv dataset from [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud).

3. Move the creditcard.csv file to the root directory of the project.

4. Create a new Conda environment and activate it:

```bash
conda create --name fraud_detection_env python=3.8
conda activate fraud_detection_env
```

5. Install the required dependencies in your new environment:

```bash
pip install -r requirements.txt
```

6. Run the main script:

```bash
python FraudDetection.py
```
