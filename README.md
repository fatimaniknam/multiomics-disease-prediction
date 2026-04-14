# Multi-Omics Disease Resistance Prediction in Common Bean (Phaseolus vulgaris)

This project explores how integrating multi-omics data improves the prediction of complex traits using machine learning. A simulated dataset was used to model disease resistance in common bean, combining genomic (SNP) and transcriptomic (gene expression) information.

---

## 📌 Project Objective

To evaluate the predictive power of different biological data layers and investigate whether combining them improves model performance.

---

## 🧬 Data Simulation

Synthetic data were generated to mimic a biological system:

- **500 samples**
- **1000 SNP markers (genomic data)**
- **200 gene expression features (transcriptomic data)**

The phenotype (**disease resistance**) was constructed based on the expression levels of a subset of genes, reflecting a biologically realistic assumption that gene activity drives observable traits.

---

## ⚙️ Methodology

### 🔹 Feature Sets
- **SNP-only** (genomic data)
- **Expression-only** (transcriptomic data)
- **Multi-omics** (combined dataset)

---

### 🔹 Models
- **Ridge Regression** (baseline linear model)
- **XGBoost** (tree-based model for nonlinear patterns)

---

### 🔹 Evaluation Strategy
- Train/Test split
- **5-fold Cross-Validation** for robustness

---

### 🔹 Model Interpretability
- **SHAP (SHapley Additive Explanations)** was used to quantify feature contributions and interpret model predictions.

---

## 📊 Key Results

- **Gene expression strongly outperformed SNP data** in predicting disease resistance
- Adding unfiltered SNP data **reduced performance due to noise**
- Multi-omics integration requires **feature selection or dimensionality reduction**
- XGBoost handled high-dimensional data more effectively than linear models

---

## 🔍 Biological Interpretation

- Transcriptomic features were the **primary drivers of prediction**
- Most SNP features contributed **minimal predictive signal**
- Higher gene expression levels were associated with **increased disease resistance**

---

## 🧠 Key Insights

- Gene expression is **closer to phenotype** than raw genetic variation
- More features do not necessarily improve model performance
- High-dimensional data can introduce noise and degrade predictive accuracy
- Proper feature selection is critical in multi-omics modeling

---

## 🚀 Future Work

- Integrate biologically realistic simulation using **AlphaSimR**
- Apply the pipeline to real genomic datasets
- Explore advanced feature selection and dimensionality reduction methods
- Extend the framework to time-series or stress-response data

---

## 🛠️ Tools & Libraries

- Python (NumPy, Pandas)
- scikit-learn
- XGBoost
- SHAP
- Matplotlib

---

## 👩‍🔬 Author

Developed as part of a transition into computational genomics and machine learning, with a focus on applying multi-omics approaches to plant breeding and complex trait prediction.
