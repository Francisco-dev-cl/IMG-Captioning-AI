# AI Image Captioning Tool (BLIP & Gradio)

A Computer Vision and Generative AI application that generates contextual image captions using Hugging Face's **BLIP (Bootstrapping Language-Image Pre-training)** model and an interactive **Gradio** web interface.

## 🎯 Key Features
* **Deep Learning Inference:** Utilizes `Salesforce/blip-image-captioning-base` for conditional and unconditional image descriptions.
* **Multimodal Processing:** Converts NumPy arrays and images into PyTorch tensors for Transformer models.
* **Interactive Web UI:** Built with Gradio for real-time drag-and-drop image captioning.
* **Standalone Scripts:** Includes decoupled scripts for local testing and automation.

## 📁 Repository Structure
* **`image_captioning_app.py`**: The core Gradio web application that processes user-uploaded images via Pillow and returns generated text.
* **`image_cap.py`**: An offline testing script that loads the Salesforce processor and model to analyze a local sample image (`Hotaru_Tomoe_Black.png`).

## 🛠 Tech Stack
* **AI/ML:** Hugging Face Transformers (`AutoProcessor`, `BlipForConditionalGeneration`), PyTorch
* **Interface & Processing:** Gradio, Pillow (PIL), NumPy, Python 3.x

## 🚀 Quickstart Guide

### 1. Clone & Install Dependencies
```bash
git clone https://github.com
cd IMG-Captioning-AI
pip install transformers torch gradio pillow numpy requests
```

### 2. Run the Application or Test Script
* **Launch Web UI:** `python image_captioning_app.py` (accessible at `http://127.0.0.1:7860`)
* **Run Console Test:** `python image_cap.py`

## 📈 Technical Highlights
* **Rapid Prototyping:** Bridges complex deep learning models with functional web interfaces.
* **Multimodal Pipelines:** Integrates Computer Vision with Natural Language Processing.
* **Modular Code:** Clean separation between UI layers and core model logic.
