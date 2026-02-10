# 🏥 Analisis Biaya Kesehatan (Healthcare Cost Analysis) – Tableau

## 📌 Gambaran Proyek
Proyek ini bertujuan untuk menganalisis **biaya kesehatan** dan mengidentifikasi **faktor utama penyebab tingginya biaya**, menggunakan pendekatan **Business Intelligence dan Data Visualization** dengan **Tableau**.

Analisis difokuskan pada:
- Pola distribusi biaya kesehatan
- Identifikasi pasien dengan **biaya tinggi (High Cost Patient)**
- Analisis faktor risiko utama seperti **kebiasaan merokok, usia, dan BMI**
- Penyusunan **rekomendasi berbasis data** untuk pengendalian biaya

---

## 📂 Dataset
Dataset berisi data pasien dengan variabel berikut:
- `age` (usia)
- `sex` (jenis kelamin)
- `bmi` (Body Mass Index)
- `children` (jumlah tanggungan anak)
- `smoker` (status merokok)
- `region` (wilayah)
- `charges` (biaya kesehatan)

**Jumlah data:** 1.337 pasien

---

## 🧹 Pembersihan & Persiapan Data (Data Cleaning & Preparation)

Tahapan pembersihan dan persiapan data dilakukan langsung di **Tableau** untuk memastikan data siap dianalisis.

### Pemeriksaan Kualitas Data
- Tidak ditemukan nilai kosong (null) yang signifikan
- Terdapat 1 data duplikat, 1 data duplikat tersebut dihapus untuk menghindari bias pada perhitungan biaya
- Nilai numerik berada dalam rentang yang wajar

### Penyesuaian Tipe Data
- **Measure (Numerik):**
  - Age
  - BMI
  - Charges
- **Dimension (Kategorikal):**
  - Sex
  - Smoker
  - Region
  - Children

---

## 🔄 Transformasi Data

Transformasi data dilakukan untuk menyederhanakan analisis dan menyesuaikan dengan konteks bisnis kesehatan.

### 🔹 Pengelompokan Usia (Age Group)
Usia dikelompokkan menjadi:
- `<30`
- `30–45`
- `46–64`

**Alasan:**  
Biaya kesehatan tidak meningkat secara linear per tahun, melainkan cenderung meningkat pada kelompok usia tertentu.

---

### 🔹 Kategori BMI (BMI Category)
BMI dikategorikan menjadi:
- Underweight
- Ideal
- Overweight
- Obese

**Alasan:**  
Kategori BMI lebih relevan untuk analisis risiko kesehatan dibandingkan nilai BMI mentah.

---

### 🔹 Kategori Biaya Kesehatan (Cost Category – Percentile Based)
Biaya kesehatan dikelompokkan berdasarkan distribusi data:
- **Low Cost** → 10% terbawah
- **Normal Cost** → 80% tengah
- **High Cost** → 10% teratas

**Alasan:**  
Distribusi biaya sangat tidak merata (right-skewed), sehingga pendekatan berbasis persentil lebih adil dibandingkan batas nominal tetap.

---

## 🧮 Calculated Field
Beberapa calculated field dibuat di Tableau untuk mendukung analisis:
- Age Group
- BMI Category
- Cost Category
- High Cost Patient Ratio (%)

---

## 📊 Eksplorasi & Analisis Data (EDA)

### 📊 Dashboard 1 — Overview Biaya Kesehatan
**Tujuan:** Memberikan gambaran umum kondisi biaya kesehatan.

**Visualisasi:**
- KPI Cards (Total Biaya, Rata-rata Biaya, Rasio High Cost)
- Histogram Distribusi Biaya
- Pie Chart Kategori Biaya
- Perbandingan Biaya Perokok vs Non-Perokok

**Insight Utama:**
- Biaya kesehatan tidak terdistribusi secara merata
- Sekitar **10% pasien masuk kategori High Cost**
- Pasien perokok memiliki biaya kesehatan jauh lebih tinggi

---

### 📈 Dashboard 2 — Analisis Risiko & Dampak
**Tujuan:** Mengidentifikasi kelompok pasien dengan risiko biaya tinggi.

**Visualisasi:**
- Scatter Plot (Usia vs Biaya)
- Rata-rata Biaya per Kelompok Usia
- Rata-rata Biaya per Kategori BMI
- Heatmap Risiko (Kelompok Usia × Kategori BMI)

**Insight Utama:**
- Biaya meningkat seiring bertambahnya usia
- Pasien dengan BMI obesitas memiliki biaya tertinggi
- Kombinasi usia lanjut dan BMI tinggi membentuk area risiko biaya paling tinggi

---

## 💡 Insight Utama
- Biaya kesehatan sangat **tidak merata**, dengan konsentrasi pada sebagian kecil pasien
- **Merokok** merupakan faktor paling dominan dalam peningkatan biaya
- Risiko biaya semakin tinggi ketika dikombinasikan dengan **usia** dan **BMI tinggi**
- Faktor **jenis kelamin, wilayah, dan jumlah anak** memiliki pengaruh relatif kecil

---

## ✅ Rekomendasi Berbasis Data
Berdasarkan hasil analisis, rekomendasi yang diberikan:
- Fokus pada program pencegahan dan edukasi bagi pasien **perokok**
- Program pengelolaan berat badan untuk pasien dengan **BMI tinggi**
- Pendekatan preventif dan monitoring kesehatan pada **kelompok usia berisiko**
- Penerapan strategi berbasis risiko untuk pengendalian biaya kesehatan

---


## 📁 Output Proyek
- File Tableau Dashboard (`.twbx`)
- Slide Presentasi (`canva`)
- Dokumentasi Proyek (`README.md`)

---

## 📌 Kesimpulan
Analisis ini menunjukkan bahwa visualisasi data dan dashboard interaktif dapat membantu mengidentifikasi kelompok pasien berbiaya tinggi secara efektif, sehingga mendukung pengambilan keputusan yang lebih tepat dalam pengelolaan biaya kesehatan.
