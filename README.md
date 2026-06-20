# Reinforcement Learning: Tic-Tac-Toe Agent

A Python implementation of a tabular Q-Learning agent trained to play Tic-Tac-Toe. This project demonstrates the application of the Bellman equation, epsilon-decreasing strategies, and state-space optimization.

It features both a graphical interface which uses `tkinter` library; and a console interface. The user can choose the interface and other parameters in the `main` function at the end of the notebook.
Other interesting statistics are also shown.
### Game Interface (tkinter)
<p align="center">
<img width="493" height="601" alt="image" src="https://github.com/user-attachments/assets/9938be99-3ce0-4fc5-b3ed-9ca9d4465f34" />
</p>
  
### Example of training evolution
<p align="center">
<img width="1054" height="660" alt="image" src="https://github.com/user-attachments/assets/d021b678-be14-4e10-907e-73ebfe9b30d7" />
</p>

### Context
This project was originally developed for *Artificial Intelligence I* subject at UCM. While this documentation is in English, the internal code comments and Notebook explanations are in **Spanish**.

### Project Overview
The goal of this project was to create an agent capable of achieving **100% invincibility** (win or draw) against any opponent, including a Minimax algorithm (which is invincible). 

### Key Features

#### 1. Q-Learning Implementation
* **Dynamic Learning Rate ($\alpha$)**: Implemented a decay formula based on state visits.
* **Sparse rewards**: The agent learns effectively receiving rewards only at the end of the game (win/defeat/draw).
* **Backtracking Updates**: Speeds up convergence by updating the Q-table in reverse order after each episode.
* **Epsilon-greedy-decreasing policy**: A policy that chooses between exploration or exploitation as training progresses.

#### 2. Optimization & Generalization
* **Symmetry Reduction:** I implemented a normalization algorithm that maps rotations and reflections of the board to a canonical state. This reduced the state space from thousands of combinations to just **~620 unique states**, drastically reducing training time.
* **Relative Perception:** The agent learns to play relative to the current turn, allowing the same policy to be used for both Player 'X' and Player 'O'.

#### 3. Validation
* **Minimax Benchmark:** A Minimax algorithm was developed to train the agent and test it.
* **Monte Carlo Test:** A statistical validation function proves how well the agent was trained, using the previous Minimax algorithm.

### Tech Stack
* **Language:** Python
* **Libraries:** `matplotlib` (visualization), `tkinter` (GUI), `random`.

### How to Run
1.  Clone the repository and install the required dependencies in its folder (requirements.txt).
2.  Open the notebook `tictactoe_qlearning_agent.ipynb`.
3.  Go to the `main` function at the end of the notebook.
4.  Configure the specified parameters.
5.  Run all cells.
