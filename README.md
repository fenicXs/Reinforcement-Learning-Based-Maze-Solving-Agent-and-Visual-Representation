# Reinforcement-Learning-Based-Maze-Solving-Agent-and-Visual-Representation

This project implements a **Reinforcement Learning-based Turtle Graphics Agent** capable of navigating a grid maze and reaching designated goals. The agent uses a value-based learning approach to optimize its policy, visually representing its learning process and decision-making on a graphical interface.

---

## Features
- **Turtle Graphics Representation**:
  - A visually appealing grid layout created using Python's `turtle` module.
  - Dynamic agent movement with clear markers for start, goal, walls, and traps.
- **Custom Reinforcement Learning Logic**:
  - Implements reward-based navigation.
  - Supports exploration (with an adjustable exploration rate) and exploitation for learning.
- **Interactive Visualization**:
  - Real-time agent movement and value updates across the grid cells.
  - Displays learned values for each state in the maze.
- **Deterministic Environment**:
  - Predictable outcomes for each action (up, down, left, right), ensuring stable learning dynamics.

---

## How It Works
1. **Grid Setup**:
   - A 3x4 maze grid is created, with specific regions designated as:
     - **Start Point**: `(-225, -225)`
     - **Win Zone**: `(225, 75)` (reward: +1)
     - **Lose Zone**: `(225, -75)` (reward: -1)
     - **Wall**: `(-75, -75)` (blocked area)
   - Other regions provide neutral rewards of 0.
   
2. **Agent Design**:
   - The agent starts at the designated **start point**.
   - It takes actions to move up, down, left, or right while avoiding walls and learning optimal paths to the **Win Zone**.

3. **Learning Mechanism**:
   - **Q-value Update**:
     - Rewards are back-propagated after each episode.
     - Learning rate (`lr`) ensures incremental updates.
   - **Exploration vs Exploitation**:
     - Exploration rate (`exp_rate`) balances between trying new paths and leveraging known information.

4. **Visualization**:
   - State values are displayed on the grid for each episode.
   - The agent's path and decisions are rendered live.

---

## Requirements
- Python 3.8+
- Libraries:
  - `numpy`
  - Python `turtle` module (standard library)

---

## Future Improvements
- Support stochastic environments to simulate unpredictable outcomes.
- Implement additional algorithms like Q-Learning or SARSA.
- Expand to larger and more complex maze designs.
