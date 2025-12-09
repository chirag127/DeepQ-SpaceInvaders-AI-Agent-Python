<div align="center">
  <img src="https://raw.githubusercontent.com/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python/main/assets/deepq_logo.svg" alt="DeepQ Logo" width="150" height="150"/>
  <h1>DeepQ-SpaceInvaders-AI-Agent-Python</h1>
  <p><h3>The Apex Reinforcement Learning Engine for Atari Environments.</h3></p>

  <!-- Badges Section -->
  <p>
    <a href="https://github.com/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python/actions/workflows/ci.yml">
      <img src="https://img.shields.io/github/actions/workflow/status/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python/ci.yml?branch=main&style=flat-square&label=CI%20Pipeline" alt="CI Status"/>
    </a>
    <a href="https://codecov.io/gh/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python">
      <img src="https://img.shields.io/codecov/c/github/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python?style=flat-square&label=Coverage" alt="Code Coverage"/>
    </a>
    <img src="https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python&logoColor=white" alt="Python Version"/>
    <img src="https://img.shields.io/badge/RL%20Stack-DQN%20%7C%20PyTorch%20%7C%20Gym-orange?style=flat-square&logo=pytorch" alt="Tech Stack"/>
    <a href="https://github.com/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python/blob/main/LICENSE">
      <img src="https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey?style=flat-square" alt="License"/>
    </a>
    <a href="https://github.com/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python/stargazers">
      <img src="https://img.shields.io/github/stars/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python?style=flat-square&label=Stars&color=yellow" alt="GitHub Stars"/>
    </a>
  </p>
  <!-- Social Proof -->
  <a href="https://github.com/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python">
    <img alt="Star this Repo" src="https://img.shields.io/badge/Star%20this%20Repo-⭐-black.svg?style=for-the-badge"/>
  </a>
</div>

## 🚀 Overview: Apex Deep Q-Network Agent

**DeepQ-SpaceInvaders-AI-Agent-Python** is an elite, high-performance command-line interface (CLI) application implementing the Deep Q-Network (DQN) algorithm to autonomously achieve expert-level performance in classic Atari games, specifically leveraging the OpenAI Gym environment for `SpaceInvaders-v4`. This project embodies robust Python engineering principles combined with advanced Reinforcement Learning strategies.

The architecture is designed for modular experimentation, allowing rapid iteration on hyperparameter tuning, model architectures (e.g., Dueling DQN, Double DQN), and replay buffer strategies, ensuring the highest standards of reproducible research in game AI.

---

## 🏗️ Architecture & Structure

This repository employs a **Modular Monolith** structure, separating the core RL components (Agent, Model, Environment Manager) from the CLI interface and configuration.

mermaid
graph TD
    A[Start: main.py / run.py] --> B(CLI Interface: Click);
    B --> C(Config Layer: Hydra/YAML);
    C --> D{RL Core Engine};
    D --> E(DQN Agent: Selection Strategy);
    D --> F(Replay Buffer: Experience Storage);
    D --> G(Deep Q-Model: PyTorch CNN);
    D --> H(Environment Manager: Gym API);
    E --> G;
    F --> G;
    G --> I(Experiment Tracker: TensorBoard/WandB);


### Table of Contents

