# Multimodal Zero-Shot Detection and Vision–Language Models for Scalable Aquaculture Image Understanding

This repository provides the official implementation and dataset resources for the paper:

**Multimodal Zero-Shot Detection and Vision–Language Models for Scalable Aquaculture Image Understanding**

The project demonstrates how modern visual computing pipelines—combining zero-shot foundation models, vision–language models (VLMs), and geometry-aware visual representations—can enable scalable, low-annotation image understanding for aquaculture applications.

---
## 📌 Overview
Accurate identification and grading of aquaculture species (fish, shellfish, eel, shrimp) is essential for quality control, yield estimation, and farm management. Traditional computer vision approaches require extensive manual annotation, limiting scalability and deployment.
This work proposes a **multimodal, annotation-efficient workflow** that integrates:
- **Zero-shot object detection and segmentation**
- **Vision–Language Models (VLMs) with prompt-based reasoning**
- **Automatic dataset generation with polygon masks and bounding boxes**
- **Geometry-aware morphological feature extraction**
A shrimp posture classification case study demonstrates the effectiveness of the proposed pipeline.


## 🧠 Methodology
The workflow consists of four main stages:

1. **Zero-Shot Detection & Segmentation**
   - Foundation models (LLMDet, SAM2) automatically generate bounding boxes and polygon segmentation masks without manual labels.
2. **Dataset Construction**
   - Auto-generated annotations include:
     - Polygon masks
     - Bounding boxes
     - Textual posture labels (`straight`, `semi-curved`, `curved`)
   - The resulting dataset is released as open-source.
3. **Vision–Language Model Reasoning**
   - Prompt-based posture classification using six open-source VLMs:
     - Qwen2.5-VL  
     - Gemma3  
     - Phi4  
     - Ovis2  
     - InternVL  
     - Eagle  
4. **Geometry-Aware Feature Extraction**
   - Morphological contour features extracted from segmentation masks:
     - Skeleton length
     - Area
     - Width
     - Perimeter  
   - Enables downstream machine learning and grading tasks.

---
## 📊 Key Results

- Lightweight VLM **Ovis2-4B** achieves **79% F1-score** on shrimp posture classification.
- Demonstrates feasibility of **prompt-based multimodal learning** for appearance-based assessment.
- Eliminates the need for large-scale manual annotation.
- Scalable to other visual inspection and grading domains.
---

📦 Dataset
Auto-generated polygon masks and bounding boxes
Textual posture annotations
Suitable for:
Grading
Classification
Multimodal learning
Shape-based analysis
The dataset can be used independently for research in visual computing and aquaculture automation.

🔬 Applications
Intelligent aquaculture grading
Automated quality inspection
Generalized zero-shot dataset creation pipelines

