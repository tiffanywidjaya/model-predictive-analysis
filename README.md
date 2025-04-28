# Predictive Analytics Project: Credit Risk Prediction

## Domain Project
Pada proyek ini, dilakukan prediksi risiko kredit untuk menentukan apakah seorang nasabah berpotensi mengalami gagal bayar atau tidak. 
Masalah ini penting karena dapat membantu lembaga keuangan dalam mengambil keputusan pemberian pinjaman.

## Business Understanding
**Problem Statement:**
- Bagaimana cara memprediksi apakah nasabah akan mengalami gagal bayar berdasarkan data demografis dan keuangan mereka?

**Goals:**
- Membangun model klasifikasi untuk memprediksi risiko gagal bayar pinjaman.

**Solution Statement:**
- Mencoba dua model Machine Learning: Logistic Regression (dengan scaling) dan Decision Tree Classifier (tanpa scaling).
- Memilih model dengan performa terbaik berdasarkan metrik evaluasi klasifikasi.

## Data Understanding
- Dataset: Credit Risk Dataset
- Jumlah Data: (Tulis jumlah baris dan kolom dari `data.shape`)
- Sumber Dataset: [Kaggle - Credit Risk Dataset](https://www.kaggle.com/datasets/zaurbegiev/my-dataset)

**Fitur pada dataset:**
(Tulis daftar fitur berdasarkan `data.columns` + sedikit penjelasan.)

Contoh:
- person_age: Umur peminjam
- person_income: Pendapatan peminjam
- person_home_ownership: Status kepemilikan rumah
- loan_status: Target (1 = gagal bayar, 0 = tidak gagal bayar)
(dan seterusnya)

## Data Preparation
- Encoding fitur kategorikal menggunakan LabelEncoder.
- Mengisi missing value menggunakan median.
- Scaling fitur numerik menggunakan StandardScaler untuk model Logistic Regression.
- Membuat dua dataset:
  - Data scaled untuk Logistic Regression.
  - Data raw untuk Decision Tree.

## Modeling
- Model 1: Logistic Regression (dengan scaling)
- Model 2: Decision Tree Classifier (tanpa scaling)

**Parameter default** digunakan pada kedua model.

## Evaluation
**Metrik Evaluasi:**
- Classification Report: Precision, Recall, F1-Score
- Confusion Matrix
- Accuracy Score

**Hasil Evaluasi:**
(Tulis hasil accuracy Logistic Regression dan Decision Tree kamu di sini.)

Contoh:
- Logistic Regression Accuracy: 83.5%
- Decision Tree Accuracy: 81.2%

**Pemilihan Model Terbaik:**
(Di sini tulis: "Model dengan accuracy lebih tinggi dipilih sebagai model akhir." atau "Model yang balanced precision-recall lebih dipilih", terserah sesuai hasilmu.)

## Conclusion
Model yang dibangun dapat membantu dalam memprediksi risiko kredit berdasarkan data pelanggan. Model terbaik yang dipilih adalah (Logistic Regression / Decision Tree) berdasarkan hasil evaluasi metrik klasifikasi.
