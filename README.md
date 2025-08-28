# Clothing Detection and Isolation

A computer vision project exploring **clothing segmentation and identification** using **Mask R-CNN** with the **Fashionpedia dataset**.  
Developed at the **University of Michigan**.

---

## 📖 Overview
In today’s digital age, users often encounter clothing items in images (social media, fashion blogs, online ads) that they wish to purchase but cannot easily identify or locate online.  
This project explores building a system to **automatically isolate clothing items from images** and **identify them by searching for similar pieces** online.

The project leverages **Detectron2’s Mask R-CNN** model and the **Fashionpedia dataset** to evaluate how deep learning can be used for fashion analysis.

---

## 🔍 Problem Statement
- People often see clothing online without a direct way to find it.
- Need a system that can:
  1. Detect and isolate clothing from images.
  2. Identify similar items through image-based search.
- Challenges include:
  - Clothing diversity (styles, fabrics, poses).
  - Computational costs for fine-tuning & real-time inference.

---

## 📚 Related Work
- **Mask R-CNN**: High accuracy for instance segmentation, but computationally expensive.
- **YOLO**: Great for fast detection, but lacks pixel-wise segmentation.
- **Fashion-MNIST**: Too low resolution for practical use.
- **Fashionpedia dataset**: Provides high-quality clothing annotations across 46 categories.

---

## 🛠️ Method

### High-Level Workflow
1. **Data Preparation** – Preprocess Fashionpedia images for Detectron2.  
2. **Segmentation** – Apply Mask R-CNN to detect & isolate clothing.  
3. **Evaluation** – Metrics: Intersection over Union (IoU), Mean Average Precision (mAP).  

### Model Details
- **Architecture**: Mask R-CNN w/ ResNet-50 + FPN.  
- **Dataset**: Fashionpedia (46 clothing categories).  
- **Batch Size**: 2 images/iteration.  
- **Learning Rate**: 0.001.  
- **Max Iterations**: 5000.  
- **ROI Head Batch Size per Image**: 512.  
- **Evaluation Metrics**: IoU, mAP.  

---

## 📊 Results
- Improved IoU for common clothing categories.  
- Struggled with **overlapping items** & **complex backgrounds**.  
- Limited by **computational resources** (iterations, tuning).  
- Image extraction postponed due to low-quality bitmasks.  

---

## ✅ Conclusion
- Mask R-CNN showed moderate success in segmentation.  
- Identification task remained incomplete due to resource limits.  
- Key takeaways:
  - Hyperparameter tuning and longer training needed.  
  - Cropping & feature extraction require refinement.  
  - With more compute, model performance can improve significantly.  

This project provides a **foundation for future work** in fashion recognition and search systems.

---

## 📎 References
1. P. Potrimba, *What is Mask R-CNN? The Ultimate Guide*, Roboflow, 2023. [Link](https://blog.roboflow.com/mask-rcnn/)  
2. J. Redmon, *YOLO: Real-Time Object Detection*, 2018. [Link](https://pjreddie.com/darknet/yolo/)  
