# 🫀 ECG-FilterHub: Advanced Bio-signal Processing Pipeline

![MATLAB](https://img.shields.io/badge/MATLAB-R2024-orange?logo=mathworks)
![Simulink](https://img.shields. slowed/badge/Simulink-Simulation-blue?logo=mathworks)
![Field](https://img.shields.io/badge/Domain-Biomedical_Engineering-red)

## 📌 Overview
This repository contains a high-fidelity **ECG Simulation and Processing System** developed in MATLAB/Simulink. The project bridges the gap between cardiac physiology and digital signal processing by generating synthetic cardiac rhythms and applying clinical-grade filtering to recover signals from heavy environmental noise.

---

## 🚀 Key Features
* **Dynamic Waveform Synthesis:** Models $P, QRS, \text{and } T$ waves using scaled Gaussian pulses.
* **Arrhythmia Modulator:** Simulates Heart Rate Variability (HRV) and irregular rhythms ($43-100 \text{ BPM}$).
* **Clinical Noise Injection:**
    * **PLI:** 50 Hz Powerline Interference.
    * **BW:** 0.5 Hz Baseline Wander (Respiration).
    * **EMG:** High-frequency Muscle Artifacts.
* **DSP Pipeline:** Includes a precision Notch filter, IIR High-pass, and a 200-sample Moving Average filter.

---

## 🛠️ System Architecture

The simulation follows a classic biomedical acquisition chain:

1.  **Generation:** `ecg_gen(t, period)` function creates a continuous cardiac vector.
2.  **Contamination:** Addition of deterministic and stochastic noise sources.
3.  **Filtration:** * **Notch:** Targeted rejection of $50 \text{ Hz}$.
    * **High-Pass:** DC-offset removal ($\alpha=0.98$).
    * **Moving Average:** Smoothing of EMG ripples.
4.  **Analysis:** Instantaneous BPM calculation via $60/RR$ logic.

> [!TIP]
> **View the results:** Check the `Results/` folder for screenshots of the Scope before and after filtration.

---

## 📊 Technical Specifications

| Parameter | Specification |
| :--- | :--- |
| **Sampling Rate ($f_s$)** | $1000 \text{ Hz}$ |
| **Resolution ($T_s$)** | $0.001 \text{ s}$ |
| **Notch Center Freq** | $50 \text{ Hz}$ |
| **BPM Tracking** | Real-time Adaptive |
| **Output Format** | `.csv` (Time, Raw, Noisy, Filtered) |

---

## 💻 Installation & Usage

1.  **Clone the Repo:**
    ```bash
    git clone [https://github.com/YourUsername/ECG-FilterHub.git](https://github.com/YourUsername/ECG-FilterHub.git)
    ```
2.  **Open in MATLAB:** Launch `ECG_Simulation.slx`.
3.  **Run Simulation:** Click 'Run' and observe the multi-channel Scope.
4.  **Export Data:** The model automatically generates `Combined_ECG_Data.csv` for further Python/R analysis.

---

## 🧪 Simulation Results
| Regular Simulation | Irregular Simulation |
| :---: | :---: |
| ![Regular Simulation](<img width="1658" height="990" alt="Diagrams" src="https://github.com/user-attachments/assets/5a922fbe-4d96-4d21-a636-411b1d3cd47e" />). | ![Irregular Simulation](<img width="1658" height="990" alt="Irr_Di" src="https://github.com/user-attachments/assets/0bcd0a78-d13f-4232-8c7d-f06c4e23b2f0" />) | 



---

## 🎓 Academic Context
* **Course:** Medical Equipment.
* **Department:** Systems & Biomedical Engineering (SBME).
* **University:** Cairo University, Faculty of Engineering.

**Developer:** Habiba  
**Connect with me:** [LinkedIn](www.linkedin.com/in/habiba-a-frahat-95754b390) | [Email](ahmdhbybh753@gmail.com)

---
© 2026 Habiba. Distributed under the MIT License.
