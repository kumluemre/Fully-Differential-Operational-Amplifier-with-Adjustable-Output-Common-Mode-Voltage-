# Fully Differential Op-Amp with Adjustable Output Common-Mode Voltage

## 🚀 Project Overview
This project focuses on the design and implementation of a **Two-Stage Fully Differential Operational Amplifier** using **XFAB XH018 (180nm High Voltage CMOS)** technology.

The design features an **adjustable output common-mode voltage** (0.6V to 1.5V) controlled by an external input, making it highly versatile for analog signal processing chains. It also includes a high-performance, low-power **Reference Circuit** operating in the subthreshold region.

---

## 📊 Performance Metrics (Simulation Results)
The circuit demonstrates robust performance across PVT corners. The nominal results at **3.3V** supply are as follows:

| Parameter | Result |
| :--- | :--- |
| **DC Gain** | **84.9 dB** |
| **Unity-Gain Bandwidth** | **76.4 MHz** |
| **Phase Margin** | **59.7°** |
| **CMRR (@50 kHz)** | **166.71 dB** |
| **PSRR** | **102.04 dB** |
| **Slew Rate (CL=5pF)** | 40.29 V/µs |
| **Output CM Range** | 0.6V - 1.5V (Adjustable) |
| **Current Consumption** | 279.4 µA |

### ⚡ Reference Circuit Performance
* **Current Consumption:** 149.6 nA (Ultra-low power)
* **Temp Coefficient:** 1.12% (-40°C to +85°C)
* **PSRR:** 91.26 dB

---

## 🛠️ Circuit Architecture

### 1. Main Amplifier Topology
* **Stage 1:** **Folded Cascode** with PMOS inputs to support negative input common-mode levels (-0.3V).
* **Stage 2:** **Common Source** (NMOS) to boost gain and output swing.
* **Compensation:** Miller compensation with a nulling resistor (implemented via linear region NMOS) to eliminate the RHP zero.

### 2. Common-Mode Feedback (CMFB)
* Uses a continuous-time CMFB network with an active-loaded differential pair.
* Senses output common-mode voltage via high-impedance paths to minimize loading.
* Stabilizes the output levels to match the external control voltage ($V_{cm}$).

### 3. Robust Reference Circuit
* Designed using subthreshold MOSFETs to generate temperature and supply-independent bias voltages.
* Includes a Low-Pass Filter to enhance PSRR.

---

## 💻 Tools & Technology
* **EDA Tool:** Cadence Virtuoso Analog Design Environment (ADE)
* **Technology:** XFAB XH018 (180nm CMOS)
* **Verification:** DC, AC, Transient, and PVT Corner Analysis (Worst-Power, Worst-Speed, etc.)

---

## 📄 Project Report
For detailed circuit schematics, design equations, and comprehensive corner analysis results, please refer to the full project report:

### 👉 [View Full Project Report (PDF)](./Fully-Differential-OpAmp-Report.pdf)
