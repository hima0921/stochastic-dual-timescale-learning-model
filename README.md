# Dual-Timescale Model of Learning (ODE & SDE)

## Overview
This project models learning as a combination of fast and slow processes using differential equations. The goal is to understand how learning and memory evolve over time, and how noise affects these dynamics.

The model is inspired by findings in cognitive science and motor learning, where behavior cannot be explained by a single learning rate. Instead, a fast process adapts quickly but forgets quickly, while a slow process learns gradually and retains information over longer periods.

## Motivation
In both human learning and machine learning systems, there is a tradeoff between:
- learning quickly from new information  
- retaining knowledge over time  

This project explores how this tradeoff can be modeled mathematically, and how it connects to:
- motor learning in humans  
- memory systems in the brain  
- training dynamics in neural networks  

## Model

### Deterministic Model (ODE)
The system is modeled using two coupled differential equations:

- Fast component: learns quickly, forgets quickly  
- Slow component: learns slowly, retains longer  

Both components respond to the same error signal:
- learning is driven by how far the system is from a target  
- forgetting is modeled as decay over time  

The model allows:
- equilibrium analysis  
- stability analysis using eigenvalues  
- visualization using phase planes  

### Key Results (Deterministic)
- The system has a unique, globally stable equilibrium  
- The fast and slow components operate at distinct timescales  
- Long-term learning is dominated by the slow component  

### Rest Period Extension
A time-varying target was introduced to simulate learning and rest phases.

This shows:
- **Savings**: relearning becomes faster over time  
- **Differential forgetting**: fast component decays quickly, slow component persists  

These effects emerge naturally from the model without adding new parameters.

---

## Stochastic Extension (SDE)

To account for randomness in learning, the model was extended using stochastic differential equations:

- Noise is introduced using a Wiener process  
- This captures variability in biological systems and machine learning  

### Key Results (Stochastic)

1. **Mean Preservation**  
   The average behavior of the system follows the same path as the deterministic model.

2. **σ² Scaling Law**  
   The variance of the system scales with the square of noise intensity (σ²).

3. **Higher Variance in Slow Component**  
   The slow component accumulates more variability because it responds more slowly to changes.

---

## Connection to AI
The model provides insights into machine learning systems:

- Fast component ↔ gradient updates  
- Slow component ↔ momentum / long-term learning  
- Noise ↔ stochastic gradient descent / temperature in LLMs  

It helps explain:
- catastrophic forgetting  
- stability vs plasticity tradeoff  
- variability in model training outcomes  

---

## Materials
- [Full project report](Report.pdf)  
- [Presentation slides](Slides.pdf)

---

## My Contribution
This was a group project. My contributions focused on the theoretical and modeling components of the work, including:

- Formulating the dual-timescale learning model in continuous time using differential equations  
- Analyzing equilibrium behavior and stability of the system  
- Extending the deterministic model to a stochastic framework (SDEs)  
- Deriving and interpreting key results, including mean preservation and the σ² scaling law  
- Developing the conceptual connection between biological learning systems and artificial learning models  

My contribution covered the project up to the theoretical stochastic modeling stage. The later implementation of neural network training and experimental results was completed as part of collaborative work.

---

## Context
Developed as part of coursework at Arizona State University.
