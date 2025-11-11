# 🎵 BopBot: Predicting Song Popularity with MLP


BopBot is a machine learning project that predicts a song’s popularity using a Multi-Layer Perceptron (MLP). By analyzing patterns in musical attributes, BopBot aims to uncover the key elements behind a hit song—offering insights for songwriters, producers, and streaming platforms alike.

## 👥 Contributors

- **Lia Mathews** — Project Lead, Model Design, and Experimentation  
- **Andrea Ayon** — Data Preprocessing and Analysis  
- **Jillian Russell** — Evaluation Metrics and Visualization  
- **Emily Freeman** — Documentation and Testing

## Overview

BopBot uses a regression-based neural network model to estimate a song’s popularity score based on its features. The project experiments with various model parameters to balance accuracy, computational efficiency, and generalizability.

Our final model achieved:

Mean Absolute Error (MAE): 10.45

Mean Squared Error (MSE): 158.84

Prediction Confidence Interval: 53.9–55.6 (95% confidence)

While the model avoids extreme prediction errors, it may slightly underestimate highly popular or unpopular songs—demonstrating a strong but cautious predictive pattern.

## Experiment Details

### Activation Function

We used the Softplus activation function for smooth, differentiable transitions across all input values. Compared to ReLU, Softplus helped maintain stable gradient updates during training, improving performance on our dataset.

### Network Architecture

After testing multiple configurations, we found that two hidden layers offered the best performance balance:

Hidden Layer 1: 12 neurons

Hidden Layer 2: 8 neurons

Adding more layers or neurons increased overfitting and slowed down training without improving accuracy.

### Loss Function

We chose Mean Squared Error (MSE), which is well-suited for regression tasks and provided consistent optimization feedback.

### Batch Size

Through experimentation, a batch size of 64 produced the best trade-off between training stability and speed.

### Epochs

Training typically converged around 200 epochs. With early stopping no longer necessary, we fixed the epoch count to 200 for efficiency.
