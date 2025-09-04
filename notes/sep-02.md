---
type: note
layout: note
title: Lecture 2
date: 09/02/25
status: n/a
professor: Mamoun
labels:
hidden: true
---

### Artificial Intelligence — Gradient Descent

Linear regression starts with a simple model:
$$
y = a + bx
$$

In multiple dimensions:
$$
\hat{y} = m_b + m_1x_1 + m_2x_2 + \dots
$$

---

### Loss Function (Linear Regression)

We measure how far off predictions are using the **sum of squared residuals**:

$$
L = \sum_{i=1}^{n} \big( y_i - \hat{y}_i \big)^2
$$

- $y_i$ = actual value  
- $\hat{y}_i$ = predicted value  
- Residual = difference between prediction and truth  

#### Squaring ensures all errors are positive and penalizes large mistakes more.

---

### Gradient Descent

To minimize the loss, we update the weights step by step:

$$
\theta := \theta - \alpha \frac{\partial L}{\partial \theta}
$$

- $\alpha$ = learning rate (step size)  
- $\frac{\partial L}{\partial \theta}$ = slope of the loss function (gradient)  

---

### Logistic Regression

When the output should be a probability (classification), we use the **sigmoid function**:

$$
f(x) = \frac{1}{1 + e^{-x}}
$$

This maps any input to a value between 0 and 1.  
- Close to 0 → likely "No"  
- Close to 1 → likely "Yes"

---

### Logistic Loss

Instead of squared error, Logistic Regression uses **log loss** (cross-entropy):

$$
L = - \sum_{i=1}^n \Big[ y_i \log(\hat{y}_i) + (1 - y_i) \log(1 - \hat{y}_i) \Big]
$$

- If $y=1$, loss is small when $\hat{y}$ is close to 1.  
- If $y=0$, loss is small when $\hat{y}$ is close to 0.  

---

### Example Connections

Linear Regression:
$$
\text{Predicted Height} = \text{intercept} + \text{slope} \cdot \text{weight}
$$

Logistic Regression:
$$
P(\text{Pass Exam} | \text{Hours Studied}) = \frac{1}{1 + e^{-(b_0 + b_1 \cdot \text{hours})}}
$$
