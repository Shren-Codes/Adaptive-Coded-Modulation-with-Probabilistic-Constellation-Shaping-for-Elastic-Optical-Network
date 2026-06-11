# 📡 Adaptive Coded Modulation with Probabilistic Constellation Shaping for Elastic Optical Networks

<div align="center">

### Intelligent Modulation Selection for Next-Generation Optical Networks

![MATLAB](https://img.shields.io/badge/MATLAB-R2024a-orange)
![OptiSystem](https://img.shields.io/badge/OptiSystem-Simulation-blue)
![Optical Communication](https://img.shields.io/badge/Domain-Optical%20Communication-purple)
![Status](https://img.shields.io/badge/Status-Completed-success)

</div>

---

# 🎯 Project Overview

The rapid growth of cloud computing, video streaming, 5G infrastructure, IoT ecosystems, and data center interconnects has created an unprecedented demand for optical network capacity. Modern optical communication systems must efficiently utilize available bandwidth while maintaining reliable data transmission under varying channel conditions.

Traditional optical systems typically employ a fixed modulation format throughout the entire communication link. While this approach simplifies system design, it often leads to inefficient spectrum utilization and degraded performance. Conservative modulation schemes waste available channel capacity during favorable conditions, while aggressive high-order modulation formats may suffer excessive Bit Error Rates (BER) under poor channel conditions.

To address these challenges, this project presents an **Adaptive Coded Modulation (ACM)** framework enhanced with **Probabilistic Constellation Shaping (PCS)** for Elastic Optical Networks (EONs).

The proposed system continuously evaluates channel quality using Optical Signal-to-Noise Ratio (OSNR) measurements and dynamically selects the most appropriate modulation format. By intelligently switching between modulation schemes, the system maintains communication reliability while maximizing throughput and spectral efficiency.

---

# 🌟 Key Innovation

Unlike conventional adaptive modulation systems that switch only between fixed modulation formats, this project integrates:

### 🔄 Adaptive Modulation

Dynamic switching between:

- QPSK
- 16-QAM
- PCS-16QAM

based on real-time channel conditions.

### 📊 Probabilistic Constellation Shaping (PCS)

Instead of transmitting all constellation symbols with equal probability, PCS employs a Maxwell-Boltzmann probability distribution to favor lower-energy symbols.

This enables:

- Reduced average transmit power
- Improved BER performance
- Enhanced energy efficiency
- Operation closer to the Shannon capacity limit

### 🧠 Multi-Objective Optimization

The adaptive controller jointly optimizes:

- 📉 Bit Error Rate (BER)
- 🚀 Spectral Efficiency (SE)
- ⚡ Power Consumption

through a normalized composite scoring function.

### 🔒 Hysteresis-Based Stability Control

A finite-state machine (FSM) with hysteresis prevents unnecessary switching events and eliminates oscillatory behavior near decision thresholds.

---

# 🏗️ System Architecture

The complete adaptive optical communication system consists of three major layers:

## 📡 Physical Layer

Responsible for optical transmission and reception.

Components include:

- PRBS Generator
- QPSK Modulator
- 16-QAM Modulator
- Dual-Port Mach-Zehnder Modulator
- Optical Fiber Channel
- Optical Noise Source
- Coherent Receiver
- BER Analyzer

---

## 📏 Measurement Layer

Responsible for monitoring channel quality.

Functions include:

- OSNR estimation
- BER monitoring
- Signal quality assessment

---

## 🎛️ Control Layer

Responsible for intelligent modulation selection.

Functions include:

- Adaptive modulation control
- Composite score computation
- Hysteresis-based switching
- PCS optimization

---

# ⚙️ Adaptive Modulation Strategy

The modulation format is selected according to channel quality.

| Channel Condition | Selected Format |
|------------------|----------------|
| Low OSNR | QPSK |
| Moderate OSNR | PCS-16QAM |
| High OSNR | 16-QAM |

This strategy allows the system to maintain BER requirements while maximizing spectral efficiency.

---

# 📊 Probabilistic Constellation Shaping

Probabilistic Constellation Shaping is implemented using a Maxwell-Boltzmann distribution:

P(ai) = exp(-λ|ai|²)/Z

where:

λ = 0.35

The selected shaping parameter achieves an effective balance between:

- Energy efficiency
- Spectral efficiency
- BER performance

### Benefits Achieved

✅ +1.20 dB shaping gain

✅ 13% reduction in power consumption

✅ Improved BER performance

✅ Increased robustness under moderate OSNR conditions

---

# 🔄 Hysteresis-Based Switching

One of the major challenges in adaptive modulation systems is excessive switching near threshold boundaries.

To address this issue, a hysteresis dead-band is introduced.

| Action | Threshold |
|----------|------------|
| Upgrade to Higher Modulation | 22 dB |
| Downgrade to Lower Modulation | 18 dB |

This mechanism prevents rapid oscillation between modulation formats and ensures stable system operation.

---

# 🧠 Multi-Objective Composite Scoring

The modulation selection process is driven by a normalized composite score:

S(m) = w₁ × BER + w₂ × SE + w₃ × Power

Where:

| Metric | Weight |
|---------|---------|
| BER | 0.50 |
| Spectral Efficiency | 0.30 |
| Power Consumption | 0.20 |

The controller prioritizes communication reliability while simultaneously maximizing throughput and minimizing power usage.

---

# 🖥️ Simulation Environment

## MATLAB

Used for:

- BER modeling
- PCS implementation
- Adaptive switching logic
- Composite score computation
- Hysteresis FSM implementation

## OptiSystem

Used for:

- Physical-layer optical simulation
- Fiber transmission modeling
- Coherent receiver validation
- BER analysis
- Eye diagram generation

---

# 📈 Performance Highlights

### 📉 BER Performance

- BER maintained below 10⁻⁶
- Zero BER violations across OSNR sweep
- Reliable communication under varying channel conditions

### 🚀 Spectral Efficiency

- Fixed QPSK: 2 bits/symbol
- Adaptive ACM+PCS: 3.728 bits/symbol

✅ 86% improvement over fixed QPSK

### ⚡ Energy Efficiency

- Improved bits-per-watt performance
- Reduced transmit power through PCS
- Higher throughput with controlled power consumption

### 🔒 Stability

- Only 2 switching events across the complete OSNR sweep
- No oscillatory behavior
- Robust hysteresis operation

---

# 🌟 Key Contributions

✅ Adaptive Coded Modulation Framework

✅ Probabilistic Constellation Shaping Integration

✅ Multi-Objective Optimization Strategy

✅ Hysteresis-Stabilized Finite State Machine

✅ MATLAB–OptiSystem Co-Simulation

✅ BER-Compliant Elastic Optical Network Design

---

# 🔮 Future Scope

- Extension to 64-QAM and 256-QAM
- Adaptive PCS parameter optimization
- WDM-based multi-channel optical systems
- FPGA implementation of adaptive controller
- Integration with Forward Error Correction (FEC)
- Real-time deployment in software-defined optical networks

---

# 👩‍💻 Author

### Shrenica Chawda

🎓 B.Tech Electronics and Communication Engineering

🏛️ Vellore Institute of Technology, Chennai

📡 Optical Communication • Signal Processing • Embedded Systems

---

⭐ If you found this project useful, consider giving the repository a star.
