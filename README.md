# Industrial-Diagnostic-Model-DEMO

This project is a demonstration platform for large language models in industrial rotating machinery diagnostics, developed by the _Intelligent Manufacturing & Quality Engineering Laboratory @ CityUHK_.

> **A Multi-modal Industrial Agent combining Large Language Models (LLMs) with Domain-Specific Deep Learning for offline, edge-computing environments.**

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python](https://img.shields.io/badge/Python-3.10%2B-green)](https://www.python.org/)
[![Model](https://img.shields.io/badge/LLM-Qwen2.5--14B--Int4-purple)](https://huggingface.co/Qwen)
[![Device](https://img.shields.io/badge/Edge-RTX%204090-orange)](https://www.nvidia.com/)

---

## 🎥 Video Demonstration

Watch the full system demonstration to see the Roto-LLM-Agent in action, featuring real-time monitoring and conversational diagnostics.

[![Watch the video](https://img.youtube.com/vi/YOUR_VIDEO_ID_HERE/maxresdefault.jpg)](YOUR_YOUTUBE_LINK_HERE)
*(Click the image above to view the demonstration on YouTube)*

---

## Overview

**Roto-LLM-Agent** is an intelligent diagnostic system designed for **isolated industrial environments** (e.g., ocean-going vessels, remote wind farms) where internet connectivity is limited or unavailable. 

By leveraging the **Function Calling** capabilities of quantized Large Language Models (Qwen 2.5-14B-Int4), this system acts as a "Virtual Mechanical Engineer." It autonomously orchestrates specialized Python tools to process high-frequency vibration signals and provides comprehensive fault analysis without relying on cloud resources.

<img width="7384" height="3548" alt="封面" src="https://github.com/user-attachments/assets/ce22f967-dcad-402d-907f-e50530cf4dd1" />


---

## Key Features

The system integrates a generic cognitive core (the LLM) with a specialized perception engine (a Multi-Task CNN/Transformer hybrid model). This architecture offers a comprehensive suite of diagnostic capabilities through both graphical UI interactions and flexible natural language prompts.

### 1. Continuous Signal Monitoring & Data Inspection
The system continuously ingests and processes high-frequency vibration data streams in real-time. In this mode, the agent autonomously navigates raw industrial data files—such as sensor metadata and compressed signal formats (`.npz`)—to establish an operational baseline. By dynamically tracking these periodic mechanical signals, the pipeline remains primed for instantaneous anomaly detection without requiring manual data preprocessing or constant human oversight.

<img width="1230" height="640" alt="1 持续检测-1" src="https://github.com/user-attachments/assets/c2b4736c-7000-4158-9ab0-0e0d20955cd8" />


### 2. Automated Anomaly Detection & Detailed Fault Analysis
Upon detecting a mechanical deviation, the system triggers an immediate visual alert on the monitoring interface and isolates the specific fault signature. The backend **Multi-Task CNN-Transformer Hybrid Model**, which is specifically optimized for rotating machinery, takes over to classify the anomaly. It is capable of simultaneously diagnosing faults across **Rotor (6 distinct classes)** and **Bearing (8 distinct classes)** components. The LLM then structures these deep-learning outputs into a highly detailed, readable diagnostic report, bridging the gap between raw numerical predictions and actionable engineering data.

<img width="1230" height="640" alt="2 故障细节展示-1" src="https://github.com/user-attachments/assets/641850ba-2dd5-49e2-97cd-f5691ff831dc" />


### 3. Interactive System Status Evaluation
Through the integrated left-panel UI, operators can request an immediate, high-level assessment of the machinery's current operating condition. Instead of manually reviewing sensor logs, clicking the "Fault Analysis" equivalent button prompts the LLM to synthesize recent sensor configurations, operating conditions, and model outputs. The result is a concise, holistic evaluation of the system's overall health, effectively summarizing complex dataset structures into an intuitive status report.

<img width="1230" height="640" alt="3 现状分析-1" src="https://github.com/user-attachments/assets/2f2a7e16-8a88-4d48-8d33-f1c2ca9bd8f1" />


### 4. One-Click Root Cause Traceability (Fault Sourcing)
Going far beyond simple classification labels, the system utilizes the LLM's vast internal knowledge base to perform physically grounded traceability. By clicking the traceability button, the agent analyzes the specific combination of detected states (e.g., an *Inner Race Fault* combined with *Rotor Unbalance*). It then infers the underlying physical mechanisms that likely caused this specific combination on a high-speed shaft—such as lubrication failure, fatigue spalling, or installation misalignment. This feature successfully turns "Black Box" neural network predictions into transparent, actionable maintenance insights.

<img width="1230" height="640" alt="4 现状溯源-1" src="https://github.com/user-attachments/assets/eed5a95c-4790-48ac-88da-e8eefc65ac20" />


### 5. Conversational Fault Analysis (Via Natural Language)
Users are not restricted to predefined UI buttons; they can utilize the chat interface to query the system regarding specific historical anomalies. By utilizing natural language prompts (e.g., *"Check what is inside the test metadata file for the most recent fault"* or *"Run the fault diagnosis model for the 3rd data sample"*), the LLM utilizes Function Calling to dynamically invoke the required Python analysis tools. It retrieves the exact event logs and renders customized diagnostic analyses on the fly, allowing for deep-dive investigations into specific timestamps.

<img width="1230" height="640" alt="5 近况故障分析-1" src="https://github.com/user-attachments/assets/829894a0-3d27-4cdb-8706-bf7b28ca94e2" />


### 6. Conversational Maintenance Strategy Formulation
The capabilities of the "Virtual Mechanical Engineer" extend to formulating concrete, physically viable solutions. Through the conversational interface, operators can ask the LLM to propose maintenance strategies based on the newly traced root causes. The LLM synthesizes its engineering knowledge with the specific localized fault data to suggest operational adjustments, repair procedures, or part replacements. 

<img width="1230" height="640" alt="6 近况故障溯源-1" src="https://github.com/user-attachments/assets/46147954-14d6-4e34-a0b6-9fa364824442" />



*> **Note:** Features 5 and 6 illustrate the immense flexibility of the LLM core. Because it operates via natural language rather than hardcoded logic, users can freely prompt the system to execute a wide variety of custom engineering and analytical tasks beyond the standard UI functionalities.*
