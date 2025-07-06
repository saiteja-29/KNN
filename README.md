# KNN Image Classifier on CIFAR-10 with PCA

This project implements a simple **K-Nearest Neighbors (KNN)** classifier on the **CIFAR-10 dataset**, using **image flattening**, **normalization**, and **Principal Component Analysis (PCA)** for dimensionality reduction. It also allows predicting the class of a **custom image from a URL**.

---

## 📦 Features

- ✅ Loads and preprocesses CIFAR-10 dataset
- ✅ Implements a basic KNN classifier from scratch (no scikit-learn)
- ✅ Normalizes pixel values to [0, 1] for better distance performance
- ✅ Applies PCA to reduce dimensionality (e.g., 3072 → 100)
- ✅ Predicts labels for test set and calculates accuracy
- ✅ Supports prediction on custom images via URL

---

## 🧠 Dataset: CIFAR-10

CIFAR-10 is a dataset of 60,000 32x32 color images in 10 classes:
- `airplane`, `automobile`, `bird`, `cat`, `deer`, `dog`, `frog`, `horse`, `ship`, `truck`

---

## 🚀 How It Works

1. **Data Loading**  
   Loads CIFAR-10 data from `tensorflow.keras.datasets`.

2. **Preprocessing**  
   - Reshapes images to flat vectors (`32x32x3 → 3072`)
   - Normalizes values (`/255.0`)
   - Applies PCA (`sklearn.decomposition.PCA`) to reduce dimensionality

3. **KNN Classification**  
   - Uses Euclidean distance to find the `k` nearest neighbors
   - Predicts the majority label among them

4. **Prediction on Custom Image**  
   - Downloads an image from a URL
   - Resizes to 32x32
   - Normalizes and flattens
   - Applies the same PCA transform
   - Predicts the class

---

## 📈 Sample Output

