**🍜 Vietnamese Food Detection & Calorie Calculation
**

📌 Overview

This project presents a real-time Vietnamese food detection and calorie calculation system. Given an image of a dish, the system automatically identifies which Vietnamese dish it is, retrieves the ingredient breakdown, and provides a calorie estimate.

We currently support 5 popular Vietnamese dishes:

Phở
Bánh mì
Bánh xèo
Cơm tấm
Gỏi cuốn
🔗 Demo Video: [Watch on YouTube](https://www.youtube.com/watch?v=v1RyfsgLyPY&feature=youtu.be)

🚀 Features

Real-time food detection using deep learning
Calorie estimation using an ingredients database
Combines deep learning and classical computer vision
Lightweight model optimized for practical use
Trained on over 5000 images
🧠 Methodology

We followed a multi-stage approach:

1. 📷 Traditional Feature-Based Methods
Color Histograms in HSV color space
SIFT descriptors
Combined features fed to ML classifiers
Result: <20% accuracy — insufficient for real-world use
2. 🧪 Custom CNN
Trained from scratch
Achieved ~80% training accuracy, but severe overfitting
Validation accuracy ~30%
3. 🔁 Transfer Learning
EfficientNetV2: High accuracy on test set (~90%), but overfitted to controlled data
MobileNetV2: Lower training accuracy (~60%) but better generalization in real-time use
4. 🧬 Fusion-Based Final Model
Extracted deep embeddings from fine-tuned MobileNetV2
Fused with Color Histogram + SIFT features
Trained Random Forest classifier on fused features
Result: Real-world accuracy > 89%
📊 Results

Dish	CNN Accuracy	Fusion Model Accuracy
Phở	6.17%	93.21%
Bánh mì	24.53%	92.45%
Bánh xèo	42.55%	92.77%
Gỏi cuốn	1.16%	84.30%
Cơm tấm	53.97%	86.24%
