# 🎮 RL Book Interactive Labs

**Companion interactive apps & notebooks for [Complete Reinforcement Learning Journey: From Basics to RLHF]()**

> *Don't just read about algorithms — watch them think.*

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/demo-live-brightgreen)](https://mlnjsh.github.io/rl-book-labs/)

---

## 🧪 What Is This?

Each chapter has **two companions**:
- 🌐 **Interactive Web App** — browser-based, no install, sliders + animations
- 📓 **Colab Notebook** — full Python code, build environments, run algorithms, plot results

---

## 📚 Available Labs

| Chapter | Web App | Colab Notebook | Concepts |
|---------|---------|----------------|----------|
| Ch 2: MDPs | [▶ MDP Explorer](https://mlnjsh.github.io/rl-book-labs/ch2/) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mlnjsh/rl-book-labs/blob/main/Ch2_MDP_Environments_Lab.ipynb) | States, Actions, Rewards, Transitions, Deterministic vs Stochastic |
| Ch 3: DP | [▶ Policy Iteration](https://mlnjsh.github.io/rl-book-labs/ch3/) | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mlnjsh/rl-book-labs/blob/main/Ch3_Dynamic_Programming_Lab.ipynb) | Policy Evaluation, Policy Iteration, Value Iteration, Convergence |
| Ch 4 | *coming soon* | *coming soon* | Monte Carlo Methods |
| Ch 5 | *coming soon* | *coming soon* | TD Learning, SARSA, Q-Learning |
| Ch 6 | *coming soon* | *coming soon* | Deep RL, DQN |
| Ch 7 | *coming soon* | *coming soon* | Policy Gradients, RLHF |

---

## 📓 Colab Notebooks

### 💻 How to Run the Notebooks

The notebooks can be run in **three ways** — pick whichever you prefer:

| Platform | How to Open | Setup Required |
|----------|------------|----------------|
| **Google Colab** | Click the "Open in Colab" badge above — runs instantly in your browser | None — everything pre-installed |
| **VS Code** | Clone this repo → open `.ipynb` file → select Python kernel → run cells | Install Python + libraries (see below) |
| **Jupyter Notebook / JupyterLab** | Clone this repo → `jupyter notebook` → open `.ipynb` file | Install Python + libraries (see below) |

#### Running in VS Code
1. Install the [Jupyter extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter) for VS Code
2. Clone this repo:
   ```bash
   git clone https://github.com/mlnjsh/rl-book-labs.git
   cd rl-book-labs
   ```
3. Install dependencies:
   ```bash
   pip install gymnasium numpy matplotlib seaborn pandas
   ```
4. Open any `.ipynb` file in VS Code → click **"Select Kernel"** → choose your Python environment → run cells with `Shift+Enter`

#### Running in Jupyter Notebook
1. Clone and install (same as above)
2. Launch Jupyter:
   ```bash
   jupyter notebook
   ```
3. Navigate to the `.ipynb` file and open it

---

### Ch2: MDP Environments Lab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mlnjsh/rl-book-labs/blob/main/Ch2_MDP_Environments_Lab.ipynb)

Build **7 MDP environments** from scratch in Python:

| # | Environment | States | Actions | Key Lesson |
|---|------------|--------|---------|------------|
| 1 | GridWorld 5×5 | 22 cells | ←↓→↑ | Walls, goal, pit, spatial navigation |
| 2 | FrozenLake 4×4 | 16 cells | ←↓→↑ | Slippery ice, holes |
| 3 | Traffic Light | 6 states | keep/switch | Real-world control |
| 4 | Thermostat | 3 states | heat/cool/off | Energy vs comfort tradeoff |
| 5 | Contextual Bandit | 3 contexts | machine A/B/C | Context-dependent rewards |
| 6 | Inventory Management | 5 levels | order 0/1/2 | Supply chain, stockouts |
| 7 | Robot Rooms | 4 rooms | go/stay | Locked doors, path planning |

**What you'll do:** Inspect transition tables, compute Q-values, visualize value heatmaps, compare deterministic vs stochastic, experiment with γ.

### Ch3: Dynamic Programming Lab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mlnjsh/rl-book-labs/blob/main/Ch3_Dynamic_Programming_Lab.ipynb)

Implement **3 core DP algorithms** and run them on all 7 environments:

| Algorithm | What It Does |
|-----------|-------------|
| Policy Evaluation | Compute V^π sweep by sweep — watch values converge |
| Policy Iteration | Evaluate → Improve loop until π* found |
| Value Iteration | Single Bellman max update — faster convergence |

**What you'll do:** Animated convergence plots, PI vs VI comparison table, γ effect on convergence speed, stochastic policy comparison (5 slip values side by side).

---

### 📦 Required Libraries

```
gymnasium    - RL environments (FrozenLake, etc.)
numpy        - numerical computation
matplotlib   - plotting and visualization
seaborn      - heatmaps for value functions
pandas       - data tables
```

**Quick install:**
```bash
pip install gymnasium numpy matplotlib seaborn pandas
```

> 💡 **Google Colab users:** All libraries are pre-installed. Just click "Open in Colab" and run — no setup needed!
>
> 💡 **VS Code / Jupyter users:** Run the install command above once, then you're good to go.

---

## 🌐 Interactive Web Apps

### Ch2: MDP Explorer
[▶ Launch App](https://mlnjsh.github.io/rl-book-labs/ch2/)

Three modes: **🔍 Explore** (click cells → see S,A,R,P), **π Policy** (click to change arrows), **V Value** (heatmap). Features: deterministic/stochastic toggle, editable grid, robot episodes, Q-value inspector.

### Ch3: Policy Iteration Visualizer
[▶ Launch App](https://mlnjsh.github.io/rl-book-labs/ch3/)

Step through PI on FrozenLake: **① One Eval Sweep** (cells light up blue), **② Improve** (arrows flash green), **🤖 Run Robot** (animated walk). Speed control, γ and slip sliders.

---

## 🏗️ Project Structure

```
rl-book-labs/
├── README.md
├── Ch2_MDP_Environments_Lab.ipynb      # 📓 Notebook: 7 MDP environments
├── Ch3_Dynamic_Programming_Lab.ipynb   # 📓 Notebook: PI, VI, convergence
├── ch2/
│   └── index.html                      # 🌐 Web App: MDP Explorer
├── ch3/
│   └── index.html                      # 🌐 Web App: Policy Iteration
├── ch4/                                # (coming soon)
└── ch5/                                # (coming soon)
```

---

## 🎓 About the Book

**Complete Reinforcement Learning Journey: From Basics to RLHF**

The only book that takes you from "What is a Markov Decision Process?" all the way to "How do we align language models with human values?" — with intuition, math, code, and interactive labs at every step.

### Key Features
- 📖 **Intuition → Math → Code** triple for every concept
- 🤖 **DeliBot** running example that grows with the theory
- 🧠 **Think Like an Agent** boxes for building intuition
- ⚠️ **Common Misconceptions** boxes to prevent errors
- 🔬 **Interactive Web Labs** for visual, hands-on learning
- 📓 **Colab / VS Code / Jupyter Notebooks** for coding along
- 📝 **Quizzes with detailed answer keys** for each chapter

---

## 🤝 Contributing

Found a bug? Have an idea for a new visualization? Contributions welcome!

1. Fork the repo
2. Create a branch (`git checkout -b feature/new-lab`)
3. Commit your changes
4. Open a Pull Request

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

<p align="center">
  <i>Built with ❤️ as a companion to the book.</i><br>
  <i>"The best way to learn an algorithm is to watch it think."</i>
</p>
