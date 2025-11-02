# 🚀 **Deep Learning Benchmark: FNN Architecture Optimization**

### 🧠 *TensorFlow Neural Network Benchmark: Architecture & Activation Analysis*

---

This repository presents a **comprehensive deep learning benchmark** exploring the relationship between **architecture complexity** and **predictive performance** in house price estimation using **TensorFlow/Keras**.

The project aims to **push beyond the limits** of simple hand-coded models and identify the **optimal Feedforward Neural Network (FNN)** configuration for achieving high accuracy with minimal computational overhead.

---

## 🎯 **The Challenge: Performance vs. Simplicity**

Previous models using basic Gradient Descent failed to converge properly — even producing **negative (R^2)** values 😬.
This study’s mission was to **break that limitation** and achieve **industry-level accuracy ((R^2 > 0.8))**, using smarter architectures and activations instead of brute force.

---

## 🧪 **Benchmark Grid: 54 Models Tested**

To ensure fairness, the **Adam optimizer** was held constant.
We systematically tested **54 unique FNN configurations** across a **6 × 3 × 3 grid**, varying activations, depth, and width.

| **Factor**     | **Test Cases**                          | **Optimal Configuration** |
| -------------- | --------------------------------------- | ------------------------- |
| **Activation** | LeakyReLU, ReLU, GELU, Swish, ELU, SELU | 🏆 **LeakyReLU**          |
| **Depth**      | 1, 2, 3 hidden layers                   | 🏗️ **3 Layers**          |
| **Width**      | 8, 16, 32 neurons per layer             | ⚙️ **32 Neurons**         |

---

## 🥇 **Key Findings: Convergence Achieved 📈**

After extensive testing, the benchmark successfully identified the **optimal FNN structure** that achieved stable convergence and superior accuracy.

| **Metric**                 | **Finding**                     | **Result**                                                     |
| -------------------------- | ------------------------------- | -------------------------------------------------------------- |
| **Overall Best Model**     | 3 Layers, 32 Neurons, LeakyReLU | 💡 **(R^2 = 0.835)** *(Highly Accurate)*                       |
| **Convergence Comparison** | Keras (A3) vs NumPy (A2)        | ✅ **Keras: 0.835**, ❌ NumPy: -4.87                             |
| **Error Reduction**        | MSE (Keras vs NumPy)            | 🔽 **35× lower error with Keras**                              |
| **Conclusion**             | Adam + Early Stopping           | 🧩 *Essential for optimal convergence even in simple datasets* |

---

## 📂 **Repository Contents**

| **File / Folder**                      | **Description**                                                |
| -------------------------------------- | -------------------------------------------------------------- |
| 🧩 `Feedforward_NeuralNetwork_Code.py` | Core engine that executes the entire 54-model benchmark.       |
| 📊 `feedforward_benchmark_results.csv` | Raw output of all 54 runs — configs, MSE, (R^2), runtime, etc. |
| 📈 `figures/`                          | Heatmaps, bar charts, and loss curves for visual analysis.     |
| 🏠 `house_prices_dataset.csv`          | The standardized dataset used for all experiments.             |

---

## ⚙️ **Getting Started**

### 🔗 Clone the Repository

```bash
git clone https://github.com/usman2ki/TensorFlow_Benchmark_NeuralNetwork.git
```

### 🧰 Install Dependencies

Ensure you have the following packages installed:

```bash
pip install tensorflow keras numpy scikit-learn matplotlib
```

### ▶️ Run the Benchmark

Execute the main benchmark script:

```bash
python Feedforward_NeuralNetwork_Code.py
```

This will reproduce all 54 model runs and generate:

* Evaluation metrics (MSE, (R^2))
* Heatmaps & plots inside `/figures`
* Full log file: `feedforward_benchmark_results.csv`

---

## 🧩 **Highlights**

* ✅ 54 Model Experiments
* ⚙️ Automated Architecture Search
* 🧠 LeakyReLU Dominance Verified
* 📉 35× MSE Improvement
* 📈 Achieved (R^2 = 0.835)

---

> 💬 *“Even simple datasets deserve sophisticated engineering.”*
> — *Muhammad Usman*

---
