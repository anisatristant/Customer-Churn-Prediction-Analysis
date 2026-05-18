# 🚀 ChurnGuard: High-Sensitivity Customer Churn Analytics

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![XGBoost](https://img.shields.io/badge/Model-XGBoost-orange?logo=xgboost)
![SMOTE](https://img.shields.io/badge/Sampling-SMOTE-green)

## 📌 1. Project Overview
Proyek ini bertujuan untuk membangun sistem prediksi churn pada dataset sebesar **100.000 pelanggan**. Fokus utama bukan hanya pada akurasi, melainkan pada **Recall**, untuk memastikan perusahaan tidak kecolongan pelanggan yang akan berhenti berlangganan.

---

## 📊 2. Exploratory Data Analysis (EDA)
Sebelum membangun model, dilakukan analisis mendalam untuk memahami karakteristik pelanggan.

### A. Distribusi Target
![Distribusi Churn](images/distribusi%20churn.png)

*Dataset menunjukkan adanya ketidakseimbangan data (Imbalance), di mana jumlah pelanggan loyal jauh lebih banyak dibanding yang churn.*

### B. Hubungan Perilaku dengan Churn
![Hubungan Login](images/hubungan%20hari%20terakhir%20login.png)

*Terlihat tren bahwa semakin lama pelanggan tidak melakukan login, semakin tinggi risiko mereka untuk Churn.*

### C. Korelasi Variabel
![Korelasi](images/korelasi%20atar%20variable.png)

*Analisis korelasi membantu menentukan fitur mana yang paling berpengaruh terhadap keputusan pelanggan.*

---

## ⚙️ 3. Preprocessing & Feature Engineering
Langkah-langkah yang diambil untuk menyiapkan data:
- **Pembersihan Data:** Menangani missing values pada kolom usia.
- **Encoding:** Mengubah data kategorikal (Kota, Gender, Payment Method) menjadi numerik.
- **Scaling:** Menyamakan skala data fitur numerik menggunakan `StandardScaler`.

---

## 🤖 4. Model Development (Model 1 vs Model 2)

Kami melakukan eksperimen dengan dua versi model:

### 🔴 Model 1: Baseline (Standard XGBoost)
![Confusion Matrix Baseline](images/confusion%20matrix%20baseline.png)

*Model awal memiliki **Recall 0.43**. Ini berarti 57% pelanggan churn tidak terdeteksi oleh sistem.*

### 🟢 Model 2: Optimized (SMOTE + Tuning)
![Perbandingan Model](images/grafik%20model%201%20dan%20model%202.png)

*Setelah dilakukan balancing data (SMOTE) dan penyesuaian threshold, **Recall meningkat drastis menjadi 0.91**.*

---

## 💡 5. Key Findings & Feature Importance
Variabel apa yang paling menentukan pelanggan akan kabur?
![Feature Importance](images/feature%20importance.png)

*Berdasarkan grafik di atas, perusahaan dapat memprioritaskan fitur-fitur tersebut dalam menyusun strategi promosi.*

---

## 📈 6. Performa Final Model
| Metric | Model 1 (Baseline) | Model 2 (Optimized) | Perubahan |
| :--- | :--- | :--- | :--- |
| **Recall (Churn)** | 0.43 | **0.91** | 🚀 **+111%** |
| **Accuracy** | 66% | 53% | 📉 Menurun |
| **AUC-ROC** | 0.69 | **0.70** | ✅ Stabil |

---

## 📂 Folder Structure
- `data/`: Dataset simulasi (medium_churn.csv).
- `images/`: Semua visualisasi hasil analisis dan model.
- `notebooks/`: File Jupyter Notebook (.ipynb) berisi kode lengkap.

## 👥 Contact
[Annisa Tristanti]
[https://www.linkedin.com/in/annisatristanti/] 
