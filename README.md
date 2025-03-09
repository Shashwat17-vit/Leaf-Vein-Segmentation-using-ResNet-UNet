# Tomato Leaf Vein Segmentation Using Deep Learning

## 1. Introduction

This project was undertaken as part of a **Kaggle Hackathon Challenge**, focusing on **infected tomato leaf vein segmentation**. The goal was to develop a deep learning model capable of accurately identifying infected regions in tomato leaves, aiding early disease detection in agriculture. 

We employed a **U-Net architecture with a ResNet backbone**, leveraging **data augmentation** techniques to enhance generalization despite the small dataset. The model was evaluated using key segmentation metrics like **IoU (Intersection over Union) and Dice Coefficient**.

---

## 2. Dataset and Preprocessing

### Dataset Overview
The dataset consisted of **tomato leaf images**, each labeled with corresponding masks indicating infected regions. The dataset was split into **training, validation, and test sets** for robust model evaluation.

### Image Preprocessing
To improve model performance, we applied several preprocessing techniques:
- **Grayscale Conversion:** Extracted the red channel for better disease visibility.
- **CLAHE (Contrast Limited Adaptive Histogram Equalization):** Enhanced contrast in the images.
- **Normalization:** Rescaled pixel values to the range [0,1] for efficient training.

**Example Preprocessed Image:**

![Preprocessed Tomato Leaf](path/to/image)

---

## 3. Model Architecture and Training

### U-Net with ResNet Backbone
We utilized a **ResNet-based U-Net**, known for its effectiveness in medical and agricultural segmentation tasks. The architecture includes:
- **Encoder:** Pretrained ResNet layers extract high-level features.
- **Bottleneck:** Convolutional layers for feature fusion.
- **Decoder:** Up-sampling layers reconstruct the segmented image.

### Data Augmentation
Since the dataset was small, we implemented augmentation techniques like:
- **Rotation, Flipping, and Zooming** to improve generalization.
- **Elastic Transformations** to mimic natural variations in leaf patterns.

### Training Setup
- **Optimizer:** Adam
- **Loss Function:** IoU loss to optimize segmentation performance.
- **Evaluation Metrics:** IoU Score and Dice Coefficient

**Training Performance Over Epochs:**

![Training vs. Validation Accuracy](path/to/image)

---

## 4. Results and Evaluation

### Performance Metrics
Our final model achieved the following:
- **IoU Score:** 0.85 (higher is better)
- **Dice Coefficient:** 0.89 (indicating good segmentation overlap)

### Visualizing Predictions
Below are examples of model predictions vs. ground truth:

| Input Image | Ground Truth | Model Prediction |
|------------|-------------|------------------|
| ![Input](path/to/image) | ![Mask](path/to/image) | ![Prediction](path/to/image) |

The model successfully segments infected regions, demonstrating its utility in agricultural disease detection.

---

## 5. Conclusion and Future Work

This project showcased the power of **deep learning in agricultural disease detection**. By leveraging **ResNet-based U-Net and augmentation techniques**, we achieved **high segmentation accuracy** even with a limited dataset.

### Future Improvements:
- **Train on a larger dataset** for better generalization.
- **Implement transformer-based segmentation models** like SegFormer for potential performance gains.
- **Deploy as a real-time mobile application** for farmers to detect infections on-site.

This work is a step towards **AI-powered precision agriculture**, enabling **early disease detection and better crop yield management**.

---

## Acknowledgment
This project was developed as part of a Kaggle Hackathon, leveraging cutting-edge deep learning techniques for real-world impact.
