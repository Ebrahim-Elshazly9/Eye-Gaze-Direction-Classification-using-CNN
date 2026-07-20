# 👁️ Eye Gaze Direction Classification using CNN

A deep learning project that classifies eye gaze direction from grayscale eye images using a Convolutional Neural Network (CNN). The model is implemented with TensorFlow and Keras and trained with image augmentation techniques to improve generalization.

---

## 📌 Project Overview

![Project Banner]Project Overview.png)

This project focuses on predicting the direction of a person's eye gaze using computer vision and deep learning. A custom CNN model is trained on an eye image dataset containing four gaze classes.

The project includes:

- Image preprocessing
- Data augmentation
- CNN model development
- Model training with callbacks
- Performance evaluation
- Confusion matrix and classification report

---

## 🚀 Features

- Custom CNN architecture
- Batch Normalization & Dropout
- Image augmentation
- EarlyStopping
- ReduceLROnPlateau
- ModelCheckpoint
- Performance visualization
- Confusion Matrix
- Classification Report

---

## 🛠️ Tech Stack

- Python
- TensorFlow
- Keras
- OpenCV
- NumPy
- Scikit-learn
- Matplotlib
- Pandas
- KaggleHub

---

## 📂 Dataset

Dataset used:

**Eye Dataset** from Kaggle

The dataset contains four eye gaze classes:

- 👀 Forward Look
- 😑 Close Look
- 👉 Right Look
- 👈 Left Look

The dataset is downloaded automatically using **KaggleHub**.

---

## 📁 Project Structure

```
Eye-Gaze-Direction-Classification/
│
├── dataset/
│
├── models/
│   └── best_model.keras
│
├── notebook/
│   └── CNN_for_Eye_dataset.ipynb
│
├── results/
│   ├── accuracy.png
│   ├── loss.png
│   └── confusion_matrix.png
│
├── requirements.txt
└── README.md
```

---

## 🧹 Data Preprocessing

The images are processed before training by:

- Converting images to grayscale
- Resizing images to **128 × 128**
- Pixel normalization (`rescale = 1/255`)
- Splitting the dataset into:
  - Training
  - Validation (15%)
  - Test

---

## 🔄 Data Augmentation

Training images are augmented using:

- Rotation (10°)
- Zoom
- Width Shift
- Height Shift
- Horizontal Flip

These techniques improve model robustness and reduce overfitting.

---

## 🧠 CNN Architecture

The model consists of multiple convolutional blocks followed by fully connected layers.

Architecture:

```
Input (128 × 128 × 1)
        │
Conv2D (32)
        │
BatchNormalization
        │
MaxPooling
        │
Conv2D (64)
        │
BatchNormalization
        │
MaxPooling
        │
Conv2D (128)
        │
BatchNormalization
        │
MaxPooling
        │
Flatten
        │
Dense
        │
Dropout
        │
Dense (Softmax)
```

---

## ⚙️ Training

The model is trained using:

- Optimizer: Adam
- Loss Function: Categorical Crossentropy
- Epochs: Up to **150**
- Callbacks:
  - EarlyStopping
  - ReduceLROnPlateau
  - ModelCheckpoint

---

## 📈 Evaluation

Model performance is evaluated using:

- Accuracy
- Confusion Matrix
- Classification Report
- Precision
- Recall
- F1-Score

Training history includes:

- Training Accuracy
- Validation Accuracy
- Training Loss
- Validation Loss

---

## ▶️ Run the Project

### Install dependencies

```bash
pip install -r requirements.txt
```

### Open the notebook

```bash
jupyter notebook CNN_for_Eye_dataset.ipynb
```

or

```bash
jupyter lab
```

Run all notebook cells to:

1. Download the dataset
2. Prepare the images
3. Train the CNN
4. Evaluate the model
5. Save the best model

---

## 📊 Output

The notebook generates:

- Trained CNN model
- Accuracy & Loss curves
- Confusion Matrix
- Classification Report
- Test Accuracy

---

## 💡 Applications

- Human-Computer Interaction (HCI)
- Driver Monitoring Systems
- Eye-controlled Interfaces
- Accessibility Applications
- Smart Assistive Systems
- Attention Tracking

---

## 🔮 Future Improvements

- Transfer Learning (EfficientNet, MobileNet)
- Real-time webcam prediction
- Eye tracking integration
- TensorFlow Lite deployment
- Mobile application support
- Vision Transformer (ViT)

---

## 👨‍💻 Author

**Ebrahim Elshazly**

AI Engineer | Machine Learning | Deep Learning | Computer Vision

---

## 📄 License

This project is released under the MIT License.
