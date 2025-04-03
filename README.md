
# 🚗 Reinforcement Learning Recitation – Deep Learning Variants

This project explores the comparative performance of multiple deep reinforcement learning algorithms—**Deep Q-Network (DQN)**, **Proximal Policy Optimization (PPO)**, **Soft Actor-Critic (SAC)**, and **Advantage Actor-Critic (A2C)**—in an autonomous driving simulation environment called `highway-fast-v0`.

## 🔍 Objective

The goal is to train agents to drive safely and efficiently in a simulated highway environment, avoiding collisions while maximizing rewards. This work evaluates and compares agent behaviors, stability, and performance across different algorithms.

## 🛠️ Technologies Used

- **Reinforcement Learning Framework**: Stable-Baselines3
- **Environment**: `highway-fast-v0` (`highway-env`)
- **Notebook Platform**: Google Colab
- **Visualization**: TensorBoard
- **Language**: Python

## 📦 Algorithms Implemented

### 1. Deep Q-Network (DQN)
- Value-based approach using experience replay and target networks.
- Learning rate: `0.001`, Batch size: `64`
- Challenges: Instability, low reward, high variance.

### 2. Proximal Policy Optimization (PPO)
- Policy-gradient method with clipped surrogate objective.
- Learning rate: `0.0003`, Clip range: `0.2`
- Strengths: High stability and consistent performance.

### 3. Soft Actor-Critic (SAC) *(Bonus)*
- Off-policy actor-critic algorithm with entropy maximization.
- Achieved highest reward with minimal variance.
- Well-suited for continuous action spaces.

### 4. Advantage Actor-Critic (A2C) *(Bonus)*
- Policy-gradient method using both actor and critic networks.
- Moderate performance; better than DQN but less optimal than PPO/SAC.

## 🧪 Environment Configuration

- **Simulation**: `highway-fast-v0`
- **Duration**: 40 seconds per episode
- **Traffic**: 20 vehicles
- **Reward**: Speed (20–40), Safety, Lane adherence

## 📊 Key Results

| Algorithm | Avg. Reward | Avg. Episode Length | Stability | Crash Rate |
|-----------|-------------|---------------------|-----------|------------|
| DQN       | 15.67 ± 8.40| 21.6s               | Low       | High       |
| PPO       | 28.27 ± 1.16| 40s (max)           | High      | Low        |
| SAC       | 43.99 ± 0.64| 40s (max)           | Very High | Very Low   |
| A2C       | 25.45 ± 2.31| 38.7s               | Moderate  | Moderate   |

## 📽️ Visual Outputs

- **Training Videos**: Showcase agent behaviors under different policies.
- **TensorBoard Logs**: Track training performance, episode lengths, and reward curves.

## 📁 File Structure

- `sb3_highway_dqn.ipynb`: Implementation notebook (Google Colab compatible)
- `models/`: Trained model directories (if available)
- `report.pdf`: Full project report with results and comparison
- `README.md`: You're here!

## 🔗 Resources & Tools

- [highway-env GitHub](https://github.com/eleurent/highway-env)
- [Stable-Baselines3 Docs](https://stable-baselines3.readthedocs.io/)
- [TensorBoard](https://www.tensorflow.org/tensorboard)

## 📌 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/rl-highway-recitation.git
   cd rl-highway-recitation
   ```

2. Open the notebook on Google Colab:
   [Click to Open](https://colab.research.google.com/drive/17MgwOrJFYCKeG9xNb4f6wJUzVGjS0vdM?usp=sharing)

3. Run each cell in order to:
   - Set up the environment
   - Train each RL model
   - Visualize results via TensorBoard

## 📌 Citation

Project by **Anusha Shiva Kumar**, for Human-Robot Interaction coursework at the University of Pittsburgh.

