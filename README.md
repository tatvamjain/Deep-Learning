# Deep Learning Lab Experiments 

## Overview

This repository contains implementations of core **neural network and machine learning algorithms from scratch using NumPy**.
The goal of these experiments is to understand the **fundamental working principles of perceptrons, logistic regression, linear regression, and multilayer neural networks with backpropagation** without relying on high-level deep learning frameworks.

All models are implemented using **basic mathematical operations and gradient descent**.

---

# Experiment 1

## Perceptron for Logic Gates

### Objective

Design and implement a **single layer perceptron** to learn basic logical gates.

### Logic Gates Implemented

* AND
* OR
* NAND
* NOR
* XOR

### Key Concepts

* Weighted sum
* Step activation function
* Decision boundary
* Linear separability

### Perceptron Equation

```text
y = step(w1x1 + w2x2 + b)
```

Where

* `x1, x2` = inputs
* `w1, w2` = weights
* `b` = bias

### Results

The perceptron correctly learns:

| Gate | Output  |
| ---- | ------- |
| AND  | Correct |
| OR   | Correct |
| NAND | Correct |
| NOR  | Correct |

XOR required a **multi-layer approach** because XOR is **not linearly separable**.

---

# Experiment 2

## Logistic Regression using Single Layer Perceptron

### Objective

Implement **binary classification using logistic regression** with a single layer perceptron.

### Dataset

Glass Identification Dataset
Source: Kaggle / UCI Machine Learning Repository

Dataset features include chemical properties such as:

* Sodium
* Magnesium
* Aluminum
* Silicon
* Potassium
* Calcium
* Barium
* Iron

### Model

Logistic Regression equation:

```text
z = XW + b
p = sigmoid(z)
```

Sigmoid activation:

```text
σ(z) = 1 / (1 + e^(-z))
```

### Loss Function

Binary Cross Entropy:

```text
Loss = -[y log(p) + (1-y) log(1-p)]
```

### Optimization

Weights updated using **gradient descent**.

### Evaluation

* Train-Test Split
* Classification Accuracy

Typical performance:

```text
Accuracy ≈ 83.72%
```

---

# Experiment 3

## Multiple Linear Regression using Perceptron

### Objective

Implement **multiple linear regression using perceptron learning with gradient descent**.

### Dataset

Multiple Linear Regression Dataset
Source: Kaggle

Features include:

* Age
* Experience

Target variable:

* Income / Salary

### Model

Linear Regression Equation:

```text
ŷ = w1x1 + w2x2 + ... + wn xn + b
```

### Loss Function

Mean Squared Error (MSE):

```text
MSE = (1/n) Σ (y - ŷ)^2
```

### Training

Gradient descent updates the weights iteratively to minimize the loss.

### Evaluation Metric

* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)

---

# Experiment 4

## Multilayer Perceptron with Backpropagation (Regression)

### Objective

Implement a **Multilayer Perceptron (MLP)** using backpropagation to predict the **age of abalone**.

### Dataset

Abalone Dataset
Source: UCI Machine Learning Repository

Input features include:

* Length
* Diameter
* Height
* Whole Weight
* Shucked Weight
* Viscera Weight
* Shell Weight

Target variable:

* Rings (used to estimate age)

### Neural Network Architecture

```text
Input Layer
     ↓
Hidden Layer (ReLU)
     ↓
Output Layer (Linear)
```

### Activation Function

ReLU:

```text
ReLU(x) = max(0, x)
```

### Loss Function

Mean Squared Error:

```text
MSE = (1/n) Σ (y - ŷ)^2
```

### Performance

Example results:

```text
Test MSE ≈ 4.3
```

---

# Experiment 5

## Multilayer Perceptron with Backpropagation (Digit Classification)

### Objective

Build a **multilayer neural network from scratch** to classify handwritten digits.

### Dataset

Digits Dataset (from sklearn)

Dataset details:

* Total samples: 1797
* Features: 64
* Classes: 10 (digits 0–9)

### Neural Network Architecture

```text
Input Layer (64)
      ↓
Hidden Layer (128 neurons) – ReLU
      ↓
Output Layer (10 neurons) – Softmax
```

### Activation Functions

ReLU:

```text
ReLU(x) = max(0, x)
```

Softmax:

```text
softmax(x_i) = e^x_i / Σ e^x_j
```

### Loss Function

Categorical Cross Entropy:

```text
Loss = - Σ y log(y_pred)
```

### Training

* Forward propagation
* Backpropagation
* Gradient descent optimization

### Model Performance

Typical results:

```text
Accuracy ≈ 94%
```

---

# Technologies Used

* Python
* NumPy
* Pandas
* Scikit-learn (dataset utilities and evaluation)

---

# Key Learning Outcomes

These experiments demonstrate:

* Implementation of **perceptron models**
* Understanding **activation functions**
* Implementation of **logistic regression from scratch**
* Implementation of **linear regression using gradient descent**
* Building **multilayer neural networks**
* Understanding **backpropagation**
* Implementing **softmax classification**
* Evaluating models using **accuracy, MSE, and RMSE**

---

# Conclusion

This project provides hands-on understanding of how neural networks operate internally.
By implementing algorithms from scratch, the experiments illustrate how **weights, biases, activation functions, and gradient descent interact to enable machine learning models to learn from data**.

---

# Author
**Tatvam Jain\
102303484**
