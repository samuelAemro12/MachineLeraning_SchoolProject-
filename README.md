# Breast Cancer Recurrence Prediction

&#x20;

This project focuses on predicting breast cancer recurrence events using machine learning models. The goal is to identify patients at risk of recurrence based on features such as tumor size, degree of malignancy, lymph node involvement, and other clinical attributes.

---

## Table of Contents

1. [Overview](#overview)
2. [Dataset](#dataset)
3. [Features](#features)
4. [Installation](#installation)
5. [Usage](#usage)
6. [Models](#models)
7. [Evaluation Metrics](#evaluation-metrics)
8. [Results](#results)
9. [Contributing](#contributing)

---

## Overview

Breast cancer recurrence prediction is critical for improving patient outcomes. This project uses machine learning techniques to predict whether a patient will experience a recurrence event (`recurrence-events`) or not (`no-recurrence-events`). The dataset contains clinical features of breast cancer patients, and three models (Random Forest, Naive Bayes, and SVM) are trained and evaluated.

---

## Dataset

The dataset used in this project is stored in `breast-cancer.csv`. It contains the following information:

- **Rows**: Patient records.
- **Columns**: Clinical features and target variable (`Class`).

### Key Characteristics:

- **Target Variable**: `Class` (binary classification: `recurrence-events` or `no-recurrence-events`).
- **Features**: Age, menopausal status, tumor size, lymph node involvement, degree of malignancy, breast quadrant, radiation therapy, etc.
- **Missing Values**: Some features contain missing values, which are handled during preprocessing.

---

## Features

| Feature       | Description                                       | Connection to Recurrence Events                                 |
| ------------- | ------------------------------------------------- | --------------------------------------------------------------- |
| `age`         | Age range of the patient                          | Younger/older patients may have different recurrence risks.     |
| `menopause`   | Menopausal status                                 | Hormonal changes can influence recurrence risk.                 |
| `tumor-size`  | Size of the tumor                                 | Larger tumors are associated with higher recurrence risk.       |
| `inv-nodes`   | Number of invaded lymph nodes                     | More invaded nodes indicate higher metastasis risk.             |
| `node-caps`   | Presence of capsular involvement in lymph nodes   | Indicates invasive tumors, increasing recurrence risk.          |
| `deg-malig`   | Degree of malignancy                              | Higher malignancy grades are linked to more aggressive cancers. |
| `breast`      | Location of the tumor (left/right)                | May be relevant for surgical/treatment decisions.               |
| `breast-quad` | Quadrant of the breast where the tumor is located | Certain quadrants may be linked to higher recurrence risk.      |
| `irradiat`    | Whether the patient received radiation therapy    | Radiation therapy reduces recurrence risk.                      |

---

## Installation

To set up the project locally, follow these steps:

### 1. Clone the Repository

```bash
git clone https://github.com/samuelAemro12/MachineLeraning_SchoolProject-.git
cd MachineLeraning_SchoolProject-
```

### 2. Install Dependencies

Install the required Python libraries using pip:

```bash
pip install -r requirements.txt
```

### 3. Dataset

Ensure the `breast-cancer.csv` file is placed in the project directory.

---

## Usage

Run the following command to preprocess the data, train the models, and evaluate their performance:

```bash
python main.py
```

### Steps Executed by the Script:

1. Load and preprocess the dataset (handle missing values, encode categorical variables, drop duplicates).
2. Split the data into training and testing sets.
3. Train three machine learning models: Random Forest, Naive Bayes, and SVM.
4. Evaluate the models using accuracy and F1-Score.
5. Generate visualizations comparing model performance.

---

## Models

Three machine learning models are implemented and compared:

### 1. Random Forest

- Ensemble learning method that builds multiple decision trees.
- Handles noise and overfitting effectively.

### 2. Naive Bayes

- Probabilistic model based on Bayes' theorem.
- Assumes feature independence, making it computationally efficient.

### 3. Support Vector Machine (SVM)

- Finds the optimal hyperplane for classification.
- Effective for high-dimensional data.

---

## Evaluation Metrics

The models are evaluated using the following metrics:

- **Accuracy**: Measures the overall correctness of predictions.
- **F1-Score**: Balances precision and recall, particularly important for imbalanced datasets like this one.

---

## Results

| Model         | Accuracy | F1-Score |
| ------------- | -------- | -------- |
| Random Forest | 69.09%   | 0.41     |
| Naive Bayes   | 65.45%   | 0.39     |
| SVM           | 67.27%   | 0.31     |

### Key Findings:

- **Random Forest** performs best in both accuracy and F1-Score.
- All models struggle with detecting `recurrence-events`, indicating room for improvement.

---

## Contributing

Contributions are welcome! To contribute:

1. **Fork the repository**.
2. **Create a new branch**:
   ```bash
   git checkout -b feature/YourFeature
   ```
3. **Commit your changes**:
   ```bash
   git commit -m "Add YourFeature"
   ```
4. **Push to the branch**:
   ```bash
   git push origin feature/YourFeature
   ```
5. **Open a pull request**.

Please ensure your code follows the project's coding standards and includes appropriate documentation.

