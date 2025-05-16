# 🐶🐱 Dog vs Cat Image Classifier using CNN

This project implements a **Convolutional Neural Network (CNN)** using TensorFlow/Keras to classify images as either **dogs** or **cats**. The model is trained on a labeled dataset and achieves over **82% validation accuracy**. It also includes evaluation visualizations and testing with a custom image.

---

## 📂 Dataset

- **Source**: [Kaggle - Dogs vs Cats Dataset](https://www.kaggle.com/datasets/salader/dogs-vs-cats)
- **Size**: ~20,000 training images, ~5,000 testing images
- **Classes**: `dog`, `cat`
- Downloaded and extracted using Kaggle API within the notebook.

---

## 🧠 Model Architecture

- CNN Layers:
  - 3 Convolutional layers (with ReLU activation)
  - MaxPooling after each conv layer
  - Batch Normalization for stability
- Dense Layers:
  - Flatten → Dense(128) → Dropout
  - Dense(64) → Dropout → Dense(1, sigmoid)

```python
Input → Conv2D(32) → MaxPool → Conv2D(64) → MaxPool → Conv2D(128) → MaxPool → Flatten → Dense(128) → Dropout → Dense(64) → Dropout → Dense(1)
