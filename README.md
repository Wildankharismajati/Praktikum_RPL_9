# 🎓 Sistem Prediksi Kelulusan Mahasiswa

Repository ini merupakan dokumentasi dan source code **Praktikum 9 Rekayasa Perangkat Lunak (SSD1030)** dengan studi kasus Sistem Prediksi Kelulusan Mahasiswa.

Praktikum ini menerapkan konsep **Layered Architecture, Clean Code, dan SOLID (Single Responsibility Principle)** menggunakan Python, Streamlit, dan SQLite.

## 👨‍🎓 Identitas Mahasiswa

| Keterangan | Detail |
|---|---|
| Nama | Wildan Kharisma Jati |
| NIM | 60124022 |
| Program Studi | Sains Data |
| Mata Kuliah | Rekayasa Perangkat Lunak (SSD1030) |
| Praktikum | Pertemuan 9 |

## 📌 Deskripsi Proyek

Sistem Prediksi Kelulusan Mahasiswa merupakan aplikasi sederhana yang digunakan untuk menentukan status kelulusan mahasiswa berdasarkan nilai IPK dan jumlah SKS yang telah ditempuh.

Aplikasi menyediakan form input data mahasiswa, menampilkan hasil prediksi kelulusan, serta menyimpan data ke database sehingga dapat ditampilkan kembali dalam tabel riwayat prediksi.

## 🛠️ Teknologi yang Digunakan

- Python
- Streamlit
- SQLAlchemy
- SQLite
- Python-dotenv
- Pandas

## 🏗️ Arsitektur Sistem

Proyek ini menggunakan empat layer dengan prinsip Single Responsibility Principle (SRP).

| Layer | File | Tanggung Jawab |
|---|---|---|
| View | `app.py` | Mengatur tampilan aplikasi menggunakan Streamlit |
| Service | `services/service.py` | Mengatur logika prediksi kelulusan |
| Repository | `repositories/repository.py` | Mengatur penyimpanan dan pengambilan data |
| Model | `models/model.py` | Mengatur struktur tabel database |

## 📂 Struktur Folder

```text
Praktikum_RPL_9/
│
├── app.py
├── .env
├── requirements.txt
│
├── models/
│   └── model.py
│
├── repositories/
│   └── repository.py
│
└── services/
    └── service.py
```

## ⚙️ Aturan Prediksi Kelulusan

Sistem menggunakan dua ketentuan berikut:

- IPK minimal 3.00.
- Total SKS minimal 140.

Mahasiswa dinyatakan **Lulus Tepat Waktu** apabila memenuhi kedua ketentuan tersebut. Jika salah satu atau keduanya tidak terpenuhi, statusnya adalah **Tidak Lulus**.

## 🚀 Cara Menjalankan Aplikasi

### 1. Clone Repository

```bash
git clone URL_REPOSITORY_KAMU
```

Ganti `URL_REPOSITORY_KAMU` dengan alamat repository GitHub.

### 2. Masuk ke Folder Proyek

```bash
cd Praktikum_RPL_9
```

### 3. Instal Library

```bash
python -m pip install streamlit sqlalchemy python-dotenv pandas
```

### 4. Konfigurasi Database

Buat file `.env` dengan isi:

```env
DATABASE_URL=sqlite:///data_prediksi.db
```

### 5. Jalankan Aplikasi

```bash
python -m streamlit run app.py
```

Aplikasi akan terbuka melalui browser menggunakan alamat lokal yang diberikan oleh Streamlit.

## 🧪 Pengujian Sistem

| Nama | IPK | SKS | Hasil Prediksi |
|---|---:|---:|---|
| Mahasiswa A | 3.50 | 144 | Lulus Tepat Waktu |
| Mahasiswa B | 3.00 | 140 | Lulus Tepat Waktu |
| Mahasiswa C | 2.90 | 150 | Tidak Lulus |
| Mahasiswa D | 3.60 | 120 | Tidak Lulus |

## 🎯 Tujuan Praktikum

1. Membuat mockup UI dan merancang arsitektur layered.
2. Menerapkan Clean Code dan SOLID.
3. Memisahkan kode berdasarkan tanggung jawab setiap layer.
4. Mengintegrasikan Python dengan database SQLite menggunakan SQLAlchemy.
5. Membuat antarmuka interaktif menggunakan Streamlit.

## 📄 Dokumentasi

Laporan lengkap praktikum tersedia pada file:

`Laporan_Praktikum_9_RPL_Wildan Kharisma Jati.docx`

---

**Rekayasa Perangkat Lunak (SSD1030)**  
Praktikum 9 – Sistem Prediksi Kelulusan Mahasiswa

© 2026 Wildan Kharisma Jati
