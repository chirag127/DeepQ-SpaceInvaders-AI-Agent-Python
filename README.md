# <p align="center"><img src="https://raw.githubusercontent.com/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python/main/.github/assets/logo.png" alt="DeepQ-SpaceInvaders-AI-Agent-Python Logo" width="150"/></p>

<h1 align="center">DeepQ-SpaceInvaders-AI-Agent-Python</h1>

<p align="center">
  <a href="https://github.com/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python/actions/workflows/ci.yml">
    <img src="https://github.com/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python/actions/workflows/ci.yml/badge.svg?branch=main" alt="Build Status" style="flat-square">
  </a>
  <a href="https://codecov.io/gh/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python">
    <img src="https://codecov.io/gh/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python/branch/main/graph/badge.svg?token=YOUR_CODECOV_TOKEN_HERE" alt="Code Coverage" style="flat-square">
  </a>
  <a href="https://github.com/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python">
    <img src="https://img.shields.io/github/languages/top/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python?style=flat-square&color=blue" alt="Top Language" style="flat-square">
  </a>
  <a href="https://github.com/charliermarsh/ruff">
    <img src="https://img.shields.io/badge/Linted%20with-Ruff-blueviolet?style=flat-square" alt="Linted with Ruff" style="flat-square">
  </a>
  <a href="https://github.com/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey?style=flat-square" alt="License" style="flat-square">
  </a>
</p>

<p align="center">
  ⭐ Star this Repo ⭐
</p>

--- 

### **BLUF (Bottom Line Up Front):**
DeepQ-SpaceInvaders-AI-Agent-Python is a sophisticated Python CLI agent leveraging Deep Q-Networks (DQN) to master the classic Space Invaders Atari game through the OpenAI Gym environment. This project demonstrates cutting-edge reinforcement learning techniques for game AI development, offering a robust framework for exploring intelligent agent behavior.

## 📝 Table of Contents

