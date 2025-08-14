
# Supervised Learning Notes

Supervised learning is the most commonly used machine learning technique. About 99% of today's ML algorithms use supervised learning.

In supervised learning, we provide the computer with training data that includes both inputs (**x** - features) and outputs (**y** - labels). Given specific feature inputs, the algorithm learns to generate the corresponding output value.

## Types of Supervised Learning
1. **Regression**
2. **Classification**

### Regression
In regression, we create a mathematical relationship between features and labels.  
Example: Given a house size, predict its value.

### Classification
In classification, the computer creates clusters of data, which we can label to form categories.  
Examples: Image scanning to detect cancer, self-driving cars distinguishing between humans and vehicles.

---

## Linear Regression
Equation:  
**f(x) = wx + b**, where `w` is the weight and `b` is the bias.

**Cost Function (Mean Squared Error):**  
J(w,b) = (1/2N) Σ(predicted - actual)²

**Objective:** Minimize J(w,b).

---

## Gradient Descent
An iterative method to find the values of `w` and `b` that minimize the cost function.

**Learning Rate (α):** Controls the step size.  
- Small α → Slow convergence but stable  
- Large α → Faster but risk of divergence

---

## Multiple Linear Regression
When there are multiple features:  
y = w₁x₁ + w₂x₂ + ... + wₙxₙ + b

Vectorization is used for efficiency, especially on GPUs.

---

## Feature Scaling
Scaling ensures all features are in a comparable range to speed up gradient descent.

**Types:**
- Simple scaling (0–1 range)
- Mean normalization
- Z-score normalization

---

## Polynomial Regression
Used when the relationship is non-linear.  
Example: f(x) = w₁x + w₂x² + w₃x³

Features should be scaled before applying gradient descent.

---

## Logistic Regression (Classification)
Uses the **sigmoid function** to map predictions between 0 and 1.

**Loss Function:**
- If y=1: -log(f(x))
- If y=0: -log(1 - f(x))

---

## Overfitting & Underfitting
- **Underfitting:** High bias, poor accuracy.
- **Overfitting:** High variance, fits training data too well but fails on new data.

**Solutions for Overfitting:**
- Add more data
- Feature selection
- Regularization

---

## Regularization
Adds a penalty to large weights to avoid overfitting.  
Parameter λ controls the strength of regularization.

---

*These notes also reference accompanying Jupyter notebooks for hands-on implementation.*
