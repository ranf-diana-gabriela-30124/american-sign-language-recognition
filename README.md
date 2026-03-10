# ASL Hand Gesture Recognition

**ASL Hand Gesture Recognition** is a deep learning project for recognizing **American Sign Language (ASL) letters** using a CNN with TensorFlow/Keras. Includes image preprocessing, data augmentation, median filtering, and a live webcam demo.

---

## Project Overview

This project detects hand gestures corresponding to ASL letters. It preprocesses images, applies data augmentation, trains a CNN model, and evaluates its performance. A live demo allows real-time detection using a webcam.

---

## Features

- **Preprocessing:** resize, normalize, median filter  
- **Augmentation:** rotation, zoom, translation, contrast  
- **CNN Model:** 4 Conv2D blocks + Dense + Dropout  
- **Dataset Split:** 70% train, 15% validation, 15% test  
- **Evaluation:** accuracy, confusion matrix, per-class reports  
- **Live Demo:** ASL letter recognition with visual feedback

---

## Dataset

- Images are organized in folders per class (A-Z)  
- Each folder contains JPEG/PNG images of the corresponding hand sign  
- Duplicate and corrupted images are automatically detected and removed during preprocessing  

---

### Usage Instructions

- Press **'s'** to predict the gesture in the ROI  
- Press **'q'** to quit the demo  
- The blue rectangle marks the region of interest

---

### Model Architecture

- Input: (64,64,3) RGB images  
- 4 convolutional blocks: Conv2D -> BatchNorm -> MaxPool  
- Flatten + Dense(512) + BatchNorm + Dropout(0.5)  
- Output layer: Dense(num_classes) with softmax  

- Loss: categorical_crossentropy  
- Optimizer: Adam  
- Metrics: accuracy

---

### Training & Evaluation

- Split: 70% train, 15% validation, 15% test  
- Evaluation metrics:  
  - Accuracy on train/validation/test  
  - Confusion matrix  
  - Per-class accuracy reports  
- All plots are generated during training for visual analysis

---

### Live Demo

- Detects ASL letters in real-time using a webcam  
- Displays predicted letter and confidence on screen  
- Confidence color coding:  
  - **Green:** > 85%  
  - **Red:** ≤ 85%
