# Enhanced Colon Cancer Diagnosis via Dilated Residual SqueezeNet (DRCS-Net)

This repository contains an enhanced deep learning approach for colon cancer classification using histopathological images. The project explores three SqueezeNet-based architectures and evaluates their performance for accurate and lightweight medical image classification.

### Model Variants Evaluated
- Residual SqueezeNet with Dilation  
- Residual SqueezeNet without Dilation  
- SqueezeNet with Dilation  

---

## Dataset

Dataset Sources:  
- https://github.com/tampapath/lung_colon_image_set  
- https://www.kaggle.com/datasets/andrewmvd/lung-and-colon-cancer-histopathological-images

### Dataset Summary

| Property | Description |
|--------|-------------|
| Total Images | ~10,000 |
| Classes | Adenocarcinoma vs Benign |
| Original Resolution | 768×768 |
| Model Input Resolution | 224×224 |
| Split | 50% Train / 25% Validation / 25% Test |

### Sample Images
<p align="center">
  <img src="images/colonca991.jpeg" alt="Colon Adenocarcinoma" width="200">
  <img src="images/colonn947.jpeg" alt="Colon Normal Tissue" width="200">
</p>

<p align="center"><i>Figure 1: Example histopathological images from the dataset</i></p>

---

## Methodology: DRCS-Net Architecture Overview

DRCS-Net (Dilated Residual Colon SqueezeNet) enhances SqueezeNet through:

| Component | Purpose |
|----------|--------|
| Dilated Convolutions | Increases receptive field without additional parameters |
| Residual Connections | Improves gradient flow and training stability |
| Lightweight Backbone | Enables deployment in computationally constrained environments |

### Workflow
1. Data loading and preprocessing  
2. Image normalization and resizing to 224×224  
3. Training of SqueezeNet-based models  
4. Validation-based hyperparameter tuning  
5. Final evaluation and comparison of variants  

### Architecture Workflow Diagram
<p align="center">
  <img src="images/BLOCK DIAGRAM (6).jpg" width="800">
</p>

<p align="center"><i>Figure 2: Model training and inference workflow</i></p>

---

## Results

The proposed DRCS-Net-V3 variant achieved the highest performance among all tested models.

<p align="center">
  <img src="images/table.jpeg" width="500">
</p>

<p align="center"><i>Table 1: Performance comparison of model variants</i></p>

### Summary of Findings
- Accuracy up to 99.80%
- High precision (99.90%) and recall (99.60%)
- Lightweight model suitable for deployment in medical diagnostic systems
- Outperforms standard SqueezeNet and residual variants

---

## Technology Stack

| Component | Tool |
|----------|------|
| Framework | PyTorch / TorchVision |
| Model Architecture | SqueezeNet |
| Dataset | LC25000 Colon Histopathology Dataset |
| Task | Binary classification (Adenocarcinoma vs Normal Tissue) |

---

## Future Work
- Add Grad-CAM heatmaps for model interpretability  
- Deployment via a web interface or lightweight application  
- Model compression and quantization for edge deployment  
- Testing on expanded clinical datasets  

---
