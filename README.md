# 🧠 Mental Wellbeing Classification using Machine Learning

Analisis Kesejahteraan Mental Menggunakan Model Machine Learning pada Dataset **DigitalExposome**    


---

## 📘 Deskripsi Singkat

Proyek ini bertujuan untuk mengklasifikasikan tingkat kesejahteraan mental seseorang berdasarkan data **lingkungan dan fisiologis** yang diperoleh secara real-time dari dataset **DigitalExposome**. 

Dengan menggunakan algoritma supervised learning, sistem dapat memprediksi skor kesejahteraan mental (label 1–5) secara akurat.

---

## 🎯 Tujuan Penelitian

- Mengembangkan model klasifikasi tingkat kesejahteraan mental dari data real-time.
- Menganalisis pengaruh fitur lingkungan dan fisiologis terhadap prediksi kesejahteraan.
- Mengevaluasi dan membandingkan performa beberapa model machine learning.

---

## 📊 Dataset

- 📁 **DigitalExposome Dataset**  
  42.436 entri dari 40 partisipan
- 🔍 **Fitur Fisiologis**:  
  - HR (Heart Rate), HRV (IBI), EDA, BVP
- 🌿 **Fitur Lingkungan**:  
  - PM1, PM2.5, PM10, CO, NO2, NH3, Noise
- 🎯 **Target**:  
  - Label kesejahteraan mental (1 = sangat buruk, 5 = sangat baik)

---

## ⚙️ Preprocessing

- Normalisasi Min-Max (0–1)
- Resampling dan interpolasi ke 1Hz
- Data sudah bersih tanpa missing value
- Stratified Split:
  - 70% Training (29.705)
  - 30% Testing (12.731)

---

## 🤖 Model yang Digunakan

| Model              | Parameter Utama              | Akurasi  |
|--------------------|------------------------------|----------|
| Decision Tree      | `max_depth = 8`              | 71.6%    |
| Random Forest      | `n_estimators = 100`, `max_depth = 10` | 90.1% |
| k-Nearest Neighbors| `k = 5`, Euclidean Distance  | **94.8%** ✅ |

---

## 🧠 Feature Importance

Fitur paling berpengaruh berdasarkan Random Forest:
- **Heart Rate (HR)**
- **Carbon Monoxide (CO)**
- **Electrodermal Activity (EDA)**
- **Heart Rate Variability (HRV)**

📌 Insight: **Faktor fisiologis** lebih menentukan kesejahteraan mental dibandingkan lingkungan sekitar.

---

## 📈 Evaluasi Model

- Classification Report: precision, recall, f1-score
- Confusion Matrix: akurat untuk label 1 & 5, kesalahan pada 2–4
- PCA digunakan untuk visualisasi distribusi label

---

## ✅ Hasil & Kesimpulan

- Dataset DigitalExposome sangat cocok untuk klasifikasi kesejahteraan mental
- **k-NN** menjadi model terbaik dengan akurasi **94.8%**
- Wearable device dengan pengukuran HR, HRV, dan EDA berpotensi tinggi digunakan dalam sistem prediksi kesejahteraan real-time

---
