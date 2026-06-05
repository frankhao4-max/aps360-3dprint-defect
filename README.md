# APS360 Project — Automated FDM 3D Print Defect Detection

**Course:** APS360 Applied Fundamentals of Deep Learning, Summer 2026  
**Author:** Frank Hao
**University of Toronto**

---

## Project Summary

This project trains a multi-class CNN classifier to identify FDM 3D
print defects — stringing, warping, layer shift, under-extrusion, and
over-extrusion — from webcam images captured mid-print. The goal is a
real-time quality control system that can automatically pause a printer
when a defect is detected.

## Defect Classes

| Class | Description |
|-------|-------------|
| Normal | Print proceeding correctly |
| Stringing | Thin filament strands between structures |
| Warping | Print peeling or lifting from the bed |
| Layer Shift | Layers misaligned mid-print |
| Under-extrusion | Insufficient filament flow |
| Over-extrusion | Excess filament causing blobs or clogs |

## Model Approach

- **Backbone:** EfficientNet-B0 pretrained on ImageNet (fine-tuned)
- **Training:** PyTorch with two-stage fine-tuning
- **Baseline:** HOG + SVM (scikit-learn)

## Dataset

- [Obico Open Dataset](https://github.com/TheSpaghettiDetective/obico-server) (~15,000 images)
- Kaggle "3D Printing Failures" dataset (~3,000 images)
- Self-collected images from a personal FDM printer

## Repository Structure