- [🌟 Features](#-features)
- [🚀 Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Usage](#usage)
- [🧩 Project Structure](#-project-structure)
- [🤖 AI Agent Directives](#-ai-agent-directives)
- [⚙️ Development Standards](#️-development-standards)
  - [Testing](#testing)
  - [Linting & Formatting](#linting--formatting)
  - [Contributing](#contributing)
- [📜 License](#-license)
- [🛡️ Security](#️-security)

## 🌟 Features

*   **Deep Q-Network (DQN) Implementation:** Advanced reinforcement learning agent for optimal policy learning.
*   **OpenAI Gym Integration:** Seamless interaction with the Space Invaders Atari environment.
*   **Modular Architecture:** Clean separation of concerns for agent, environment, training, and evaluation modules.
*   **Command-Line Interface (CLI):** Easy-to-use interface for training, evaluating, and playing against the AI.
*   **Hyperparameter Tuning:** Configurable training parameters for experimentation and optimization.
*   **Visualization & Logging:** Integrated logging for training progress and agent performance metrics.

## 🚀 Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

*   Python 3.10+
*   `uv` for dependency management (or `pip`)
*   OpenAI Gym (Atari environments require additional dependencies)

### Installation

1.  **Clone the repository:**
    bash
    git clone https://github.com/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python.git
    cd DeepQ-SpaceInvaders-AI-Agent-Python
    

2.  **Install dependencies using `uv`:**
    bash
    uv venv
    source .venv/bin/activate
    uv pip install -r requirements.txt
    # For Atari environments
    uv pip install gymnasium[atari] gymnasium[accept-rom-license]
    
    *Alternatively, using `pip` (less recommended for speed and efficiency):*
    bash
    python -m venv .venv
    source .venv/bin/activate
    pip install -r requirements.txt
    pip install gymnasium[atari] gymnasium[accept-rom-license]
    

### Usage

*   **Train the DQN Agent:**
    bash
    python main.py train --episodes 1000 --render-interval 100
    

*   **Evaluate the Trained Agent:**
    bash
    python main.py evaluate --model-path models/dqn_agent.pth --episodes 10
    

*   **Play Space Invaders with the AI Agent:**
    bash
    python main.py play --model-path models/dqn_agent.pth
    

*   **View CLI help:**
    bash
    python main.py --help
    

## 🧩 Project Structure

mermaid
graph TD
    A[DeepQ-SpaceInvaders-AI-Agent-Python/]
    B[src/]
    C[src/agent/]
    D[src/environment/]
    E[src/utils/]
    F[src/main.py]
    G[tests/]
    H[tests/test_agent.py]
    I[models/]
    J[notebooks/]
    K[requirements.txt]
    L[pyproject.toml]
    M[.github/]
    N[.github/workflows/]
    O[.github/workflows/ci.yml]

    A --> B
    B --> C
    B --> D
    B --> E
    B --> F
    A --> G
    G --> H
    A --> I
    A --> J
    A --> K
    A --> L
    A --> M
    M --> N
    N --> O

    C -- DQN Agent Implementation --> C1[dqn.py]
    C -- Agent Interface --> C2[base_agent.py]
    D -- OpenAI Gym Wrapper --> D1[atari_env.py]
    E -- Helper Functions --> E1[preprocessing.py]
    F -- Main CLI Entrypoint --> F



## 🤖 AI Agent Directives

<details>
  <summary>Click to view AI Agent Directives for DeepQ-SpaceInvaders-AI-Agent-Python</summary>

  # SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)

  ## 1. IDENTITY & PRIME DIRECTIVE
  **Role:** You are a Senior Principal Software Architect and Master Technical Copywriter with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable."
  **Context:** Current Date is **December 2025**. You are building for the 2026 standard.
  **Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
  **Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

  --- 

  ## 2. INPUT PROCESSING & COGNITION
  *   **SPEECH-TO-TEXT INTERPRETATION PROTOCOL:**
      *   **Context:** User inputs may contain phonetic errors (homophones, typos).
      *   **Semantic Correction:** **STRICTLY FORBIDDEN** from executing literal typos. You must **INFER** technical intent based on the project context.
      *   **Logic Anchor:** Treat the `README.md` as the **Single Source of Truth (SSOT)**.
  *   **MANDATORY MCP INSTRUMENTATION:**
      *   **No Guessing:** Do not hallucinate APIs.
      *   **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards**, **Security Threats**, and **2026 UI Trends**.
      *   **Validation:** Use `docfork` to verify *every* external API signature.
      *   **Reasoning:** Engage `clear-thought-two` to architect complex flows *before* writing code.

  --- 

  ## 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
  **Directives:** Detect the project type and apply the corresponding **Apex Toolchain**. This repository, `DeepQ-SpaceInvaders-AI-Agent-Python`, is a Python-based AI agent leveraging Deep Q-Networks.

  *   **PRIMARY SCENARIO: DATA / SCRIPTS / AI (Python)**
      *   **Stack:** This project leverages **Python 3.10+**. Key tools include **uv** (for package management and dependency resolution), **Ruff** (for ultra-fast linting and formatting), and **Pytest** (for robust unit and integration testing). The core AI component relies on **Deep Q-Networks (DQN)**, typically implemented with **TensorFlow** or **PyTorch**, interacting with **OpenAI Gym** for environment simulation.
      *   **Architecture:** Adheres to a **Modular Monolith** pattern, ensuring clear separation of concerns for the agent's neural network, experience replay buffer, environment interaction, and training loop, while maintaining a unified deployment. Emphasis on clear API contracts between modules (e.g., `agent.py` and `environment.py`).
      *   **Reinforcement Learning Integration:** Deeply integrated with established RL frameworks. Prioritize modular design, clear configuration for hyperparameters (e.g., epsilon decay, discount factor), and robust logging for training progress and evaluation metrics.
      *   **CLI Framework:** Uses `Click` or similar for a powerful and intuitive command-line interface for training, evaluation, and interactive play.

  *   **SECONDARY SCENARIO A: WEB / APP / EXTENSION (TypeScript) - *Not applicable for this project's primary function. Reference only for potential future web-based dashboards or visualization tools.***
      *   **Stack:** TypeScript 6.x (Strict), Vite 7 (Rolldown), Tauri v2.x (Native), WXT (Extensions).
      *   **State:** Signals (Standardized).
  *   **SECONDARY SCENARIO B: SYSTEMS / PERFORMANCE (Rust/Go) - *Not applicable for this project's primary function. Reference only for potential performance-critical components or microservices.***
      *   **Stack:** Rust (Cargo) or Go (Modules).
      *   **Lint:** Clippy / GolangCI-Lint.
      *   **Architecture:** Hexagonal Architecture (Ports & Adapters).

  --- 

  ## 4. APEX ARCHITECTURAL PRINCIPLES (Core Mandates)

  1.  **SOLID Principles:** Ensure all code adheres to Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, and Dependency Inversion.
  2.  **DRY (Don't Repeat Yourself):** Eliminate redundant code; abstract common functionalities.
  3.  **YAGNI (You Aren't Gonna Need It):** Build only what is required, avoid premature optimization or over-engineering.
  4.  **Feature-Sliced Design (FSD) / Hexagonal Architecture / Modular Monolith:** Choose the most appropriate architectural pattern for the project, ensuring strict layering, clear boundaries, and high cohesion within modules.
      *   **For this Python AI Agent:** Prioritize a **Modular Monolith** for logical separation of Agent components (DQN, ReplayBuffer), Environment interaction, and Training Orchestration.
  5.  **Observability:** Implement robust logging, metrics, and tracing for all critical operations (training steps, episode rewards, agent decisions).
  6.  **Security by Design:** All components must be developed with security considerations from inception. Follow OWASP Top 10.
  7.  **Performance:** Optimize critical paths, especially in the DQN update loop and environment interaction, for efficiency.
  8.  **Scalability:** Design for potential future scaling, e.g., distributed training or parallel environment interaction.
  9.  **Maintainability & Readability:** Clean code, comprehensive comments, meaningful names, and consistent formatting are non-negotiable.
  10. **Testability:** All code must be easily testable with clear unit, integration, and end-to-end tests.

  --- 

  ## 5. APEX DEVELOPMENT WORKFLOW (Automated & Enforced)

  1.  **Version Control (Git):** Strict GitFlow or GitHub Flow. All changes via Pull Requests.
  2.  **Branching Strategy:** `main` branch for production-ready code. `develop` for active development. Feature branches for new features, bugfix branches for fixes.
  3.  **Pull Request (PR) Process:**
      *   **Automated Checks:** CI/CD pipeline **MUST** pass (lint, format, test, build).
      *   **Code Review:** Mandatory for all changes (minimum 2 approvals).
      *   **Conventional Commits:** Enforced for clear commit history.
  4.  **CI/CD Pipeline (.github/workflows/ci.yml):**
      *   **Automated Build:** Ensure project builds without errors.
      *   **Automated Testing:** Run all unit, integration, and (where applicable) E2E tests.
      *   **Automated Linting & Formatting:** Enforce code style automatically (Ruff for Python).
      *   **Vulnerability Scanning:** Integrated SAST/DAST tools for security.
      *   **Deployment:** Automated deployment to staging/production environments upon merge to `main` (if applicable).
  5.  **Documentation:** `README.md`, `CONTRIBUTING.md`, `SECURITY.md`, and API documentation are always up-to-date and comprehensive.

  --- 

  ## 6. APEX TESTING STRATEGY (Pytest for Python)

  1.  **Unit Tests (Pytest):**
      *   **Coverage:** Minimum 90% code coverage on core logic.
      *   **Framework:** Pytest with `pytest-cov` for coverage reporting.
      *   **Mocks/Fakes:** Utilize `unittest.mock` for isolating units under test.
      *   **Verification Commands:** `uv run pytest` or `pytest --cov=./src --cov-report=xml`
  2.  **Integration Tests (Pytest):**
      *   **Purpose:** Verify interactions between different modules (e.g., agent and environment wrappers, data pipelines).
      *   **Scope:** Limited to critical interaction points.
  3.  **End-to-End (E2E) Tests (Pytest with environment simulation):**
      *   **Purpose:** Simulate a full run of the AI agent (e.g., training for a few episodes, then evaluating).
      *   **Strategy:** Run the CLI commands directly and assert expected outcomes or logs.
  4.  **Code Coverage:** Integrated into CI/CD using Codecov or similar.

  --- 

  ## 7. APEX SECURITY PROTOCOL (Proactive & Reactive)

  1.  **Dependency Scanning:** Regularly scan `requirements.txt` (or `pyproject.toml` with `uv`) for known vulnerabilities using tools like Dependabot, Snyk, or Trivy.
  2.  **Static Application Security Testing (SAST):** Integrate tools like Bandit for Python to identify potential security flaws in code pre-runtime.
  3.  **Dynamic Application Security Testing (DAST):** (If applicable for web-exposed components) Use tools like OWASP ZAP.
  4.  **Secrets Management:** Environment variables or secure vault (e.g., HashiCorp Vault) for sensitive information. **Never hardcode secrets.**
  5.  **Principle of Least Privilege:** Ensure all components and users operate with the minimum necessary permissions.
  6.  **Incident Response Plan:** Defined procedures in `SECURITY.md` for reporting and addressing vulnerabilities.

  --- 

  ## 8. APEX DOCUMENTATION STANDARDS

  1.  **`README.md`:** Comprehensive, visually appealing, covering setup, usage, features, architecture, and agent directives.
  2.  **`CONTRIBUTING.md`:** Clear guidelines for contributions, including coding standards, PR process, and testing.
  3.  **`SECURITY.md`:** Detailed security policy and vulnerability reporting instructions.
  4.  **Code Comments & Docstrings:** Clear, concise, and up-to-date comments (reStructuredText or Google style for Python) for all functions, classes, and complex logic.
  5.  **Architectural Decision Records (ADRs):** Document significant architectural choices and their rationale.

  --- 

  ## 9. APEX TOOLCHAIN (Python Specific)

  *   **Package Manager:** `uv` (preferred for speed and robustness over `pip`).
  *   **Linter/Formatter:** `Ruff` (for unparalleled performance and combined linting/formatting).
  *   **Testing:** `Pytest` (with `pytest-cov`).
  *   **Type Checking:** `mypy` (strict mode).
  *   **Environment Manager:** `uv venv` or standard `venv`.

  --- 

  ## 10. APEX COMMAND VERIFICATION

  To verify the project adheres to quality standards, the following commands *must* pass:

  *   **Dependency Installation & Environment Setup:**
      bash
      uv venv
      source .venv/bin/activate
      uv pip install -r requirements.txt
      uv pip install gymnasium[atari] gymnasium[accept-rom-license]
      
  *   **Linting & Formatting Check:**
      bash
      uv run ruff check src/
      uv run ruff format src/ --check
      
  *   **Automated Tests Execution:**
      bash
      uv run pytest
      
  *   **Type Checking:**
      bash
      uv run mypy src/
      
  *   **Example Training Run (no error):**
      bash
      python main.py train --episodes 5 --render-interval 1
      

</details>

## ⚙️ Development Standards

### Testing

This project uses `pytest` for comprehensive testing. Ensure all new features and bug fixes are accompanied by appropriate tests.

*   **Run Unit and Integration Tests:**
    bash
    source .venv/bin/activate
    uv run pytest
    

*   **Run with Coverage Report:**
    bash
    source .venv/bin/activate
    uv run pytest --cov=./src --cov-report=xml
    

### Linting & Formatting

`Ruff` is used for linting and formatting to ensure code quality and consistency.

*   **Check for linting errors and formatting issues:**
    bash
    source .venv/bin/activate
    uv run ruff check src/
    uv run ruff format src/ --check
    

*   **Automatically fix linting errors and format code:**
    bash
    source .venv/bin/activate
    uv run ruff check src/ --fix
    uv run ruff format src/
    

### Contributing

We welcome contributions! Please refer to our [CONTRIBUTING.md](https://github.com/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python/blob/main/.github/CONTRIBUTING.md) for detailed guidelines on how to contribute.

## 📜 License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International Public License** (CC BY-NC 4.0). See the [LICENSE](https://github.com/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python/blob/main/LICENSE) file for details.

## 🛡️ Security

For information on security vulnerabilities and how to report them, please refer to our [SECURITY.md](https://github.com/chirag127/DeepQ-SpaceInvaders-AI-Agent-Python/blob/main/.github/SECURITY.md) policy.