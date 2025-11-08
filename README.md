# 🌸 Feature Engineering and Data Preprocessing – Iris Flower Dataset

## 📘 Overview
This project demonstrates **feature engineering and data preprocessing** using the **Iris Flower Dataset** from the **UCI Machine Learning Repository**.  
The goal is to prepare the dataset for a **classification problem**, where we predict the **species of an Iris flower** based on its sepal and petal dimensions.

---

## 📂 Dataset Information
- **Dataset Name:** Iris Flower Dataset  
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/machine-learning-databases/iris/iris.data)  
- **Type:** Classification Problem  
- **Target Variable:** `species` (Setosa, Versicolor, Virginica)  
- **Number of Instances:** 150  
- **Number of Attributes:** 5 (4 features + 1 target)

### Key Features

| Feature | Description |
|----------|--------------|
| `sepal_length` | Length of the sepal (cm) |
| `sepal_width` | Width of the sepal (cm) |
| `petal_length` | Length of the petal (cm) |
| `petal_width` | Width of the petal (cm) |
| `species` | Target: Iris species (Setosa, Versicolor, Virginica) |

---

## ⚙️ Steps Performed

1. **Data Loading & Exploration**
   - Loaded the dataset from UCI.
   - Checked data types, shape, and summary statistics.
   - Verified that no missing values exist.

2. **Missing Value Handling**
   - Used `SimpleImputer(strategy='mean')` for demonstration, ensuring robustness even if future data has gaps.

3. **Encoding Categorical Variables**
   - Encoded the `species` column using `LabelEncoder` (Setosa = 0, Versicolor = 1, Virginica = 2).

4. **Feature Scaling**
   - Applied both **StandardScaler** and **MinMaxScaler** to normalize all numeric columns for model compatibility.

5. **Feature Extraction (PCA)**
   - Performed **Principal Component Analysis (PCA)** with two components.  
   - Captured over **95% of the total variance**.

6. **Feature Selection**
   - Used:
     - **VarianceThreshold (0.01)** to remove low-variance features.  
     - **SelectKBest (f_classif)** to identify top three predictive features.

7. **Visualization**
   - Generated **correlation heatmaps** and **scatterplots** to study relationships and separability among classes.

---

## 📊 Summary of Transformations

| Step | Technique | Impact |
|------|------------|--------|
| Missing Data | Mean Imputation | Dataset becomes complete |
| Encoding | LabelEncoder | Converts categorical target to numeric |
| Scaling | StandardScaler / MinMaxScaler | Normalizes feature range |
| PCA | 2 Components | Simplifies dataset while keeping >95% variance |
| Feature Selection | SelectKBest | Highlights most influential predictors |
| Visualization | Heatmap, Scatter | Improves interpretability |

**Top Features Identified:**  
`petal_length`, `petal_width`, `sepal_length`

---

## 🧠 Observations
- **Petal measurements** are the most discriminative features among the three species.  
- **PCA** shows clear class separation in 2-D space.  
- After preprocessing, data is fully numeric, scaled, and model-ready for classification algorithms such as Logistic Regression or SVM.

---

## ⚖️ Ethical Considerations
- This dataset involves **no personal or sensitive information**, hence minimal ethical risk.  
- However, in any real-world dataset, always ensure:
  - Transparent reporting of preprocessing steps.  
  - No bias in sampling or feature selection.  
  - Reproducible and fair modeling practices.

---

## 🧩 Tools and Libraries Used
- **Python 3**  
- **Pandas**, **NumPy**  
- **Matplotlib**, **Seaborn**  
- **Scikit-learn** (PCA, StandardScaler, SelectKBest, LabelEncoder)

---

## 📁 Files in Repository

| File Name | Description |
|------------|-------------|
| `Feature_Engineering_Iris.ipynb` | Jupyter Notebook with full feature engineering workflow |
| `Feature_Engineering_Report.pdf` | 1–2 page summary of the experiment |
| `README.md` | Documentation and ethical notes |

---

## 👨‍💻 How to Run
   https://colab.research.google.com/drive/14oJbXqDfYv98VjfET--OewkzsvDDh_ut?usp=sharing
