# 🎮 RL Book Interactive Labs

**Companion interactive apps for [Complete Reinforcement Learning Journey: From Basics to RLHF]()**

> *Don't just read about algorithms — watch them think.*

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/demo-live-brightgreen)](https://mlnjsh.github.io/rl-book-labs/)

---

## 🧪 What Is This?

Each chapter of the book has a companion **browser-based interactive lab** where you can:

- 🔵 **Step through algorithms** cell-by-cell and see values update in real-time
- 🎛️ **Tweak parameters** (γ, ε, learning rate) with sliders and instantly see the effect
- 🤖 **Watch agents navigate** grids, solve problems, and learn from mistakes
- 📊 **Inspect Q-values**, policy arrows, and convergence logs live

**No installation required.** Open in any browser. Works on desktop and mobile.

---

## 📚 Available Labs

| Chapter | Lab | Concepts Covered | Try It |
|---------|-----|-----------------|--------|
| Ch 3 | **Policy Iteration on FrozenLake** | Bellman equations, policy evaluation (sweep-by-sweep), policy improvement, convergence | [▶ Launch](https://mlnjsh.github.io/rl-book-labs/ch3/) |
| Ch 4 | Monte Carlo Blackjack *(coming soon)* | First-visit MC, exploring starts, episode replay | — |
| Ch 5 | TD Learning & SARSA *(coming soon)* | TD(0), SARSA, Q-learning, cliff walking | — |
| Ch 6 | DQN on CartPole *(coming soon)* | Experience replay, target networks, training curves | — |
| Ch 7 | Policy Gradients *(coming soon)* | REINFORCE, baselines, variance reduction | — |

---

## 🚀 Ch3: Policy Iteration Visualizer

**The flagship lab.** Step through the Policy Iteration algorithm on a 4×4 FrozenLake grid.

### What You Can Do

| Button | What Happens |
|--------|-------------|
| **① One Eval Sweep** | Each cell lights up blue as its value updates via the Bellman equation |
| **① Full Evaluation** | Runs all sweeps until V^π converges |
| **② Improve Policy** | Arrows change one-by-one to the greedy action — green flash on changes |
| **▶▶ Auto-Run** | Runs the full evaluate → improve loop with pauses between iterations |
| **🤖 Run Robot** | Animated robot walks the grid following the current policy |
| **↺ Reset** | Start fresh with new parameters |

### Parameters to Experiment With

- **Discount factor γ** (0.1 → 0.99): How much does the agent care about the future?
- **Slip probability** (0 → 0.5): How stochastic is the environment?
- **Animation speed** (🐢 Slow → ⚡ Fast): Control the visualization pace

### What to Try

1. Set **γ = 0.5** → run to convergence → note the policy
2. Set **γ = 0.99** → run again → compare: the agent plans further ahead!
3. Set **Slip = 0** → deterministic → the optimal path is obvious
4. Set **Slip = 0.5** → highly stochastic → the policy becomes more cautious
5. Run 🤖 multiple times with high slip → watch different outcomes each time

---

## 🏗️ Project Structure

```
rl-book-labs/
├── index.html              # Landing page with links to all labs
├── ch3/
│   └── index.html          # Policy Iteration on FrozenLake (standalone)
├── ch4/                    # (coming soon)
├── ch5/                    # (coming soon)
└── README.md
```

Each lab is a **single HTML file** — no build step, no dependencies, no frameworks to install. Just pure HTML + CSS + JavaScript.

---

## 🎓 About the Book

**Complete Reinforcement Learning Journey: From Basics to RLHF**

The only book that takes you from "What is a Markov Decision Process?" all the way to "How do we align language models with human values?" — with intuition, math, code, and interactive labs at every step.

### Key Features
- 📖 **Intuition → Math → Code** triple for every concept
- 🤖 **DeliBot** running example that grows with the theory
- 🧠 **Think Like an Agent** boxes for building intuition
- ⚠️ **Common Misconceptions** boxes to prevent errors
- 🔬 **Interactive Labs** (this repo!) for hands-on learning
- 📝 **Quizzes with detailed answer keys** for each chapter

---

## 🤝 Contributing

Found a bug in a lab? Have an idea for a new visualization? Contributions are welcome!

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
