# Deep Learning–Based SOC and SOH Estimation for Lithium-Ion Batteries

This repository contains the implementation and analysis of a semester project focused on **State of Charge (SOC)** and **State of Health (SOH)** estimation for lithium-ion batteries using **data-driven deep learning methods**. The project evaluates multiple neural network architectures and discusses their suitability for **real-time embedded deployment** in Battery Management Systems (BMS).

---

## 📌 Project Overview

Accurate estimation of SOC and SOH is critical for the safe and efficient operation of electric vehicles and energy storage systems. Classical model-based approaches often struggle under dynamic operating conditions and battery aging. This project explores modern **machine learning and deep learning techniques** to improve estimation accuracy and robustness.

### Key Contributions:
- SOC estimation using **FCN, CNN, and LSTM**
- SOH estimation using a **CNN–LSTM hybrid architecture**
- Evaluation on realistic automotive drive cycles
- Discussion on **real-time deployment using TensorFlow Lite for Microcontrollers (TFLM)**

---

## 🧠 Methods Used

### SOC Estimation
- Fully Connected Neural Network (FCN)
- Convolutional Neural Network (CNN)
- Long Short-Term Memory (LSTM)

### SOH Estimation
- CNN-based feature extraction
- LSTM-based degradation modeling

The LSTM-based models demonstrate superior performance by effectively capturing temporal dependencies and long-term battery behavior.

---

## 📊 Dataset

The project uses the **LG HG2 lithium-ion battery dataset** collected at McMaster University.

- Cell: LG HG2 (3 Ah)
- Tests: HPPC, constant current, and standard drive cycles (UDDS, US06, HWFET, Mixed)
- Temperatures: 40°C to −20°C

📎 Dataset link:  
https://data.mendeley.com/datasets/cp3473x7xv/3

> The dataset is **not included** in this repository due to size constraints.

---

## 📈 Results Summary

- **SOC Estimation:**  
  LSTM outperforms FCN and CNN in both scatter and time-domain evaluations, showing smooth and accurate SOC tracking under dynamic drive cycles.

- **SOH Estimation:**  
  The CNN–LSTM model successfully captures battery degradation trends with low RMSE and stable generalization.

---

## 🧪 Notebooks

All experiments were conducted using Google Colab notebooks:

- `notebooks/SOC_Estimation.ipynb`
- `notebooks/SOH_Estimation.ipynb`

You can upload your Colab notebooks directly into the `notebooks/` folder.

---

## 🔧 Embedded Deployment Discussion

The project includes an analysis of deploying trained models on microcontrollers using **TensorFlow Lite for Microcontrollers (TFLM)**.

Key considerations:
- Model quantization (int8)
- Memory footprint (tensor arena)
- Inference latency for real-time BMS updates
- Suitability for Cortex-M class MCUs

Future work includes exporting trained models to `.tflite` format and benchmarking on real hardware.

---

## 🚀 Future Work

- Quantization-aware training for MCU deployment
- Benchmarking inference latency on Cortex-M MCUs
- Robustness analysis across aging and temperature
- Integration into a closed-loop BMS simulation
- Hardware-in-the-loop (HIL) validation

---

## 📄 Project Report

The complete project report is available in:

