# 🚀 Stable Diffusion Image Generation App

An advanced image manipulation web application built with **Streamlit** and **Stable Diffusion**. This project features Text-to-Image generation, Automatic Masking via Segmentation Models, and sophisticated Zoom-Out capabilities.

## 🌟 Key Features

### 1. Basic Generation (Txt2Img)
* **Prompting:** Full control via positive and negative prompts.
* **Hyperparameter Tuning:** Real-time adjustment of `guidance_scale` (CFG) and `num_inference_steps`.
* **Deterministic Output:** Seed control to ensure reproducible results.

### 2. Intelligent Masking & Inpainting
* **Auto-Segmentation:** Integrated **CLIPSeg** model to generate masks automatically based on text queries (e.g., "astronaut").
* **Manual Masking:** Interactive canvas powered by `streamlit-drawable-canvas` for precise manual masking control.
* **Seamless Inpainting:** Modify specific objects within an image while preserving the original background.

### 3. Advanced Outpainting (Zoom-Out)
* **Canvas Extension:** Expand images in specific directions (Left, Right, Top, or Bottom).
* **Zoom-Out Logic:** Gradually expand all sides of the image to create a "camera pulling back" effect.
* **Coherent Filling:** Utilizes a *Background Blur* technique to ensure smooth color transitions and context-aware filling in new areas.

### 4. Technical Optimizations
* **Scheduler Switcher:** Choose between `Euler A`, `DPM++`, and `DDIM` for varied diffusion behaviors.
* **Memory Management:** Dedicated "Clear Memory" button to manually free up GPU VRAM using `torch.cuda.empty_cache()`.

## 🛠️ Installation

Python 3.10+ and a CUDA-enabled GPU are recommended for optimal performance.

1. Install Dependancies:
   ```bash
   pip install -r requirements.txt
   ```
2. Run Streamlit:
   ```bash
   streamlit run app.py
   ```
