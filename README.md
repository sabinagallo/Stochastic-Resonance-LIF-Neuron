![Python](https://img.shields.io/badge/Python-Scientific%20Computing-blue)
![Type](https://img.shields.io/badge/Type-Academic%20Project-green)
![Field](https://img.shields.io/badge/Field-Computational%20Neuroscience-purple)
![Topic](https://img.shields.io/badge/Topic-Stochastic%20Resonance-orange)

# Stochastic Resonance in a LIF Neuron
## BSc Artificial Intelligence - Brain Modeling Project

Computational study of **stochastic resonance in neural systems** using a **Leaky Integrate-and-Fire (LIF) nueron model**.
The project investigates how stochastic noise can enhance the detection of a weak subthreshold signals and improve spike-signal synchronization at both **single-neuron and population levels**.

## Project Overview
Neural systems operate in intrinsically noisy environments. While noise is often traditionally considered detrimental to signal processing, nonlinear threshold systems such as neurons can exploit noise to enhance weak signal detection.
This phenomenon is known as **Stochastic Resonance (SR)**.

In this project, we simulate a **Leaky Integrate-and-Fire (LIF) neuron** receveing a weak sinusoidal input that remains below firing threshold. By introducing stochastic fluctuations in the input current, we study how noise enables threshold crossings and enhances **temporal signal encoding**.

The analysis investigates both **single neuron dynamics** and **population-level robustness**.

## Research Questions
This project explores the following hypotheses:

**H1 — Optimal noise level**  
Spike-signal synchronization is maximized at an intermediate noise intensity.

**H2 — Signal amplitude dependence**  
Increasing the signal amplitude shifts the optimal noise level toward lower values.

**H3 — Operating point dependence**  
Increasing the bias current brings the neuron closer to threshold, reducing the noise level required for stochastic resonance.

**H4 — High-noise degradation**  
Excessive noise increases firing activity but degrades temporal precision.

**H5 — Population robustness**  
Pooling spikes across multiple neurons produces more stable signal representations.

## Model
The neuron is modeled using a **Leaky Integrate-adnFire (LIF) model**, which describes membrane potential dynamics as a threshold system integrating incoming current.

Subthreshold membrane dynamics:

τₘ dV/dt = −(V − Eₗ) + I(t)/gₗ

A spike occurs when the membrane potential reaches the threshold \(V_{th}\), after which the neuron resets and enters a refractory period.

The neuron receives a weak periodic input:

I(t) = I_bias + A sin(2πft)

Noise is introduced as **Gaussian white noise** added to the input current

## Methods
The simulation pipeline consists of several steps:

**LIF neuron simulation**  
The membrane dynamics are simulated using numerical integration.

**Noise injection**  
Gaussian noise is added to the input current with varying noise intensity.

**Stochastic resonance analysis**  
Noise intensity is systematically varied to identify the optimal noise level.

**Spike synchronization measurement**  
Spike–signal synchronization is quantified using **Vector Strength**, a phase-locking metric.

**Parameter sweeps**  
The analysis explores how stochastic resonance depends on:

- signal amplitude
- bias current
- noise intensity

**Population simulation**  
The model is extended to a population of **N = 50 independent neurons** receiving identical signals but independent noise realizations.

## Results
The results reveal the characteristic **stochastic resonance curve**.

At low noise levels  
→ spiking is rare and synchronization is weak.

At intermediate noise levels  
→ spike timing becomes strongly phase-locked to the input signal, maximizing synchronization.

At high noise levels  
→ firing activity increases but temporal precision degrades due to noise-dominated spike timing.

## Tech Stack
**Language**  
Python

**Libraries**  
- numpy  
- scipy  
- matplotlib  
- tqdm  

**Techniques**  
Computational neuroscience modeling  
Stochastic simulations  
Phase-locking analysis  
Population neural coding  

## Project Materials
Additionals materials for this project are available below

**Project report**
Full methodological description adn results.  
[Read the report](BM_report.pdf)

**Simulation notebook**
Python notebook containing the full simulation and analysis pipeline.
[View the notebook](Project_Brain_modeing.ipynb)

## Authors
Sabina Gallo  
Beatrice Camera  
Irene Marrali  

BSc Artificial Intelligence 
University of Pavia - University of Milano Statale - University of Milano-Bicocca


