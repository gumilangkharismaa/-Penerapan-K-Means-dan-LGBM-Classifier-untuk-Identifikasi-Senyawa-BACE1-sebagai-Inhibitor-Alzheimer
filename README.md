# Penerapan K-Means dan LGBMClassifier untuk Identifikasi Senyawa BACE1 sebagai Inhibitor Alzheimer

Selamat datang di repositori kami! dalam project kali ini, kami menerapkan teknik **K-Means** untuk klasterisasi dan **LGBMClassifier** untuk klasifikasi senyawa aktif dan tidak aktif dalam proses screening virtual terhadap target enzim **BACE1**. Project ini bertujuan untuk mendukung penelitian terkait Alzheimer dengan mengidentifikasi senyawa yang potensial sebagai inhibitor **BACE1** secara lebih efisien.

## Pendahuluan
Alzheimer adalah salah satu penyakit neurodegeneratif yang paling umum terjadi pada populasi lanjut usia. Enzim **Beta-secretase 1 (BACE1)** berperan penting dalam proses pembentukan beta-amyloid yang merupakan salah satu penyebab utama penyakit Alzheimer. Identifikasi inhibitor BACE1 merupakan langkah penting dalam upaya pengembangan obat yang efektif.

### Tujuan Proyek
Proyek ini bertujuan untuk:
1. Melakukan preprocessing data senyawa kimia yang relevan dengan BACE1.
2. Menggunakan **K-Means** untuk mengelompokkan senyawa berdasarkan fingerprint kimia.
3. Menerapkan **LGBMClassifier** untuk memprediksi aktivitas bio senyawa terhadap BACE1.
4. Memberikan evaluasi hasil.

## Tahapan Project
### 1. Persiapan Data
- Mengunduh dataset senyawa menggunakan kata kunci **BACE1** dari basis data bioinformatika.

### 2. Preprocessing Data
- Menyaring data untuk spesies **Homo sapiens** dan kolom utama (**molecule_chembl_id**, **canonical_smiles**, **standard_value**).
- Melabeli data berdasarkan nilai IC50 menjadi kelas **active** (IC50 ≤ 1.000 nM) dan **inactive** (IC50 ≥ 10.000 nM), menghapus kelas **intermediate**.
- Menghitung deskriptor Lipinski: MW, LogP, NumHDonors, dan NumHAcceptors menggunakan **RDKit**.
- Mengonversi nilai IC50 menjadi **pIC50**.
- Menyimpan dataset yang telah diproses untuk analisis selanjutnya.

### 3. Klasterisasi dengan K-Means
- Menggunakan **K-Means** untuk mengelompokkan senyawa berdasarkan fingerprint.
- Mengevaluasi hasil klasterisasi melalui visualisasi.

### 4. Klasifikasi dengan LGBMClassifier
- Melatih model **LGBMClassifier** untuk memprediksi kelas senyawa (aktif atau tidak aktif).
- Mengevaluasi performa model menggunakan metrik evaluasi seperti akurasi, precision, recall, dan F1-score.

## Hasil dan Diskusi
- Model klasterisasi berhasil mengelompokkan senyawa dengan tingkat kesamaan tertentu.
- Senyawa potensial yang teridentifikasi sebagai inhibitor BACE1 diprioritaskan untuk studi lebih lanjut.

## Teknologi yang Digunakan
- **Python**: Bahasa pemrograman utama.
- **RDKit**: Untuk pengolahan struktur kimia dan fingerprint generation.
- **LGBMClassifier**: Library machine learning untuk klasifikasi.
- **Scikit-learn**: Untuk klasterisasi K-Means.
- **Matplotlib** dan **Seaborn**: Untuk visualisasi data.

## Cara Menjalankan
1. Clone repositori ini:
   ```bash
   git clone https://github.com/username/repo-name.git
   ```
2. Instal dependensi yang diperlukan:
   ```bash
   pip install -r requirements.txt
   ```
3. Jalankan notebook utama untuk preprocessing dan analisis:
   ```bash
   jupyter notebook main.ipynb
   ```

## Kontribusi
Kami terbuka untuk saran dan masukan! Jika Anda ingin berkontribusi, silakan buat pull request atau hubungi kami melalui email yang tertera di profil ini.

---
Terima kasih telah mengunjungi repositori kami. Kami berharap project ini dapat memberikan kontribusi berarti dalam penelitian Alzheimer.

## Apreciation to all of them who contribute for this project! 
1. Kharisma Gumilang
2. Dede Masita
3. Eunike Bunga
4. Ramadhita Atifa Hendri
5. Divania Rahmadani
6. Ericson Chandra Sihombing
