# 🏃‍♂️ Human Activity Recognition Using PCA

A collaborative student project to classify human activity from smartphone motion data using dimensionality reduction and classical machine learning models.

---

## 👥 Team

- **Harshul Shah**  
- **Lakshmipriya Narayanan**  
- **Priyasri Sankaran**
---

## 🎯 Project Overview

Human Activity Recognition (HAR) is the task of identifying a person’s physical activity using sensor data. In this project, we classify six daily activities—**Walking**, **Walking Upstairs**, **Walking Downstairs**, **Sitting**, **Standing**, and **Laying**—using smartphone accelerometer and gyroscope data.  

Given the **561-feature** high-dimensional input, we applied **Principal Component Analysis (PCA)** and **Kernel PCA** for dimensionality reduction and improved classification performance.

---

## 📁 Repository Contents

- `ActivityRecognition.py` – Data loading, preprocessing, PCA transformation  
- `ActivityRecognition2.py` – Linear SVM classifier training & evaluation  
- 'data.csv' -   Dataset differentiated into training and testing(70 + 30)
---

## 📚 Dataset

**UCI Human Activity Recognition Using Smartphones**  
- 📌 [Dataset Link](https://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)  
- 📋 7352 training + 2947 test instances  
- 📐 561 numeric features from time/frequency domain  
- 📱 Data collected from 30 volunteers (19–48 yrs) using Samsung Galaxy S II smartphones  

📝 Licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

---

## 🧪 Objective

To evaluate how dimensionality reduction (PCA and Kernel PCA) improves classification accuracy in high-dimensional HAR data when using:

- **Multinomial Logistic Regression (MLR)**
- **Linear Discriminant Analysis (LDA)**

---

## 🛠 Tools & Technologies

- **Programming Language**: R, Python  
- **Libraries**: 
  - R: `caret`, `ggplot2`, `factoextra`, `e1071`, `tidyverse`
  - Python: `scikit-learn`, `pandas`, `numpy`, `matplotlib`

---

## 🧠 Workflow Summary

### 1. **Data Preprocessing**
- Combined and labeled training/test datasets
- Features already standardized (range: -1 to 1)
- No missing values

### 2. **Dimensionality Reduction**
- Applied PCA and Kernel PCA (RBF kernel)
- First ~50 PCs explained >90% variance
- Reduced overfitting and improved computational efficiency

### 3. **Model Training & Evaluation**
- Trained MLR and LDA on:
  - Raw data
  - PCA-transformed data
  - Kernel PCA-transformed data
- Evaluated via accuracy, precision, recall, F1-score

---

## 📊 Results Summary

| Model Type              | Accuracy (Test) | Accuracy (Train) | Notes                        |
|------------------------|------------------|------------------|------------------------------|
| MLR (Raw)              | ~19.6%           | ~19.4%           | Underfitting                 |
| LDA (Raw)              | **97.96%**       | **98.32%**       | Severe overfitting           |
| MLR (with PCA)         | 91.03%           | 92.33%           | Good generalization          |
| **LDA (with PCA)**     | **85.1%**        | **86.95%**       | 🔥 **Best balance overall** |
| MLR (Kernel PCA)       | 26%              | 31.7%            | Underfitting                 |
| LDA (Kernel PCA)       | 32%              | 24.89%           | Underfitting                 |

📌 PCA combined with LDA yielded the **most balanced** and **generalizable** results.

---

## 🌐 Visualization

- PCA plots show separation of activities
- Scree plots illustrate explained variance by principal components
- UMAP & t-SNE used for exploratory visualizations

---

## 💡 Future Scope

- 🧠 Explore **advanced classifiers** like XGBoost or Deep Learning models (CNNs, LSTMs)
- 🔄 Real-time activity recognition on mobile devices
- 🧪 Experiment with **non-linear kernels** (Polynomial, Sigmoid)
- 👤 Personalize models for individual users’ motion patterns
- 🩺 Add dynamic activities for fitness or health monitoring use-cases

---

## 🧠 Skills Applied

### Technical
- PCA & Kernel PCA  
- Classification models: MLR, LDA  
- Model evaluation metrics  
- Visualization with biplots, scree plots, t-SNE/UMAP  

### Soft Skills
- Team collaboration on a structured workflow  
- Research and integration of multiple modeling approaches  
- Clear documentation and interpretability  
- Responsible use of open-source datasets

---

## 🤝 Acknowledgments

We would like to thank our faculty and the UCI Machine Learning Repository for making high-quality, real-world data available for academic use.

---

## 📬 Contact

For suggestions, collaborations, or discussion:
- **GitHub**: [@harshul27](https://github.com/harshul27)
- 📫 Reach out via issues or pull requests!

---

⭐ If this project inspired you, **star this repository** and help us grow as data science enthusiasts!

> “From complexity to clarity—dimensionality reduction helps us see what truly matters.”
