# 🌟 Stellar Age Prediction from GALAH DR4 Spectral Data Using Deep Learning

## 🧪 Context & Motivation

As part of my preparation for an upcoming erasmus+ internship involving astrophysical data analysis, I designed this project to deepen my understanding of spectroscopic datasets and machine learning applications in astronomy.  
This notebook explores how deep learning techniques can be used to predict stellar ages using the GALAH DR4 survey — one of the largest high-resolution spectroscopic datasets available.

---

## 🧭 Project Overview

The project is organized into four main sections:

---

## 1️⃣ Data Analysis

- Selected a subset of the GALAH DR4 dataset by focusing on meaningful spectroscopic and stellar parameters.
- Reduced dimensionality to focus on 131 relevant features.
- Performed exploratory data analysis (EDA) using histograms, scatter plots, and correlation analysis.
- Visualizations helped understand the age distribution, feature relationships, and potential outliers in the dataset.

---

## 2️⃣ Data Processing

- Handled missing values:
  - Imputed missing data where appropriate.
  - Removed rows with excessive missingness or invalid values.
- Normalized all numerical features for neural network input.
- Final shape of the dataset: `900,000 samples × 131 features`

---

## 3️⃣ Creating the Model

- Built a **neural network regression model** using TensorFlow/Keras.
- Architecture:
  - Dense layers with ReLU activation
  - Output: 1 node (regression target = stellar age)
- Trained for 80 epochs with a batch size tuned to GPU capacity.
- Used `mean_squared_error` as the loss function and `Adam` as the optimizer.

---

## 4️⃣ Model Evaluation

The model's performance was evaluated using multiple regression metrics:

| Metric | Value |
|--------|-------|
| **Mean Absolute Error (MAE)** | `0.6188` |
| **Mean Squared Error (MSE)**  | `0.6485` |
| **Explained Variance Score**  | `0.9679` (out of 1) |

Visualizations included:
- **Training vs Validation Loss** over epochs
- **Scatter plot** comparing true vs. predicted ages
- Optional zoomed-in and filtered views
- Manual inspection of the first 10 prediction results

The model achieved **high accuracy** in age prediction across the dataset, which ranges from ~0 to ~15 billion years.

---

## 🔍 Final Checks

To assess model reliability beyond metrics:
- Compared the predicted vs. actual ages for the first 10 test samples.
- Plotted residual errors to evaluate model consistency and outliers.


---

## 🚀 Tools Used

- Python, Pandas, NumPy
- TensorFlow / Keras
- Astropy (for FITS file handling)
- Matplotlib for visualizations

---

### 🔗 Dataset

The GALAH DR4 dataset is publicly available at:

[GALAH DR4 Website](https://www.galah-survey.org)

Due to size and license limitations, the dataset is not included in this repository.

---

## 📌 Note

This project was developed as a **self-directed learning initiative** to support future research and internship work on similar spectroscopic datasets.

> ⭐️ *Prepared using real stellar data from the GALAH DR4 survey. All code and analysis are available in the accompanying Jupyter Notebook.*
