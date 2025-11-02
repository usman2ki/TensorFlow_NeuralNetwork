🚀 DEEP LEARNING BENCHMARK: FNN Architecture Optimization

Project Title: TensorFlow Neural Network Benchmark: Architecture & Activation Analysis

This repository documents a comprehensive study designed to break the performance barrier of simple hand-coded models and determine the optimal architecture for accurate house price prediction using TensorFlow/Keras.

🎯 THE CHALLENGE: Performance vs. Simplicity

The central goal was to escape the failure mode of basic Gradient Descent (as seen in prior assignments, resulting in negative $\text{R}^2$) and achieve industry-standard predictive accuracy ($\text{R}^2 > 0.8$).

The Benchmark Grid

We trained 54 unique Feedforward Neural Networks (FNNs) across a $6 \times 3 \times 3$ grid, holding the Adam optimizer fixed to isolate the impact of structure.

Factor

Test Cases

Optimal Configuration

Activation

LeakyReLU, ReLU, GELU, Swish, ELU, SELU

LeakyReLU

Depth

1, 2, 3 hidden layers

Depth 3

Width

8, 16, 32 neurons per layer

Width 32

🥇 KEY FINDINGS: Convergence Achieved

The benchmark successfully identified the high-complexity, optimized model required for convergence.

Metric

Optimal Finding

Result

Overall Best Model

3 Layers, 32 Neurons, LeakyReLU

$\mathbf{\text{R}^2 = 0.835}$

Convergence Success

Keras (A3) vs. NumPy (A2)

Keras achieved $\mathbf{0.835}$; NumPy achieved $\mathbf{-4.87}$

Error Reduction

Keras $\text{MSE}$ vs. NumPy $\text{MSE}$

Keras reduced prediction error by over 35X.

Conclusion on Optimization

The $\text{R}^2$ of $0.835$ confirms the successful application of the Adam optimizer and Early Stopping, proving that advanced tooling is non-negotiable for finding high-quality solutions, even when dealing with relatively simple datasets.

📂 REPOSITORY CONTENTS

File / Folder

Description

Feedforward_NeuralNetwork_Code.py

The Core Engine: Python script executing the entire 54-model dynamic benchmark.

feedforward_benchmark_results.csv

Raw Data Proof: Complete output of all 54 runs (Config, $\text{MSE}$, $\text{R}^2$, Runtime).



figures/

Visual Evidence: Contains all generated visualizations (Heatmaps, $\text{R}^2$ Bar Chart, Loss Curves).

house_prices_dataset.csv

The standardized 3-feature input dataset.

🚀 GETTING STARTED

Clone the Repository:

git clone [https://github.com/usman2ki/TensorFlow_Benchmark_NeuralNetwork.git](https://github.com/usman2ki/TensorFlow_Benchmark_NeuralNetwork.git)


Run the Benchmark: Execute the primary Python script (Feedforward_NeuralNetwork_Code.py) to reproduce the results.
