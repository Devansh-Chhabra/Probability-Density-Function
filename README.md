## Probability Density Function Estimation Using Parameterized Non-Linear Model 📊

## 📌 Overview
The objective is to analyze the `NO2` feature from the **India Air Quality Data** dataset and perform a non-linear transformation. After transformation, the parameters of a Gaussian-like PDF are estimated using **Maximum Likelihood Estimation (MLE)**

---

## 🛠️ Mathematical Model

### Step 1: Data Transformation
Each value of the feature $x$ (NO2) is transformed into $z$ using the following function:
$$z = T_r(x) = x + a_r \sin(b_r x)$$

### Step 2: PDF Parameter Estimation
The goal is to learn the parameters $\lambda$, $\mu$, and $c$ for the predicted probability $\hat{p}(z)$:
$$\hat{p}(z) = c \cdot e^{-\lambda(z-\mu)^2}$$

By treating this as a **Gaussian Distribution**, we calculate:
* **$\mu$ (Mean):** Average of the transformed variable $z$.
* **$\lambda$:** Calculated as $\frac{1}{2\sigma^2}$ (Precision).
* **$c$:** The normalization constant $\frac{1}{\sqrt{2\pi\sigma^2}}$.

---

## 🚀 Getting Started

### Prerequisites
The following Python stack is required:
* `numpy`
* `pandas`
* `matplotlib`

### Dataset
The raw data is sourced from the **India Air Quality Data** archive on Kaggle.
* **Feature used**: `no2`

---

## 📈 Results
The implementation successfully outputs:
* **$\mu$**: The central tendency of the transformed air quality data.
* **$\lambda$**: The spread/variance factor of the distribution.
* **$c$**: The peak scaling factor for the probability density.

---

## 👨‍💻 Author

**Devansh Chhabra**  
📧 Email: [devanshchhabr@gmail.com](mailto:devanshchhabr@gmail.com)  

---
