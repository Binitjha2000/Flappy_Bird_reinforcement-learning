# Flappy_Bird_reinforcement-learning

#Deep reinforcement learning agent to play the Flappy Bird game using Q-learning. Below is a point-wise description of the code:

# Imports and Dependencies:

The code imports necessary libraries including pygame for game rendering, random for random operations, numpy for numerical operations, and pickle for saving/loading Q-values.
# Constants and Hyperparameters:

Defines several constants such as the screen dimensions, frames per second (FPS), gravity, and bird-related parameters.
Hyperparameters for Q-learning include learning rate (alpha), discount factor (gamma), and exploration-exploitation balance (epsilon).
Game Environment Setup:

Initializes the pygame environment and sets up the game window, background, bird, and pipe images.
Defines the Bird, Pipe, and Base classes to encapsulate the behavior of the bird, the pipes, and the base (ground).
State Representation:

Represents the state as a tuple containing information about the bird’s vertical position, velocity, and the position of the next pipe relative to the bird.
# Action Space:

The action space consists of two possible actions: flap or not flap (0 for no flap, 1 for flap).
# Q-Learning Algorithm:

Initializes a Q-table (Q) to store the Q-values for different state-action pairs.
The Q-learning update rule is applied during the game to update the Q-values based on the reward received after taking an action.
# Reward Function:

The reward function gives a positive reward for passing a pipe and a negative reward for colliding with a pipe or the ground.
# Game Loop and Training:

The main game loop handles the movement of the bird, the pipes, and checks for collisions.
During training, the agent selects actions based on an epsilon-greedy policy and updates the Q-table accordingly.
The game loop also handles rendering the game on the screen during training.
Saving and Loading Q-values:

Q-values are saved to a file at regular intervals, and the code provides functionality to load previously saved Q-values to resume training.
# Training Process:

The training process runs for a predefined number of episodes, with the performance of the agent improving as it learns to avoid pipes more effectively.
# Game Visualization:

The code includes visualization of the game, which can be toggled on or off during training for performance reasons.
# Final Evaluation:

After training, the agent's performance is evaluated by running the game without exploration (using the greedy policy).
