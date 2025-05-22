# VIETNAMESE FOOD DETECTION & CALORIE CALCULATION

<img width="1470" alt="image" src="https://github.com/user-attachments/assets/78156919-f062-4dd2-84fe-207fb677599f" />

## 1. Overview:

This project presents a real-time Vietnamese food detection and calorie calculation system. Given an image of a dish, the system automatically identifies which Vietnamese dish it is, retrieves the ingredient breakdown, and provides a calorie estimate.

We currently support 5 popular Vietnamese dishes:

- Phở
- Bánh mì
- Bánh xèo
- Cơm tấm
- Gỏi cuốn

Demo Video: [Watch on YouTube](https://www.youtube.com/watch?v=v1RyfsgLyPY&feature=youtu.be)

## 2. Features:
+ Real-time food detection using deep learning
+ Calorie estimation using an ingredients database
+ Combines deep learning and classical computer vision
+ Lightweight model optimized for practical use
+ Trained on over 5000 images

## 3. Methodology:

We followed a multi-stage approach:

- Traditional Feature-Based Methods
Color Histograms in HSV color space
SIFT descriptors
Combined features fed to ML classifiers
Result: <20% accuracy — insufficient for real-world use
- Custom CNN
Trained from scratch
Achieved ~80% training accuracy, but severe overfitting
Validation accuracy ~30%
- Transfer Learning
EfficientNetV2: High accuracy on test set (~90%), but overfitted to controlled data
MobileNetV2: Lower training accuracy (~60%) but better generalization in real-time use
- Fusion-Based Final Model
Extracted deep embeddings from fine-tuned MobileNetV2
Fused with Color Histogram + SIFT features
Trained Random Forest classifier on fused features
Result: Real-world accuracy > 89%

=> Choose Fusion-Based Model as the final method with the result below

<img width="674" alt="image" src="https://github.com/user-attachments/assets/12f931c6-eddb-46f7-ad5a-726322cd783b" />

