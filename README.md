# Deep Learning and Reinforcement Learning  

## Overview
This repository contains all six programs for the Deep Learning and Reinforcement Learning (DLRL).   
The main focus of the modifications was to improve code structure, training performance, and visualization while keeping the original logic intact.  
All programs were tested successfully in Google Colab and standard Python environments.

---

## Program 1 – AlexNet Model

**File:**  
  alexnet.py
  
**Modifications:**
- Converted the Sequential model into a subclass of `tf.keras.Model` for better flexibility.  
- Added Batch Normalization after convolutional layers to improve training stability.  
- Used He Normal weight initialization suitable for ReLU activations.  
- Added configurable parameters like `input_shape`, `num_classes`, and `dropout_rate`.  
- Adjusted input size for smaller datasets and added a clean `main` block for testing.

**Reason:**  
To make the model easier to adapt for different datasets and improve training efficiency and generalization.

https://colab.research.google.com/drive/1OhhDUb43Vy-Nr2LaIykdxp03DA8jg79N
---

## Program 2 – Q-Learning (Deep Reinforcement Learning)

**File:**  
  deep_reinforcement_learning.py

**Modifications:**
- Introduced an epsilon-greedy approach for exploration and exploitation balance.  
- Added a learning rate (`alpha`) parameter to control Q-value updates.  
- Used the proper Q-learning update equation.  
- Organized the logic into smaller reusable functions.  
- Improved reward tracking and visualization with a simple training graph.

**Reason:**  
To make the Q-learning algorithm more realistic, mathematically correct, and easy to understand while maintaining modularity.

https://colab.research.google.com/drive/1FzPVZBUWWBjFXH7BSSjZvBmGPebA_sd5
---

## Program 3 – LSTM Time Series Forecasting

**File:**  
  lstm.py

**Modifications:**
- Automatically loads the airline passenger dataset from a public URL instead of using a local file.  
- Added a reusable function to create time-step sequences.  
- Increased model depth with two LSTM layers and included dropout for regularization.  
- Added loss curve visualization and future forecasting (next 12 months).  
- Displayed RMSE scores for training and testing data.

**Reason:**  
To make the code self-contained, improve prediction accuracy, and include visualization and future trend forecasting.

https://colab.research.google.com/drive/1zZyJMGXJJGgrp4jv9cQx-JuJsfD5fCTq

---

## Program 4 – CNN Model (Face Mask Detection)

**File:**  
  mask_withoutmask.py

**Modifications:**
- Replaced the Cats vs Dogs dataset with a real-world Face Mask Detection dataset (downloaded automatically).  
- Implemented transfer learning using the MobileNetV2 pretrained model.  
- Added image augmentation such as rotation, zoom, brightness, and flipping.  
- Added fine-tuning of the last 40 layers for improved performance.  
- Included dropout, global average pooling, and detailed accuracy/loss plots.  
- Added functionality to test user-uploaded images interactively in Colab.

**Reason:**  
To demonstrate a real-world CNN application using transfer learning and data augmentation for improved generalization.

https://colab.research.google.com/drive/1mU50FxcUd1GTnI0C4JIRDhC1jI9Kcp_g
---

## Program 5 – RNN Text Generation

**File:**  
  rnn.py

**Modifications:**
- Increased sequence length to give the model more context.  
- Expanded RNN layer size to 128 neurons and switched to `tanh` activation.  
- Added a function to generate text with controlled randomness for more natural results.  
- Extended training epochs for better accuracy.  
- Tested with two different starting phrases to compare generated text.

**Reason:**  
To improve text coherence, reduce repetition, and make the generator produce more human-like sequences.

https://colab.research.google.com/drive/1f1AdrVUcuxB1Pe0bXhP5I6OgbmOPpwLy

---

## Program 6 – Tic Tac Toe (Reinforcement Learning)

**File:**  
  tictactoe.py

**Modifications:**
- Fixed initialization errors (`_init_` → `__init__`) and main function naming issues.  
- Corrected player logic, reward distribution, and winner detection.  
- Simplified reward function and ensured fair outcomes for both players.  
- Improved board display and human input validation.  
- Added saving and loading of learned policies using safe file handling.  
- Included an option to replay the game with the trained computer agent.

**Reason:**  
To make the game fully functional, bug-free, and interactive while maintaining reinforcement learning behavior.

https://colab.research.google.com/drive/1eh2ikSkm3_eFi2RxoyolzRUQwBre8SMc

