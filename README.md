# Flux Dual-Pipeline Eye Detailer for ComfyUI

A precision dual-pipeline ComfyUI workflow designed to solve common generative artifacts in human eyes (e.g., flat irises, missing lacrimal caruncles, and off-center pupils).

## 🚀 Key Features
- **Dual-Pass Refinement:** Uses custom YOLOv12-Face detection for initial alignment, followed by specialized eye segmentation via SAM (ViT-H).
- **Anatomical Accuracy:** High-detail prompt conditioning focusing on realistic sclera capillaries, natural wetness, and proper iris textures.
- **Seamless Integration:** Features Gaussian mask feathering and color matching (`hm-mkl-hm`) to ensure face identity remains untouched.

## 🛠️ Stack & Requirements
- **Models:** Flux.2 Dev (BF16), Mistral 3 Small Flux2 CLIP (BF16), Flux VAE
- **Detectors:** `yolov12l-face.pt`, `Eyes.pt` BBOX, `sam_vit_h`
- **Nodes Required:** Impact Pack, Impact Subpack, ComfyUI-KJNodes, rgthree

## 📦 How to Use
1. Download the `.json` workflow file from this repository.
2. Drag and drop it into your ComfyUI interface.
3. Ensure all required custom nodes and detection models are installed.
