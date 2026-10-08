# ❤️ Heart Disease Prediction using Machine Learning

This project focuses on predicting the presence of heart disease using machine learning classification algorithms. The dataset is cleaned, preprocessed, encoded, and divided into training and testing sets before training multiple classification models.

The project also investigates how different feature scaling techniques affect the performance of different machine learning models.

---

## 📌 Project Overview

Heart disease is one of the major health-related challenges worldwide. Machine learning can be used to analyze patient-related features and predict whether a patient is likely to have heart disease.

In this project, several classification algorithms are trained and compared using different feature scaling techniques.

### Machine Learning Models

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Gaussian Naive Bayes
- Random Forest

### Feature Scaling Techniques

- Standard Scaling
- Min-Max Scaling
- Robust Scaling
- Without Scaling

---

## 📊 Dataset

The project uses the **Heart Failure Prediction / Heart Disease Prediction dataset**.

The dataset contains patient health-related features such as:

- Age
- Sex
- Chest Pain Type
- Resting Blood Pressure
- Cholesterol
- Fasting Blood Sugar
- Resting ECG
- Maximum Heart Rate
- Exercise-Induced Angina
- ST Depression
- ST Slope

### Target Variable

`HeartDisease`

Where:

- `0` = No Heart Disease
- `1` = Heart Disease

---

## 🛠️ Data Preprocessing

The following preprocessing steps were performed:

1. Loaded the dataset using Pandas.
2. Checked the dataset structure and data types.
3. Checked missing values.
4. Identified `"?"` values as missing data.
5. Treated impossible zero values in `Cholesterol` and `RestingBP` as missing values.
6. Removed columns containing more than 20% missing values.
7. Filled numerical missing values using the median.
8. Filled categorical missing values using the mode.
9. Converted categorical variables into numerical values using Label Encoding.
10. Separated features and target variable.
11. Split the dataset into training and testing sets.

### Train-Test Split

```text
Training Data: 80%
Testing Data: 20%

random_state = 42
stratify = y
```

---

## 🤖 Machine Learning Models

### 1. Logistic Regression

Logistic Regression is used as a linear classification algorithm for predicting whether a patient has heart disease.

### 2. K-Nearest Neighbors (KNN)

KNN predicts the class of a data point based on the classes of its nearest neighboring observations.

### 3. Gaussian Naive Bayes

Gaussian Naive Bayes is a probabilistic classification algorithm based on Bayes' theorem.

### 4. Random Forest

Random Forest is an ensemble learning algorithm that combines multiple decision trees to improve classification performance.

---

## ⚖️ Scaling Methods

Different scaling techniques were tested to understand their effect on model performance.

| Scaling Method | Description |
|---|---|
| Standard Scaling | Standardizes features using mean and standard deviation |
| Min-Max Scaling | Scales features to a fixed range |
| Robust Scaling | Uses median and interquartile range |
| Without Scaling | Uses the original feature values |

Scaling was applied inside a `Pipeline`, ensuring that the scaler was fitted only on the training data.

---

## 📈 Model Comparison

Each machine learning model was trained using all four scaling approaches.

The following combinations were evaluated:

```text
Logistic Regression × 4 Scaling Methods
KNN × 4 Scaling Methods
Naive Bayes × 4 Scaling Methods
Random Forest × 4 Scaling Methods
```

The final notebook generates a comparison table and a grouped bar chart showing the accuracy of each model under different scaling methods.

---

## 📊 Evaluation Metric

The main evaluation metric used in this project is:

### Accuracy

Accuracy measures the proportion of correctly classified samples.

```text
Accuracy = Correct Predictions / Total Predictions
```

The notebook also imports:

- Classification Report
- Confusion Matrix

for further model evaluation.

---

## 📉 Results

The model comparison results are generated directly from the notebook.

After running the notebook, the accuracy comparison can be viewed in the generated results table and visualization.

### Model Performance

| Model | Standard Scaling | Min-Max Scaling | Robust Scaling | Without Scaling |
|---|---:|---:|---:|---:|
| Logistic Regression | — | — | — | — |
| KNN | — | — | — | — |
| Naive Bayes | — | — | — | — |
| Random Forest | — | — | — | — |

> **Note:** Run the notebook to populate the actual accuracy values.

---

## 📈 Visualization

The notebook generates a grouped bar chart comparing model accuracy across different scaling methods.

You can place the generated figure inside the repository:

```text
results/model-comparison.png
```

Then display it in this README using:

```markdown
![Model Comparison](results/model-comparison.png)
```

---

## 💻 Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook

---

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/heart-disease-prediction.git
```

Move into the project directory:

```bash
cd heart-disease-prediction
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ How to Run

Open the Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
20245103173-ml-lab-task-hard-disease.ipynb
```

Run all cells sequentially to reproduce the analysis and model comparison.

---

## 📁 Project Structure

```text
heart-disease-prediction/
│
├── README.md
├── 20245103173-ml-lab-task-hard-disease.ipynb
├── requirements.txt
├── .gitignore
│
├── data/
│   └── README.md
│
├── results/
│   └── model-comparison.png
│
└── LICENSE
```

---

## 🎯 Objectives

The main objectives of this project are:

- To preprocess a real-world healthcare dataset.
- To handle missing and invalid values.
- To convert categorical data into numerical form.
- To train multiple machine learning classification models.
- To investigate the effect of feature scaling.
- To compare model performance using accuracy.
- To visualize the performance differences between models.

---

## ⚠️ Disclaimer

This project is developed for educational and academic purposes only.

The predictions generated by this machine learning model should **not** be considered medical advice or used as a substitute for professional medical diagnosis.

---

## 👨‍💻 Author

**20245103173**

Machine Learning Lab Project

---

## ⭐ Acknowledgement

The dataset used in this project is the Heart Failure Prediction dataset available through Kaggle.

If you find this project useful, feel free to ⭐ star the repository.
