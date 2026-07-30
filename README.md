# MNIST Handwritten Digit Classification: Model Comparison

This project compares the performance of classical machine learning algorithms and a Feedforward Artificial Neural Network (ANN) on the MNIST handwritten digit classification dataset.

MNIST contains grayscale images of handwritten digits from **0 to 9**. Each image has a resolution of **28 × 28 pixels** and is represented as **784 input features** after flattening.

## Models Implemented

* **Logistic Regression** using Scikit-learn
* **Random Forest Classifier** using Scikit-learn
* **Feedforward Artificial Neural Network (ANN)** using PyTorch

## ANN Architecture

The Feedforward ANN consists of fully connected layers with ReLU activation functions:

```text
Input Layer: 784 neurons
        ↓
Hidden Layer: 128 neurons + ReLU
        ↓
Hidden Layer: 64 neurons + ReLU
        ↓
Output Layer: 10 neurons
```

The ANN uses:

* **Cross-Entropy Loss** for multiclass classification
* **Backpropagation** to calculate gradients
* **Adam Optimizer** to update model weights
* **25 training epochs**

The training loss decreased consistently from **2.3** in Epoch 1 to **0.8598** in Epoch 25, indicating that the model was learning during training.

## Model Performance

| Model               |                           Accuracy |  Precision |     Recall |   F1-Score |
| ------------------- | ---------------------------------: | ---------: | ---------: | ---------: |
| Logistic Regression |                             92% |     92% |     92% |     92% |
| Random Forest       |                         **97%** | **97%** | **97%** | **97%** |
| Feedforward ANN     | Evaluated using Cross-Entropy Loss |          — |          — |          — |

## Evaluation Metrics

The models were evaluated using:

* **Accuracy** — percentage of correctly classified images
* **Weighted Precision** — reliability of the model’s predictions across all digit classes
* **Weighted Recall** — ability to correctly identify images from each digit class
* **Weighted F1-Score** — balance between precision and recall

## Results

Random Forest achieved the strongest reported classification performance, with an accuracy of **96.96%**. Logistic Regression achieved an accuracy of **92.57%**, providing a strong baseline despite being a linear model.

The Feedforward ANN demonstrated successful learning through a consistent reduction in training loss over 25 epochs. Its performance was evaluated using Cross-Entropy Loss.

## Technologies Used

* Python
* PyTorch
* Scikit-learn

## Project Objective

The objective of this project is to compare traditional machine learning approaches with a neural-network-based approach for handwritten digit classification and to understand the complete machine learning workflow, including:

1. Data preparation
2. Image flattening
3. Model training
4. Loss calculation
5. Backpropagation
6. Weight optimization
7. Model evaluation
8. Performance comparison

