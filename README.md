# Laporan Proyek Machine Learning - Predictive Analytics: Credit Risk Prediction

## Domain Proyek

Proyek ini bertujuan untuk memprediksi risiko gagal bayar kredit berdasarkan data demografis dan keuangan nasabah.  
Permasalahan ini penting karena dapat membantu lembaga keuangan dalam mengurangi risiko kerugian akibat pemberian pinjaman kepada calon nasabah yang berpotensi default.

**Referensi**:  
- Kaggle - Credit Risk Dataset [link](https://www.kaggle.com/datasets/laotse/credit-risk-dataset?resource=download)

## Business Understanding

### Problem Statements
- Bagaimana cara memprediksi apakah seorang nasabah berpotensi gagal bayar berdasarkan data demografis dan keuangan?

### Goals
- Mengembangkan model machine learning yang mampu mengklasifikasikan nasabah menjadi kategori risiko gagal bayar atau tidak.

### Solution Statements
- Mencoba dua model machine learning:
  - Logistic Regression (dengan scaling).
  - Decision Tree Classifier (tanpa scaling).
- Memilih model dengan performa terbaik berdasarkan metrik evaluasi klasifikasi (Accuracy, Precision, Recall, F1-Score).

## Data Understanding

- **Jumlah Data**: 32581 baris dan 12 kolom (dari file `credit_risk_dataset.csv`)
- **Sumber Data**: [Kaggle - Credit Risk Dataset](https://www.kaggle.com/datasets/laotse/credit-risk-dataset?resource=download)

### Fitur pada dataset:
- **person_age**: Usia peminjam dalam tahun.
- **person_income**: Pendapatan tahunan peminjam.
- **person_home_ownership**: Status kepemilikan rumah (RENT, OWN, MORTGAGE, OTHER).
- **person_emp_length**: Lama bekerja dalam tahun.
- **loan_intent**: Tujuan pinjaman (personal, medical, education, dll).
- **loan_grade**: Grade atau tingkat kualitas pinjaman.
- **loan_amnt**: Jumlah pinjaman yang diajukan.
- **loan_int_rate**: Persentase bunga pinjaman.
- **loan_percent_income**: Persentase jumlah pinjaman dibandingkan pendapatan.
- **cb_person_default_on_file**: Riwayat default kredit sebelumnya (Yes/No).
- **cb_person_cred_hist_length**: Lama riwayat kredit dalam tahun.
- **loan_status**: Target (1 = default, 0 = tidak default).

### Visualisasi Data:
- Visualisasi distribusi kelas `loan_status` menunjukkan bahwa data sedikit imbalance antara nasabah gagal bayar dan tidak.

## Data Preparation

- **Encoding**:
  - Fitur kategorikal (`person_home_ownership`, `loan_intent`, `loan_grade`, `cb_person_default_on_file`) diencoding menggunakan `LabelEncoder`.
- **Handling Missing Value**:
  - Missing value pada fitur-fitur diisi menggunakan median dari masing-masing kolom.
- **Scaling**:
  - Data di-scaling menggunakan `StandardScaler` untuk model Logistic Regression.
- **Splitting**:
  - Dataset dibagi menjadi train-test split 80:20 menggunakan `train_test_split`.

## Modeling

### Model 1: Logistic Regression
- Input: Data hasil scaling.
- Parameter: Menggunakan parameter default.
- Kelebihan: Cepat dan efisien untuk data linier.
- Kekurangan: Perlu scaling; sensitif terhadap outlier.

### Model 2: Decision Tree Classifier
- Input: Data raw (tanpa scaling).
- Parameter: Menggunakan parameter default.
- Kelebihan: Tidak butuh scaling; dapat memodelkan hubungan non-linear.
- Kekurangan: Rentan overfitting.

## Evaluation

### Metrik Evaluasi:
- Accuracy
- Precision
- Recall
- F1-Score

### Hasil Evaluasi:

**Logistic Regression**:
- Accuracy: **83.7%**
- Macro Precision: 79%
- Macro Recall: 70%
- Macro F1-Score: 72%

**Decision Tree Classifier**:
- Accuracy: **88.5%**
- Macro Precision: 83%
- Macro Recall: 84%
- Macro F1-Score: 84%

### Pemilihan Model Terbaik:
Model **Decision Tree Classifier** dipilih karena menghasilkan performa klasifikasi yang lebih tinggi dibandingkan Logistic Regression, berdasarkan nilai akurasi, precision, recall, dan F1-Score.

## Conclusion

Dengan menggunakan dataset Credit Risk dari Kaggle, dua model Machine Learning telah dikembangkan untuk memprediksi kemungkinan gagal bayar nasabah.  
Dari hasil evaluasi, **Decision Tree Classifier** menjadi pilihan model terbaik dengan akurasi **88.5%**, sehingga model ini dapat membantu lembaga keuangan dalam pengambilan keputusan pemberian kredit yang lebih bijaksana.
