# spatial_vision_ai
Local edge-AI system using Ollama to track real-time physical object coordinates and query environmental history without cloud dependencies.
Spatial Vision World Modeler

An edge-AI spatial intelligence pipeline that continuously builds and updates a real-time memory state of the physical world. Built for privacy-first environments, this system tracks spatial coordinates of objects dynamically and provides an interface to query the scene history locally.

## Key Features
* **Real-Time Spatial Logging:** Dynamically processes live camera feeds to generate structured bounding box coordinate matrices.
* **Persistent Agent Memory:** Automatically constructs a continuous JSON timeline log tracking environmental changes.
* **Local Privacy-First Query Interface:** Leverages a local LLM pipeline (via Ollama) to interpret spatial data history without relying on cloud APIs.
* **High Efficiency:** Low-latency inference designed to run directly on consumer edge devices.

---

## How It Works

1. **Vision Tracking Layer:** The system opens a localized camera feed to detect and track objects, logging their coordinate matrices into an internal state vector.
2. **Memory Updaters:** As actions occur, the system continuously updates a `raw_observation` timeline detailing object history.
3. **Natural Language Querying:** Users can query the persistent world model (e.g., asking *"What objects did you see?"*), prompting the local intelligence layer to extract semantic meaning from spatial coordinate logs.

---

## System Architecture & Tech Stack

* **Language:** Python 3.13+
* **Local Inference Engine:** Ollama (running local large language models)
* **API Communication:** Python `requests` library for zero-overhead local endpoints
* **Data Layer:** Structured JSON World Model State Management

---

## Quick Start Guide

### 1. Prerequisites
Ensure you have Python installed and the Ollama background service running with your preferred local model:
```bash
ollama run llama3

**DEMO VIDEO**
https://drive.google.com/file/d/1wOMDM_itb8MpPkc8f3iQB6bwjORLX7Nm/view?usp=drivesdk
