# Pelican-RL: Biomimetic Visual Servoing through Reinforcement Learning

## Historical Context: Project Pigeon
This research draws its foundational inspiration from B.F. Skinner's historical "Project Pigeon". In the original biological setup, conditioned pigeons were utilized to guide the Pelican missile by pecking at an image of a target (a ship) projected onto a screen. This repository modernizes that historical mechanical interface, framing the biological visual and decision-making processing as a benchmark for autonomous reinforcement learning architectures.

## Abstract
This research project aims to explore the use of Reinforcement Learning (RL) to solve a visual servoing problem. The primary objective is to identify and design the most optimized RL architecture capable of replacing the biological visual and decision-making processing of the bird. By evaluating the trade-offs between computational complexity, onboard inference time, and tracking accuracy, this project establishes robust baselines for autonomous robotics.

## Markov Decision Process (MDP) Formulation
*   **State Space ($S_t$)**: End-to-End processing utilizing a stack of the last $N$ visual frames. This captures environmental dynamics, specifically the relative speed and the target's magnification.
*   **Action Space ($A_t$)**: An evolutive approach. The initial phase mimics the historical interface using a discrete space (simulating a pecking grid). The advanced phase utilizes a continuous space for direct flight commands.
*   **Reward Function ($R_t$)**: A dense continuous function providing positive rewards as long as the geometric center of the target remains close to the image crosshair. Penalties are applied for losing the target in the field of view or issuing abrupt commands.