1.  [🚀 Overview](#-overview-apex-deep-q-network-agent)
2.  [🏗️ Architecture & Structure](#️-architecture--structure)
3.  [🤖 AI Agent Directives](#-ai-agent-directives-master-control-program)
4.  [🛠️ Quick Start & Setup](#️-quick-start--setup)
5.  [🧠 Training the Agent](#-training-the-agent)
6.  [📄 License](#-license)

---

## 🤖 AI Agent Directives (Master Control Program)

<details>
<summary><strong>📐 APEX Architectural Mandates for RL/AI Systems</strong></summary>

The following directives define the engineering standards for the **DeepQ-SpaceInvaders-AI-Agent-Python** project. Future code contributions and refactoring must align with these standards.

### 1. Technology Stack Definition
*   **Core Language:** Python 3.10+ (Static Typing enforced via MyPy).
*   **Package Management:** **uv** is the mandated tool for dependency resolution, installation, and virtual environment management, ensuring speed and deterministic builds.
*   **Deep Learning Framework:** **PyTorch** for constructing and managing the Convolutional Neural Network (CNN) used by the DQN agent.
*   **Code Quality:** **Ruff** (Linter/Formatter). Zero Ruff errors and full formatting compliance are non-negotiable before merging.
*   **Environment:** OpenAI Gym / Gymnasium for standardized Atari interaction.

### 2. Architectural Patterns (RL Focus)
*   **Decoupling:** Strict separation between the `Agent` (which handles policy, exploration, and learning loops) and the `Model` (the PyTorch neural network definition).
*   **Experience Replay Buffer:** The buffer implementation must utilize efficient data structures (e.g., collections deque or NumPy arrays) and be isolated as a service (`experience_replay.py`).
*   **Principle of Delayed Updates:** Adhere to standard DQN practice of maintaining two networks—the current Q-Network and a target Q-Network—updated synchronously or asynchronously based on configuration.
*   **Clean Code Principles:** **SOLID, DRY, YAGNI.** Specifically: Single Responsibility Principle (SRP) mandates that configuration handling, environment stepping, and Q-value calculation reside in distinct classes/methods.

### 3. Verification & Execution Commands
*   **Setup:** Use `uv` for environment management.
    bash
uv venv
source .venv/bin/activate
uv pip install -r requirements.txt # Or use pyproject.toml
    
*   **Code Audit (LINT & FORMAT):**
    bash
ruff check . --fix
ruff format .
    
*   **Unit & Integration Testing (TEST):** All logic (agent updates, buffer manipulation) must be covered.
    bash
pytest --cov=deepq --verbose
    
*   **Agent Execution (RUN):**
    bash
python run.py --env SpaceInvaders-v4 --mode train --episodes 1000 --model-path ./models/dqn_model.pth
    
</details>

---

## 🛠️ Quick Start & Setup

### Prerequisites
*   Python 3.10 or higher.
*   The `uv` package manager (recommended for speed).

### 1. Environment Initialization
Clone the repository and initialize the Python environment using `uv`:

bash
# Clone the repository
git clone https://github.com/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python.git
cd DeepQ-SpaceInvaders-AI-Agent-Python

# Create and activate the virtual environment using uv
uv venv
source .venv/bin/activate

# Install dependencies
uv pip install -r requirements.txt


### 2. Running Verification Tests
Ensure the codebase is functioning correctly before training:

bash
# Run the complete test suite
pytest


---

## 🧠 Training the Agent

The core training loop is controlled via the `run.py` CLI script. Use `--help` to see all available hyperparameters (learning rate, discount factor, epsilon decay, etc.).

### Example: Start Training on Space Invaders

This command initiates the DQN agent training process, storing model checkpoints and logging metrics to TensorBoard:

bash
python run.py train \
    --env "SpaceInvaders-v4" \
    --steps 5000000 \
    --gamma 0.99 \
    --batch-size 32 \
    --log-dir ./runs/space_invaders_run_1


### Monitoring Progress
Training results are logged using TensorBoard. Run the following command in a separate terminal to monitor performance metrics (reward average, loss, epsilon):

bash
tensorboard --logdir=./runs
# Open http://localhost:6006 in your browser


---

## 🤝 Contributing

We welcome contributions that adhere to the **Apex Agent Directives**. Please see the official [CONTRIBUTING.md](.github/CONTRIBUTING.md) for detailed guidelines on setting up your environment, running tests, and submitting Pull Requests.

---

## 📄 License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International Public License (CC BY-NC 4.0)**. See the [LICENSE](LICENSE) file for full details.