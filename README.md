TensorFlow Neural Network Benchmark: Architecture & Activation Analysis

This repository contains the complete project for a deep learning benchmark study on house price regression, focusing on Feedforward Neural Network (FNN) architecture optimization using TensorFlow/Keras.

🎯 Project Objective

The goal of this study was to empirically determine the optimal configuration for a regression task by systematically testing the effect of three critical hyperparameters on model performance ($\text{R}^2$):

Activation Function (e.g., LeakyReLU, ReLU, GELU)

Network Depth (Number of hidden layers)

Network Width (Neurons per layer)

📈 Key Findings & Optimal Configuration

The benchmark involved training 54 unique models ($6 \text{ Activations} \times 3 \text{ Depths} \times 3 \text{ Widths}$) under fixed optimization (Adam optimizer).

Metric

Optimal Finding

Result

Overall Best Model

$\text{D}=3, \text{W}=32$ with LeakyReLU

$\mathbf{\text{R}^2 = 0.835}$

Best Architecture

Depth 3, Width 32

Maximum complexity was required for stable and accurate convergence.

Comparative $\text{R}^2$

Keras (A3) vs. NumPy (A2)

Keras achieved $\mathbf{0.835}$; NumPy achieved $\mathbf{-4.87}$.

Conclusion on Optimization

The success of this project hinged on using the Adam optimizer and Early Stopping in Keras, which enabled the model to reduce the prediction error ($\text{MSE}$) by over 35 times compared to the high loss incurred by simpler, hand-coded Gradient Descent implementations.

📂 Repository Contents

File / Folder

Description

Feedforward_NeuralNetwork_Code.py

The main Python script that executes the entire 54-model benchmark, including dynamic model creation, training, and metrics logging.

feedforward_benchmark_results.csv

Raw output data for all 54 model runs, containing configuration, runtime, Test $\text{MSE}$, and Test $\text{R}^2$ for detailed analysis.

figures/

Directory containing all generated visualizations: Heatmaps (Depth vs. Width MSE) and the $\text{R}^2$ Bar Chart comparing activation performance.

house_prices_dataset.csv

The standardized 3-feature input dataset used across the entire project lifecycle.

🚀 Getting Started

Clone the Repository:

git clone [https://github.com/usman2ki/TensorFlow_Benchmark_NeuralNetwork.git](https://github.com/usman2ki/TensorFlow_Benchmark_NeuralNetwork.git)


Install Dependencies: Ensure you have Python, TensorFlow, Keras, NumPy, pandas, and scikit-learn installed.

Run the Benchmark: Execute the primary Python script (Feedforward_NeuralNetwork_Code.py) to reproduce the results.
