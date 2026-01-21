# Transformers
# Analisis Sentimen Bahasa Indonesia dengan Transformers

## Deskripsi Proyek

Repositori ini berisi implementasi **analisis sentimen teks Bahasa Indonesia** menggunakan pendekatan *Deep Learning* berbasis **Hugging Face Transformers**. Proyek ini bertujuan untuk melakukan proses pelatihan model klasifikasi sentimen (positif, netral, negatif), melakukan pengujian, serta mengekspor hasil prediksi ke dalam file CSV.

Notebook ini dibuat sebagai tugas/eksperimen pembelajaran terkait *Natural Language Processing (NLP)* dan pemanfaatan model *pre-trained transformer*.

---

## Struktur File

```
├── tugas_11_transformasi.ipynb   # Notebook utama analisis sentimen
├── hasil_prediksi_sentimen.csv  # Output hasil prediksi sentimen
└── README.md                    # Dokumentasi proyek
```

---

## Penjelasan File

### 1. `tugas_11_transformasi.ipynb`

Notebook utama yang berisi seluruh tahapan analisis sentimen, meliputi:

#### a. Persiapan Dataset

* Data teks sentimen dibagi menjadi:

  * **Data Positif**
  * **Data Negatif**
  * **Data Netral**
  * **Data Tanpa Label (unlabeled)**
* Dataset dibuat secara manual untuk keperluan eksperimen.

#### b. Instalasi dan Import Library

Library utama yang digunakan:

* `transformers`
* `datasets`
* `torch`
* `scikit-learn`
* `pandas`

#### c. Preprocessing Data

* Mengubah data teks menjadi format *DataFrame*
* Mapping label sentimen ke dalam bentuk numerik
* Tokenisasi teks menggunakan tokenizer dari model Transformer

#### d. Pembuatan Model

* Menggunakan **AutoModelForSequenceClassification** dari Hugging Face
* Model disesuaikan untuk klasifikasi 3 kelas sentimen

#### e. Training Model

* Konfigurasi pelatihan menggunakan `TrainingArguments`
* Proses training dilakukan dengan `Trainer`

#### f. Evaluasi dan Prediksi

* Model diuji menggunakan data uji
* Hasil prediksi dikonversi kembali ke label sentimen:

  * Negatif
  * Netral
  * Positif

#### g. Visualisasi dan Output

* Hasil prediksi ditampilkan dalam bentuk tabel
* Data hasil prediksi diekspor ke file CSV

---

### 2. `hasil_prediksi_sentimen.csv`

File output yang berisi:

* Teks input
* Label sentimen hasil prediksi model

File ini dapat digunakan untuk:

* Analisis lanjutan
* Visualisasi
* Pelaporan hasil eksperimen

---

## Alur Proses Sistem

1. Input data teks sentimen
2. Preprocessing & tokenisasi teks
3. Training model Transformer
4. Evaluasi model
5. Prediksi sentimen
6. Ekspor hasil ke CSV

---

## Teknologi yang Digunakan

* Python
* Google Colab
* Hugging Face Transformers
* PyTorch
* Pandas

---

## Cara Menjalankan Notebook

1. Buka `tugas_11_transformasi.ipynb` di Google Colab
2. Jalankan seluruh cell secara berurutan
3. Pastikan koneksi internet aktif untuk mengunduh model Transformer
4. Setelah selesai, file `hasil_prediksi_sentimen.csv` akan otomatis terbuat



> README ini dibuat untuk mendokumentasikan proyek analisis sentimen berbasis Transformer dan siap digunakan pada repositori GitHub.
