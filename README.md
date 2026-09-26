# Proyek 1 EDA — Smart City: Bike Sharing

## Judul Analisis
**Analisis Data Penyewaaan Sepeda sebagai Bagian dari Smart City)**

## Topik
Smart City — transportasi publik / bike sharing.

## Dataset
Dataset yang digunakan adalah **Bike Sharing Dataset** dari UCI Machine Learning Repository.

- Sumber: UCI Machine Learning Repository
- URL: https://archive.ics.uci.edu/dataset/275/bike+sharing+dataset
- DOI: https://doi.org/10.24432/C5W894
- Lisensi: Creative Commons Attribution 4.0 International (CC BY 4.0)
- Data: jumlah penyewaan sepeda harian dan informasi cuaca/musim pada sistem Capital Bikeshare tahun 2011–2012.
- File yang digunakan: `bikesharing_dataset.csv`
- Unit observasi: **1 baris = 1 hari**
- Ukuran `day.csv`: **731 baris, 16 kolom**
- Tidak ada nilai missing pada dataset sumber.

## Kenapa termasuk Smart City?
Bike sharing merupakan bagian dari mobilitas perkotaan. Data penyewaan dapat digunakan untuk memahami pola penggunaan transportasi di kota dan membantu melihat bagaimana permintaan berubah menurut waktu, musim, serta kondisi cuaca.

## Pertanyaan Analisis
1. Bagaimana pusat dan penyebaran jumlah penyewaan sepeda (`cnt`) dalam satu hari?
2. Bagaimana jumlah penyewaan berbeda menurut musim (`season`)?
3. Bagaimana pola hubungan yang terlihat antara suhu normalisasi (`temp`) dan jumlah penyewaan (`cnt`)?

## Struktur Folder

proyek1-eda-kelompok-08/
├── README.md
├── eda_kelompok_08.ipynb
└── data/
    ├── bikesharing_dataset.csv

## Cara Mendapatkan Dataset

1. search Bike Sharing Dataset di UCI Machine Learning,
2. mengunduh Bike Sharing Dataset dari UCI Machine Learning,
3. mengambil `day.csv`,
4. menyimpannya ke `data/bikesharing_dataset.csv`.

## Instalasi
Gunakan environment mata kuliah:

```bash
conda create -n statprob python=3.11 -y
conda activate statprob
conda install -c conda-forge jupyter pandas matplotlib seaborn -y
```

Jalankan:

```bash
jupyter notebook
```

Jika ingin membukanya lagi, maka cara aktifkan kembali Jupyter Notebook yaitu:

```bash
conda activate statprob
jupyter notebook
```

Kemudian buat Folder Baru:
`proyek1-eda-kelompok-08`

## Catatan penting tentang variabel

- `temp`: suhu normalisasi, dibentuk dari rentang -8°C sampai +39°C.
- `atemp`: suhu yang dirasakan dalam bentuk normalisasi.
- `hum`: kelembapan normalisasi, dibagi 100.
- `windspeed`: kecepatan angin normalisasi, dibagi 67.
- `cnt`: total jumlah penyewaan sepeda = `casual + registered`.

## Hasil angka yang dapat dijadikan pengecekan
Untuk dataset `bikesharing_dataset.csv`, ringkasan statistik yang umum muncul adalah:

| Variabel | Mean | Median | Min | Q1 | Q3 | Max |
|---|---:|---:|---:|---:|---:|---:|
| temp | 0.495385 | 0.498333 | 0.059130 | 0.337083 | 0.655417 | 0.861667 |
| hum | 0.627894 | 0.626667 | 0.000000 | 0.520000 | 0.730209 | 0.972500 |
| cnt | 4504.348837 | 4548 | 22 | 3152 | 5956 | 8714 |

Untuk `cnt`, jangkauan = 8714 − 22 = **8692**, sedangkan IQR = 5956 − 3152 = **2804**.

Distribusi musim berdasarkan kode UCI:
- 1 = Winter: 181 hari
- 2 = Spring: 184 hari
- 3 = Summer: 188 hari
- 4 = Fall: 178 hari


