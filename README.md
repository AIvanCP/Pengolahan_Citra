# Pengolahan Citra - Job 1

Proyek praktikum pengolahan citra digital dengan Python menggunakan scikit-image dan NumPy.

## Struktur Folder

```
job1/
├── p1.ipynb          # Ukuran gambar digital
├── p2.ipynb          # Piksel dan area fokus
├── p3.ipynb          # Array NumPy
├── p4.ipynb          # Sistem koordinat
├── p5.ipynb          # Model warna RGB
├── p6.ipynb          # Kanal warna R, G, B
├── p7.ipynb          # Format file (BMP, JPEG, TIFF)
├── p8.ipynb          # Kompresi lossy vs lossless
└── explanations/     # Penjelasan untuk laporan (local only, di-ignore)
    ├── p1.md
    ├── p2.md
    ├── p3.md
    ├── p4.md
    ├── p5.md
    ├── p6.md
    ├── p7.md
    └── p8.md
```

## Instalasi & Setup

### 1. Clone Repository
```bash
git clone <repository-url>
cd ngoding/job1
```

### 2. Setup Virtual Environment
```bash
# Buat virtual environment
python -m venv venv

# Aktivasi venv (Windows)
venv\Scripts\activate

# Aktivasi venv (Linux/Mac)
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install numpy matplotlib scikit-image
```

### 4. Jalankan Jupyter Notebook
```bash
jupyter notebook
```

Buka file `p1.ipynb` hingga `p8.ipynb` secara berurutan.

## Daftar Praktikum

| File | Topik | Deskripsi |
|------|-------|-----------|
| `p1.ipynb` | Ukuran Gambar | Menghitung dan menampilkan ukuran gambar dalam bit, byte, KB, MB |
| `p2.ipynb` | Piksel & Zoom | Visualisasi Area fokus dan nilai piksel gambar |
| `p3.ipynb` | Array NumPy | Memahami struktur gambar sebagai array multidimensi |
| `p4.ipynb` | Koordinat | Sistem koordinat (0,0) kiri atas dalam gambar digital |
| `p5.ipynb` | Model RGB | Model warna aditif dan 16 juta kombinasi warna |
| `p6.ipynb` | Kanal Warna | Ekstraksi dan visualisasi kanal Merah, Hijau, Biru |
| `p7.ipynb` | Format File | Perbandingan BMP (uncompressed), JPEG (lossy), TIFF (flexible) |
| `p8.ipynb` | Kompresi | Perbedaan lossy (JPEG) vs lossless (PNG) compression |

## File Penjelasan (Local Only)

Folder `explanations/` berisi dokumentasi markdown untuk laporan:
- **Format**: Kode → Output → Penjelasan Sederhana
- **Bahasa**: Mudah dipahami orang awam (non-teknis)
- **Penggunaan**: Untuk laporan atau dokumentasi lokal

**File ini di-ignore dari Git** (lihat `.gitignore`). Jika perlu push file spesifik dari folder ini, bisa gunakan:
```bash
git add -f explanations/p1.md  # Force add specific file
```

## Output Files

Program akan menghasilkan file gambar:
- `astronaut.bmp` - Format BMP (uncompressed)
- `astronaut.jpg` - Format JPEG dengan quality=95
- `astronaut.tiff` - Format TIFF
- `astronaut_lossy_50.jpg` - JPEG lossy quality=50
- `astronaut_lossy_90.jpg` - JPEG lossy quality=90
- `astronaut_lossless.png` - PNG lossless

Files ini akan di-generated saat menjalankan `p7.ipynb` dan `p8.ipynb`.

## .gitignore Details

### Apa yang Di-Ignore:

**Python & Jupyter:**
- `__pycache__/` - Cache Python
- `.ipynb_checkpoints/` - Jupyter checkpoint

**Virtual Environment:**
- `venv/`, `env/`, `ENV/` - Virtual environment

**Output Files:**
- `*.csv`, `*.xlsx` - Data files
- `*.png`, `*.jpg`, `*.jpeg`, `*.gif`, `*.bmp`, `*.tiff` - Generated images
- `*.egg-info/` - Package files

**Local Documentation:**
- `explanations/` - Folder penjelasan untuk laporan lokal
- `report/` - Folder laporan
- `*.report.docx` - File laporan Word

### Force Include Files

Jika perlu push file yang normally di-ignore, gunakan flag `-f`:
```bash
# Force add file yang di-ignore
git add -f explanations/p1.md
git add -f astronaut.jpg

# Atau edit .gitignore dengan negation pattern:
# !explanations/p1.md
```

## Tips Penggunaan

### Jalankan Notebook Secara Berurutan
1. Mulai dari `p1.ipynb` hingga `p8.ipynb`
2. Setiap notebook berdiri sendiri (self-contained)
3. Bisa dijalankan ulang tanpa dependencies dari notebook sebelumnya

### Untuk Laporan
Gunakan file penjelasan di `explanations/`:
```
1. Copy-paste kode dari p1.ipynb
2. Refer output dari explanations/p1.md
3. Copy-paste penjelasan dari explanations/p1.md
4. Format: [Kode] → [Output] → [Penjelasan]
```

### Edit .gitignore Jika Diperlukan

Jika ingin mengubah apa yang di-ignore/include:

```bash
# Edit .gitignore
nano .gitignore        # Linux/Mac
notepad .gitignore     # Windows

# Commit perubahan
git add .gitignore
git commit -m "Update gitignore settings"
```

## Troubleshooting

**Error: `ModuleNotFoundError: No module named 'skimage'`**
```bash
pip install scikit-image
```

**Error: Port 8888 already in use**
```bash
jupyter notebook --port 8889
```

**File gambar tidak bisa ditemukan di p7/p8**
- Pastikan working directory adalah folder `job1/`
- Jalankan notebook dari `job1/` folder

## Dependencies

- `numpy` - Komputasi numerik
- `matplotlib` - Visualisasi dan plotting
- `scikit-image` - Pengolahan citra

## Lisensi

Proyek ini untuk keperluan edukasi.

## Kontak

Untuk pertanyaan, silakan hubungi instruktur.

---

**Last Updated**: April 2026  
**Python Version**: 3.7+  
**Status**: ✅ Semua notebook berfungsi dan ready untuk dijalankan
