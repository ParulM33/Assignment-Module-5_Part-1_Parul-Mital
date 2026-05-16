# Part 1: Neural Network Fundamentals and Training Behavior Analysis

 

## Problem Statement

 

The objective of this project is to build and analyze a neural network model using a structured dataset to predict customer churn. The focus is on understanding how neural networks learn through forward pass, loss calculation, and backpropagation.

 

---

 

## Dataset Understanding

 

The dataset contains customer-related information such as demographic details, subscription plans, and usage behavior.

 

- It includes both categorical and numerical features 

- Categorical features: region, plan type, contract type, payment method 

- Numerical features: tenure, monthly charges, and usage metrics 

- Target variable: **churn**

  - 1 → customer churned 

  - 0 → customer retained 

 

No significant missing values were found in the dataset.

 

---

 

## Data Preprocessing

 

The following steps were performed:

 

- Removed the `customer_id` column as it is only an identifier 

- Converted categorical variables into numerical format using one-hot encoding 

- Scaled numerical features using **StandardScaler** 

- Split the dataset into training (80%) and testing (20%) sets 

 

---

 

## Neural Network Model

 

A feed-forward neural network was implemented using TensorFlow/Keras.

 

### Model Architecture

 

- Input Layer: based on number of features 

- Hidden Layer 1: 64 neurons with ReLU activation 

- Hidden Layer 2: 32 neurons with ReLU activation 

- Output Layer: 1 neuron with Sigmoid activation 

 

### Configuration

 

- Loss Function: Binary Crossentropy 

- Optimizer: Adam 

- Activation Functions:

  - ReLU (hidden layers) 

  - Sigmoid (output layer) 

 

---

 

## Training and Evaluation

 

The model was trained for **25 epochs** with a batch size of **32**.

 

- Training and validation loss were monitored 

- Loss curve was plotted to understand model learning behavior 

- The model achieved good accuracy on the test dataset 

 

---

 

## Hyperparameter Experimentation

 

An experiment was conducted by modifying the number of epochs.

 

- Baseline: 25 epochs 

- Experiment: 35 epochs 

 

### Observation

 

Increasing the number of epochs improved learning initially, but after a point, validation loss increased, indicating possible overfitting.

 

---

 

## Final Reflection

 

Weights and biases help the model learn patterns by adjusting the importance of input features.

 

Activation functions introduce non-linearity, allowing the neural network to capture complex relationships.

 

A high learning rate can make training unstable, while a low learning rate slows down the learning process.

 

The model showed slight overfitting when trained for more epochs.

 

---

 

## Conclusion

 

The neural network successfully captured patterns related to customer churn. This project helped in understanding fundamental concepts such as forward propagation, backpropagation, and the impact of hyperparameters on model performance.

 

---

 

## Repository Structure
part-1-neural-network-analysis/ │ ├── README.md ├── notebook.ipynb ├── requirements.txt └── results/ ├── model_comparison.csv └── evaluation_outputs.png
