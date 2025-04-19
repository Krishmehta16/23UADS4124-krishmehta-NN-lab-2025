Project Objective
To build a basic Recurrent Neural Network (RNN) model using PyTorch to predict the next value in a sine wave. This shows how RNNs can learn from sequences over time.

Model Overview
What the model does:
The RNN takes in a sequence of sine wave values and tries to predict what comes next.

Architecture Details:

Input Size: 1
Hidden Size: 50
Output Size: 1
Layers: 1 RNN layer followed by a linear layer
This simple setup helps the model learn the wave’s pattern over time.

Code Breakdown
1. Data Generation:
Sine wave is created using NumPy (np.sin) across the range 0 to 100.
1000 data points are generated.

2. Preprocessing:
Data is scaled between 0 and 1 using MinMaxScaler.
Sequences of a fixed length (default = 20) are created to use as input for the RNN.

3. Model Definition:

The model is a custom class (RNNPredictor) with:
An RNN layer to process the sequence.
A Linear layer to output the prediction.

4. Training:

Loss function: Mean Squared Error (MSE)
Optimizer: Adam, learning rate = 0.01
Trained for 100 epochs
Loss is printed every 10 epochs

Model Evaluation
The model is tested on 20% of the data (held-out test set).
Predictions are compared to the actual sine wave.
A plot shows how well the model follows the real pattern.

Performance Results:

Training Loss: Goes down steadily, meaning the model is learning.
Test Loss: Final MSE is printed.
Plot: Predicted vs. actual values show the model can follow the sine wave trend.

Comments & Suggestions
Great for learning how RNNs work.
Works well on clean, synthetic data.

To Improve:
Try LSTM or GRU for better memory of longer sequences.
Add early stopping to avoid overtraining.
Tune hyperparameters like learning rate, sequence length, or hidden size.

Limitations
May not perform well on noisy or real-world data.
Basic RNNs tend to forget older inputs — LSTMs or GRUs handle this better.
Fixed settings — no parameter tuning or stopping condition.
