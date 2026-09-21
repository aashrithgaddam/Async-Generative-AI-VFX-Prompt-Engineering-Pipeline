# Async-Generative-AI-VFX-Prompt-Engineering-Pipeline
An asynchronous Python pipeline using AsyncIO and ComfyUI/Stable Diffusion APIs to transform raw director concepts into structured, production-ready cinematic VFX prompts.
##  What is this?
This project is an **automated tool for film and VFX studios**. It takes raw creative ideas from a movie director and automatically turns them into high-quality AI image prompts. It then uses fast, parallel processing to send those prompts to local AI art generators (**Stable Diffusion / ComfyUI**) to create visual effects assets without wasting time or computer power.

---

##  Why it matters (The Problem & Solution)
* **The Problem:** In film studios, manually writing detailed AI prompts for every scene takes too long. On top of that, generating images one by one leaves expensive GPUs sitting idle.
* **The Solution:** This pipeline automates the entire process. It takes a simple concept like *"dark futuristic city"* and instantly expands it with professional movie keywords (camera types, lighting, resolutions). It then sends hundreds of these requests to the AI engine **all at the same time**, maximizing the studio's hardware efficiency.

---

##  How it works
1. **Input:** You give the pipeline a list of simple text descriptions from a director.
2. **Upgrade (Prompt Engineering):** The system automatically adds cinematic details (e.g., *Anamorphic lens, Volumetric lighting, 8K resolution*) and sets up negative prompts to filter out bad quality.
3. **Async Dispatch:** Using Python's `AsyncIO` and `HTTPX`, the pipeline sends multiple image requests to the AI server simultaneously, rather than waiting for one to finish before starting the next.
4. **VFX Generation:** Local **ComfyUI** or **Stable Diffusion** endpoints receive the commands and render the images at maximum speed.

---

##  Tech Stack
* **Language:** Python
* **Speed & Concurrency:** AsyncIO, HTTPX (for fast, overlapping network requests)
* **AI Tools:** ComfyUI API, Stable Diffusion WebUI (AUTOMATIC1111)

---

##  Quick Start

### 1. Installation
```bash
git clone https://github.com
cd async-vfx-prompt-pipeline
pip install -r requirements.txt
```

### 2. Run the Pipeline
Ensure your local ComfyUI or Stable Diffusion API is running, then execute:
```bash
python main.py
```
