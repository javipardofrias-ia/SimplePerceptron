
# 🤖 Perceptron — Implementation and Training for Logic Functions

## 📘 Description

This project implements a single-layer perceptron from scratch in Python using the NumPy library. Its main goal is to train the perceptron to solve linearly separable classification problems, specifically the logical AND function, and to demonstrate its limitations with the non-linearly separable XOR function.

The notebook follows an educational and practical approach, guiding the user through the definition of the activation function, the perceptron's logic, and the training process based on the Hebbian learning rule. The process is visualized through plots of total error per epoch to understand the model's convergence.

## 🛠️ Requirements

Ensure you have Python 3.8+ and the following libraries installed:

```bash
pip install numpy pandas matplotlib
```

Libraries used:

  * `numpy` – for matrix and vector operations.
  * `pandas` – for structuring and saving results to a CSV file.
  * `matplotlib.pyplot` – for visualizing the total error per epoch.

## 📊 Dataset

The project does not use an external dataset. Instead, it generates the inputs and expected outputs for the logical AND and XOR functions.

  * **Generated Data**:
      * **AND**: `[[0, 0], [0, 1], [1, 0], [1, 1]]` with expected outputs `[0, 0, 0, 1]`.
      * **XOR**: `[[0, 0], [0, 1], [1, 0], [1, 1]]` with expected outputs `[0, 1, 1, 0]`.

This approach provides full control over the input data and facilitates a clear demonstration of the perceptron's capabilities and limitations.

## 🧠 Perceptron Configuration

The perceptron is configured with the following default parameters in the training function:

| Hyperparameter | Description | Value |
|---|---|---|
| `tasa_aprendizaje` (Learning Rate) | A factor that determines the magnitude of weight changes. | 0.4 |
| `epocas` (Epochs) | The number of complete iterations over the training dataset. | 10 |

The notebook also defines a step activation function, which returns 1 if the weighted sum of inputs is greater than or equal to a threshold, and 0 otherwise.

## 🧬 Weight Initialization & Training

The perceptron's weights (including the bias) are initialized with random values within the range `[-1, 1]`.

The training is performed using the **Hebbian learning rule with error correction**:

1.  A random input is selected.
2.  The perceptron's output is calculated and compared to the expected output to get the error.
3.  The weights are adjusted based on the error and the learning rate. If the error is positive, the weights are increased; if negative, they are decreased.
4.  This process is repeated for a defined number of epochs, allowing the perceptron to learn to correctly classify the inputs (if the problem is linearly separable).

## 📊 Visualizations and Results

The notebook generates the following outputs:

  * A line plot showing the total error per epoch for the AND function, illustrating the convergence of the training.
  * The training results for the AND and XOR functions are printed to the console, showing how the weights change in each iteration and the error.
  * A CSV file (`L2P1-Perceptron.csv`) that combines the results of both logical function trainings, saving the initial and final weights, inputs, outputs, and errors.

## 🚀 How to Run

1.  Download or clone the repository.
2.  Open the notebook:
    ```bash
    jupyter notebook L2P1-Perceptron.ipynb
    ```
3.  Run the cells sequentially to:
      * Load the necessary libraries.
      * Train the perceptron for the AND function.
      * Train the perceptron for the XOR function.
      * Save the results to a CSV file.
      * Visualize the results for the AND function.

## 📌 Applications & Extensions

  * Serves as an excellent educational tool for understanding the fundamentals of neural networks and supervised learning.
  * Can be extended to solve other linearly separable classification problems.
  * The activation function can be modified to explore different model behaviors.

