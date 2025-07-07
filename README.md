# Advanced-Neural-Network-Q-Learning-project-
Advanced Neural Network (Q-Learning project)
# Q-Learning in GridWorld 🧠➡️🗺️

This project implements **Q-learning** in a 4×4 GridWorld environment using Python and visualizes the learned policy.

---

## 📌 Problem Description

- The agent starts at position **(0, 0)**
- The goal is at **(3, 3)** and gives **+10 reward**
- Each step gives **–1 reward**
- Moving outside the grid results in staying in place and getting –1
- Episode ends at goal or after 50 steps

---

## 🏗️ Components

### ✅ Part 1: Environment Setup
- `GridWorld` class with `reset()` and `step()` methods.

### ✅ Part 2: Q-Learning Algorithm
- Parameters: 
  - Learning Rate `α`
  - Discount Factor `γ`
  - Epsilon-Greedy `ε` Exploration
- Q-table: shape `(16, 4)` for each state and action.

### ✅ Part 3: Policy Visualization
- Print final policy using arrows:
  - ↑: up, →: right, ↓: down, ←: left
- Animate learned agent path

### ✅ Part 4: Experimentation
- Compare 3 configurations:
  1. α=0.1, γ=0.9, ε=1.0→0.01
  2. α=0.5, γ=0.95, ε=1.0→0.1
  3. α=0.9, γ=0.99, ε=0.5 (constant)

---

## 🧪 Results

| Case | Path                                              | Steps | Reward Calculation | Total Reward |
|------|---------------------------------------------------|--------|---------------------|----------------|
| 1    | (0,0)→(1,0)→(2,0)→(2,1)→(2,2)→(2,3)→(3,3)         | 6      | –1×6 + 10           | +4             |
| 2    | (0,0)→(1,0)→(1,1)→(2,1)→(2,2)→(2,3)→(3,3)         | 6      | –1×6 + 10           | +4             |
| 3    | (0,0)→(1,0)→(1,1)→(2,1)→(2,2)→(3,2)→(3,3)         | 6      | –1×6 + 10           | +4             |

---

## 🎥 Visuals

- Each case is visualized using an animation on the same grid with different colors
- Agent starts at red dot and moves toward green goal

---

## 💻 Run it on Google Colab

[🔗 Open in Google Colab](https://colab.research.google.com/drive/1dVG-FGrAj2eQULDeKmih3Br43sKy0ssL)

---

## 🔧 Dependencies

```bash
pip install matplotlib numpy

