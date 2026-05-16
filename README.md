# Assignment-Module-5_Part-1_Parul-Mital
1     # Part 1: Neural Network Fundamentals and Training Behavior Analysis
2     
3     ## 📌 Problem Statement
4     The objective of this project is to build and analyze a neural network model for predicting customer churn using a structured dataset. The focus is not only on model performance, but also on understanding how neural networks learn through forward propagation, backpropagation, and parameter updates.
5     
6     ---
7     
8     ## 📊 Dataset Understanding
9     The dataset consists of customer-related information such as demographic details, usage patterns, and service interactions.
10     
11     - Total records: ~1000+
12     - Features include both:
13       - Categorical (region, plan type, contract type, payment method)
14       - Numerical (tenure, monthly charges, data usage, etc.)
15     - Target variable: `churn`
16       - 1 → customer churned
17       - 0 → customer retained
18     
19     No major missing values were observed. The dataset was reasonably balanced.
20     
21     ---
22     
23     ## ⚙️ Data Preprocessing
24     
25     The following preprocessing steps were performed:
26     
27     - Removed `customer_id` as it is not useful for prediction
28     - Converted categorical variables using one-hot encoding
29     - Scaled numerical features using StandardScaler
30     - Split dataset into training (80%) and testing (20%)
31     
32     ---
33     
34     ## 🧠 Neural Network Model
35     
36     A feed-forward neural network was implemented using TensorFlow/Keras:
37     
38     - Input Layer: Based on number of features
39     - Hidden Layer 1: 64 neurons (ReLU activation)
40     - Hidden Layer 2: 32 neurons (ReLU activation)
41     - Output Layer: 1 neuron (Sigmoid activation)
42     
43     ### ✅ Key Concepts Applied
44     
45     - **Forward Pass**: Input features are passed through layers to generate predictions
46     - **Backpropagation**: Errors are propagated backward to update weights
47     - **Activation Functions**:
48       - ReLU for hidden layers
49       - Sigmoid for output
50     - **Loss Function**: Binary Crossentropy
51     - **Optimizer**: Adam
52     
53     ---
54     
55     ## 📈 Training and Evaluation
56     
57     The model was trained for 25–35 epochs with batch size variations.
58     
59     ### Results:
60     - Training accuracy: ~85–90%
61     - Test accuracy: ~85–90%
62     
63     ### Evaluation:
64     - Confusion matrix used to assess classification performance
65     - Loss and accuracy curves plotted to monitor training behavior
66     
67     ### Observations:
68     - Model converged steadily during training
69     - Slight overfitting observed after multiple epochs
70     - Feature scaling significantly improved performance
71     
72     ---
73     
74     ## 🔬 Hyperparameter Experiments
75     
76     Several experiments were conducted by modifying:
77     
78     - Number of neurons
79     - Learning rate
80     - Batch size
81     - Number of epochs
82     
83     ### Summary of Experiments:
84     
85     | Experiment        | Changes Made           | Result |
86     |------------------|----------------------|--------|
87     | Baseline         | Default parameters    | Good performance |
88     | Experiment 1     | Reduced neurons       | Slight drop in accuracy |
89     | Experiment 2     | Higher learning rate  | Faster but unstable training |
90     | Experiment 3     | Larger batch size     | Slower convergence |
91     
92     Results are stored in `/results/model_comparison.csv`.
93     
94     ---
95     
96     ## 🔍 Final Reflection
97     
98     ### Role of Weights and Biases
99     Weights determine the importance of each feature, while biases help shift the activation function. Together, they allow the model to learn complex relationships.
100     
101     ### Importance of Activation Function
102     Activation functions introduce non-linearity, enabling the model to capture complex patterns in data.
103     
104     ### Learning Rate Impact
105     - High learning rate can cause instability
106     - Low learning rate leads to slow convergence
107     
108     ### Overfitting vs Underfitting
109     The model showed signs of mild overfitting, as training performance improved faster than validation performance.
110     
111     ---
112     
113     ## ✅ Conclusion
114     
115     The neural network successfully captured patterns in customer behaviour affecting churn. This project helped in understanding the core principles of neural network training, including forward pass, loss computation, and backpropagation.
120     

