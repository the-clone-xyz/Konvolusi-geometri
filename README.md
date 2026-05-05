# Kalkulator Konvolusi Geometri 2D

> **Interactive Visualizer for 2D Matrix Convolution with Sliding Window Algorithm**

![GitHub Stars](https://img.shields.io/badge/Built%20with-HTML5%20%7C%20JavaScript%20%7C%20Tailwind-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## 📋 Deskripsi Sistem

**Kalkulator Konvolusi Geometri 2D** adalah aplikasi web interaktif yang memvisualisasikan proses konvolusi dua dimensi secara langkah demi langkah. Aplikasi ini dirancang untuk membantu pengguna memahami bagaimana algoritma sliding window bekerja dalam operasi konvolusi matriks, yang sering digunakan dalam:

- **Pengolahan Citra Dijital** (Image Processing)
- **Jaringan Saraf Tiruan** (Neural Networks / CNN)
- **Pemfilteran Sinyal** (Signal Processing)

### ✨ Fitur Utama

- ✅ **Input Matriks Dinamis**: Tambah/kurangi baris dan kolom sesuai kebutuhan
- ✅ **Kernel Customizable**: Tentukan filter/kernel dengan ukuran bebas
- ✅ **Visualisasi Langkah Demi Langkah**: Lihat setiap iterasi sliding window
- ✅ **Perhitungan Real-time**: Hasil kalkulasi ditampilkan secara instant
- ✅ **UI Responsif**: Desain modern dengan Tailwind CSS
- ✅ **Tampilan Animasi**: Transisi halus dan highlight yang intuitif
- ✅ **Padding & Stride Support**: Dukungan untuk operasi konvolusi advanced
- ✅ **Export Hasil**: Lihat output dan rumus dalam format yang rapi

### 🎯 Algoritma

Aplikasi menggunakan algoritma **sliding window** klasik untuk konvolusi 2D:

```
Untuk setiap posisi (i, j) pada output:
  1. Ambil window dari input matriks sesuai ukuran kernel
  2. Kalikan elemen-elemen yang sesuai antara window dan kernel
  3. Jumlahkan semua hasil perkalian
  4. Simpan hasil di output[i][j]
```

## 🚀 Cara Instalasi

### Prasyarat

- **Node.js** (versi 14+)
- **npm** atau **yarn**
- Browser modern (Chrome, Firefox, Safari, Edge)

### Langkah Instalasi

1. **Clone Repository**

```bash
git clone https://github.com/the-clone-xyz/Konvolusi-geometri.git
cd Konvolusi-kalkulator
```

2. **Install Dependencies**

```bash
npm install
```

Atau jika menggunakan yarn:

```bash
yarn install
```

3. **Jalankan Secara Lokal**

Buka file `index.html` langsung di browser:

```bash
# Menggunakan Live Server (VS Code Extension)
# Klik kanan pada index.html → "Open with Live Server"

# Atau menggunakan Python (jika terinstall)
python -m http.server 8000

# Atau menggunakan Node.js http-server
npx http-server
```

Kemudian akses di: **`http://localhost:8000`**

4. **Build untuk Production (Opsional)**

Jika ingin menggunakan Tailwind CSS secara offline:

```bash
npm run build
```

## 📖 Cara Penggunaan

### 1. **Input Matriks Input (I)**

- Masukkan nilai-nilai numerik untuk matriks input
- Gunakan tombol **"+ Tambah Baris"** / **"+ Tambah Kolom"** untuk menambah dimensi
- Gunakan tombol **"- Kurangi Baris"** / **"- Kurangi Kolom"** untuk mengurangi dimensi
- Nilai default: Matriks 3×3

### 2. **Input Kernel (K)**

- Masukkan nilai-nilai untuk filter/kernel
- Ukuran kernel biasanya lebih kecil dari matriks input
- Contoh kernel populer:
  - **Edge Detection**: `[[-1, 0, 1], [-2, 0, 2], [-1, 0, 1]]`
  - **Blur**: `[[1/9, 1/9, 1/9], [1/9, 1/9, 1/9], [1/9, 1/9, 1/9]]`
  - **Sharpen**: `[[0, -1, 0], [-1, 5, -1], [0, -1, 0]]`

### 3. **Atur Padding & Stride**

- **Padding**: Jumlah lapisan nol yang ditambahkan di sekitar input (default: 0)
- **Stride**: Jumlah piksel untuk menggeser kernel di setiap langkah (default: 1)

### 4. **Hitung Konvolusi**

- Klik tombol **"Hitung Konvolusi 2D"**
- Aplikasi akan menampilkan:
  - Output matriks hasil
  - Dimensi output
  - Langkah-langkah perhitungan detail
  - Visualisasi sliding window

### 5. **Analisis Hasil**

- **Output Matrix**: Hasil akhir dari operasi konvolusi
- **Computation Steps**: Detail perhitungan untuk setiap posisi output
- **Window Visualization**: Tampilan visual dari kernel yang sedang diproses

## � Screenshot & Demo

### Interface Utama
![Kalkulator Konvolusi 2D - Main Interface](screenshots/01-main-interface.png)

*Layar input matriks utama dan kernel dengan kontrol untuk mengatur dimensi*

### Visualisasi Langkah-Langkah
![Visualisasi Langkah Konvolusi](screenshots/02-visualization-steps.png)

*Demonstrasi visual sliding window dengan area tumpang tindih (overlap area) dan perhitungan detail per posisi*

### Hasil Perhitungan & Analisis
![Hasil Konvolusi 2D](screenshots/03-computation-results.png)

*Output matriks hasil konvolusi dengan breakdown perhitungan mathematical untuk setiap posisi (i,j)*

## �📊 Contoh Penggunaan

### Contoh 1: Konvolusi Dasar 3×3

**Input:**
```
1 2 3
4 5 6
7 8 9
```

**Kernel:**
```
1 0
0 1
```

**Hasil Output:**
- Ukuran: 2×2 (karena stride=1, padding=0)
- Nilai-nilai dihitung dari setiap sliding window

### Contoh 2: Blur Effect

Gunakan kernel Gaussian blur:
```
1/9 1/9 1/9
1/9 1/9 1/9
1/9 1/9 1/9
```

Ini akan menghasilkan efek blur pada matriks input.

## 🛠️ Stack Teknologi

| Teknologi | Versi | Penggunaan |
|-----------|-------|-----------|
| HTML5 | - | Struktur halaman |
| Vanilla JavaScript | ES6+ | Logika aplikasi & kalkulasi |
| Tailwind CSS | 3.0+ | Styling & responsiveness |
| npm | 6.0+ | Package management |

## 📁 Struktur Proyek

```
Konvolusi-kalkulator/
├── index.html           # File utama aplikasi
├── package.json         # Konfigurasi npm & dependencies
├── package-lock.json    # Lock file untuk dependencies
├── README.md            # Dokumentasi ini
├── .gitignore           # File/folder yang diabaikan Git
└── node_modules/        # Dependencies (jangan di-commit)
```

## 🔧 Konfigurasi & Customization

### Mengubah Ukuran Matriks Default

Edit di dalam `index.html` bagian `<script>`:

```javascript
// Default: Matriks 3x3
const DEFAULT_ROWS = 3;
const DEFAULT_COLS = 3;
```

### Mengubah Batch Size atau Max Dimensions

```javascript
// Maksimum baris/kolom yang diizinkan
const MAX_MATRIX_SIZE = 10;
```

## ⚠️ Batasan & Catatan

- **Ukuran Matriks**: Maksimum 10×10 untuk menjaga performa browser
- **Presisi Desimal**: Nilai ditampilkan dengan 4 desimal
- **Browser Kompatibilitas**: IE tidak didukung (gunakan browser modern)
- **Performance**: Matriks sangat besar (>15×15) mungkin lambat

## 🤝 Kontribusi

Kontribusi sangat diterima! Silakan:

1. Fork repository ini
2. Buat branch feature (`git checkout -b feature/AmazingFeature`)
3. Commit perubahan Anda (`git commit -m 'Add some AmazingFeature'`)
4. Push ke branch (`git push origin feature/AmazingFeature`)
5. Buat Pull Request

## 📝 Lisensi

Proyek ini dilisensikan di bawah **MIT License**. Lihat file [LICENSE](LICENSE) untuk detail.

## 👨‍💻 Author

**Yogi Syahputra** (@yogisyahputra)

- GitHub: [the-clone-xyz](https://github.com/the-clone-xyz)
- Email: yogisyahputra@example.com

> *"Built with logic, designed with passion."*

## 📚 Referensi & Resources

- [Convolution (Wikipedia)](https://en.wikipedia.org/wiki/Convolution)
- [Convolutional Neural Networks](https://en.wikipedia.org/wiki/Convolutional_neural_network)
- [Image Convolution Explained](https://towardsdatascience.com/convolutions-explained-1a0a886b3bce)
- [Tailwind CSS Docs](https://tailwindcss.com/docs)

## 🐛 Issue & Bug Report

Jika menemukan bug atau issue, silakan buka **Issue** di [GitHub Issues](https://github.com/the-clone-xyz/Konvolusi-geometri/issues).

---

**Last Updated**: May 5, 2026  
**Version**: 1.0.0
