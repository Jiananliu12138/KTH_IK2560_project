# KTH_IK2560_project

This project investigates inter-cell interference (ICI) coordination methods in cellular networks to improve network performance for edge users. Specifically, it evaluates three ICI coordination strategies—Uncoordinated Scheduling, Queue Load Based Selection (QLBS), and P-persistent Scheduling—under varying traffic loads and interference scenarios.

## Table of Contents

1. [Introduction](#introduction)
2. [System Model](#system-model)
   - [Path Loss Model](#path-loss-model)
   - [Noise Model](#noise-model)
   - [Signal-to-Interference-plus-Noise Ratio (SINR)](#signal-to-interference-plus-noise-ratio-sinr)
   - [Traffic Model](#traffic-model)
   - [Throughput and Delay](#throughput-and-delay)
3. [Simulation](#simulation)
   - [Single Base Station Performance](#single-base-station-performance)
   - [P-value Optimization](#p-value-optimization)
   - [Dual Base Station Coordination](#dual-base-station-coordination)
   - [Monte Carlo Analysis](#monte-carlo-analysis)
4. [Results](#results)
5. [Conclusion and Future Work](#conclusion-and-future-work)
6. [References](#references)
7. [Appendix](#appendix)

---

## Introduction

Inter-cell interference remains a significant challenge in cellular networks, especially for users at cell edges. This project systematically evaluates the performance of three ICI coordination methods and identifies the optimal strategies for different traffic loads.

## System Model

### Path Loss Model
Uses the log-distance model:  
**PL(d) = PL₀ + 10α log₁₀(d/d₀)**  
Where:
- PL₀ is the reference path loss.
- α is the path loss exponent (set to 3 in this study).

### Noise Model
The noise follows an Additive White Gaussian Noise (AWGN) model with power spectral density \(N₀ = 10^{-21}\) W/Hz.

### Signal-to-Interference-plus-Noise Ratio (SINR)
Defined as:
**SINR = Ps / (Pi + Pn)**  
Where \(Ps\) is the received signal power, \(Pi\) is the interference power, and \(Pn\) is the noise power.

### Traffic Model
Packet arrivals follow a Poisson distribution, with arrival rates corresponding to low, medium, and high traffic loads.

### Throughput and Delay
- **Throughput**: Total successfully transmitted packets over time.  
- **Delay**: Average queue length normalized by throughput.

## Simulation

### Single Base Station Performance
Compares the three methods without interference between base stations to evaluate baseline throughput and delay.

### P-value Optimization
Optimizes the probability \(p\) in P-persistent scheduling for balancing collision avoidance and resource utilization under different traffic loads.

### Dual Base Station Coordination
Analyzes performance when users are located in interference-sensitive areas covered by two base stations.

### Monte Carlo Analysis
Simulates multi-user environments and calculates user success rates and system throughput under various SINR thresholds.

## Results

- **Uncoordinated Scheduling**: Performs well under low loads but suffers under high loads due to interference.  
- **QLBS**: Consistently achieves high throughput and low delay across all traffic conditions.  
- **P-persistent Scheduling**: Balances performance through dynamic \(p\)-value adjustments but is sensitive to SINR thresholds.

## Conclusion and Future Work

### Conclusion
QLBS emerges as the most effective strategy in minimizing interference, optimizing throughput, and reducing latency in cellular networks.

### Future Work
- Extend the study to more complex network topologies.
- Incorporate advanced spectrum resource allocation techniques like OFDM.
- Evaluate under real-world scenarios with more diverse traffic patterns.

## References

1. Yiqing Zhou et al., "An overview on intercell interference management in mobile cellular networks: From 2G to 5G," IEEE, 2014.  
2. Chrysovalantis Kosta et al., "On interference avoidance through ICIC based on OFDMA mobile systems," IEEE Communications Surveys & Tutorials, 2012.  
3. [Full reference list available in the project report](#appendix).

## Appendix

- [GitHub Repository](https://github.com/Jiananliu12138/KTH_IK2560_project.git)
- Detailed simulation parameters and results are provided in the project report.
