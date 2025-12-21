# Industrial-Diagnostic-Model-DEMO
This project is a demonstration platform for large language models in industrial rotating machinery diagnostics, developed by the Intelligent Manufacturing and Quality Engineering Laboratory at CityUHK

> **A Multi-modal Industrial Agent combining Large Language Models (LLM) with Domain-Specific Deep Learning for offline, edge-computing environments.**

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python](https://img.shields.io/badge/Python-3.10%2B-green)](https://www.python.org/)
[![Model](https://img.shields.io/badge/LLM-Qwen2.5--14B--Int4-purple)](https://huggingface.co/Qwen)
[![Device](https://img.shields.io/badge/Edge-RTX%204090-orange)](https://www.nvidia.com/)

---

## 🎥 Video Demo 

Click the button below to watch the full demonstration:

[![Watch on Bilibili](https://img.shields.io/badge/Bilibili-Watch_Video-00A1D6?style=for-the-badge&logo=bilibili&logoColor=white)](https://www.bilibili.com/video/BV1cTqUBYER8)

##  Overview

**Roto-LLM-Agent** is an intelligent diagnostic system designed for **isolated industrial environments** (e.g., ocean-going vessels, remote wind farms) where internet connectivity is limited or unavailable. 

By leveraging the **Function Calling** capabilities of quantized Large Language Models (Qwen 2.5-14B-Int4), this system acts as a "Virtual Mechanical Engineer." It autonomously orchestrates specialized Python tools to process high-frequency vibration signals and provides comprehensive fault analysis without relying on cloud resources.

![Overview](https://github.com/user-attachments/files/24277103/capture_20251221123419892.bmp)



##  Key Features

The system integrates a generic cognitive core (LLM) with a specialized perception engine (CNN/Transformer), offering four distinct capabilities:

### 1.  Intelligent Data Inspection
The agent can autonomously navigate and inspect raw industrial data files (CSV/Metadata) to understand the operating conditions before diagnosis.
- **Capability:** Reads metadata, checks sensor configurations, and summarizes dataset structures.
- **User Prompt Example:** *"Check what is inside the test metadata file."*
  
![Data Inspection](https://github.com/user-attachments/files/24277107/capture_20251221123452450.bmp)


### 2.  Signal Visualization & Analysis
Bridge the gap between raw numbers and visual intuition. The system dynamically generates high-resolution time-domain waveform plots from compressed signal files (`.npz`).
- **Capability:** Parses vibration data, applies visualization standards (customized specifically for periodic mechanical signals), and renders high-quality waveform images for user review.
- **User Prompt Example:** *"Plot the signal waveform for row 5 to check for periodic impacts."*
  
![Signal Visualization](https://github.com/user-attachments/files/24277108/capture_20251221123536918.bmp)


### 3.  Deep Learning-Based Fault Diagnosis
At the core is a specialized **Multi-Task CNN-Transformer Hybrid Model** optimized for rotating machinery.
- **Capability:** The LLM invokes the backend inference engine to classify faults across **Rotor** (6 classes) and **Bearing** (8 classes) components simultaneously.
- **Flexibility:** Supports both **Batch Evaluation** (assessing overall fleet health) and **Specific Instance Diagnosis** (pinpointing issues in a specific timestamp).
- **User Prompt Example:** *"Run the fault diagnosis model for the 3rd data sample."*
  
![Fault Diagnosis](https://github.com/user-attachments/files/24277110/capture_20251221123618404.bmp)


### 4.  Root Cause Analysis & Traceability (Fault Sourcing)
Going beyond simple classification labels, the system utilizes the LLM's vast internal knowledge base to provide **physically grounded explanations**.
- **Capability:** After obtaining the diagnosis result (e.g., *Inner Race Fault* + *Rotor Unbalance*), the agent analyzes the combination of states to infer potential physical causes (e.g., lubrication failure, fatigue spalling, or installation misalignment).
- **Value:** Turns "Black Box" predictions into actionable maintenance insights.
- **User Prompt Example:** *"The diagnosis shows an Inner Race fault combined with misalignment. What are the likely physical causes for this specific combination on a high-speed shaft?"*

![Root Cause Analysis](https://github.com/user-attachments/files/24277111/capture_20251221123702477.bmp)

