In this project, I created an AI model to land a spaceship on the moon, using a method called Deep Q-Learning, which combines Q-Learning with a Neural Network. Instead of giving the spaceship set rules, it will learn on its own by figuring out the best actions to take. The Neural Network will predict the best actions based on the environment, and sometimes it will try random actions to explore and learn more. This project will show how AI can learn and master the challenge of lunar landing of spacecrafts.

This project implements a Deep Q-Learning (DQN) agent to solve the Lunar Lander environment from Gymnasium (formerly OpenAI Gym).

1. Environment: The Lunar Lander environment simulates a spacecraft attempting to land on the lunar surface. The agent receives rewards for successful landing and penalties for crashing.
2. DQN Agent: The core of the project is a DQN agent. This agent uses a neural network to approximate the optimal action-value function (Q-function), which estimates the expected cumulative reward for taking a specific action in a given state.
3. Experience Replay: The agent utilizes experience replay to store and learn from past experiences. This involves saving transition states (state, action, reward, next state, done) in a memory buffer and randomly sampling batches for training the neural network.
4. Target Network: A separate target network is used to stabilize training. This network's parameters are periodically updated with the parameters of the main network.
5. Exploration-Exploitation: The agent balances exploration (trying new actions) and exploitation (choosing actions known to yield high rewards) using an epsilon-greedy strategy. Epsilon gradually decreases over time, shifting the agent's behavior from exploration to exploitation.
6. Training: The agent is trained over multiple episodes, gradually improving its performance by updating the neural network based on the observed rewards and the predicted Q-values.

Tech Stack:

1. Python: The primary programming language used for implementing the DQN agent and environment interactions.
2. Gymnasium: Provides the Lunar Lander environment and tools for reinforcement learning simulations.
3. PyTorch: A deep learning framework used for building and training the neural network.
4. NumPy: Used for numerical computations and array operations.
5. Collections: Provides data structures like deque for efficient experience replay.
6. Matplotlib and PIL: Used for visualizing the training progress and the agent's behavior.
