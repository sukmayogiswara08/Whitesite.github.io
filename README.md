# Virtual Tour — GitHub Pages Ready

Folder ini sudah disiapkan sebagai situs statis untuk GitHub Pages. Tidak ada proses build, instalasi, atau server khusus yang diperlukan.

## Isi penting

- `index.html` — halaman utama yang dibaca GitHub Pages.
- `.nojekyll` — mencegah GitHub Pages memproses aset melalui Jekyll.
- `script.js`, `lib/`, dan `media/` — mesin tur virtual dan seluruh aset panorama.

Semua jalur aset bersifat relatif sehingga situs tetap dapat berjalan pada alamat proyek seperti:

`https://USERNAME.github.io/NAMA-REPOSITORY/`

## Cara unggah yang disarankan

Karena proyek memuat ribuan berkas gambar, gunakan GitHub Desktop atau Git melalui terminal. Jangan hanya mengunggah berkas ZIP ke repository karena GitHub Pages tidak mengekstraknya otomatis.

### Menggunakan GitHub Desktop

1. Ekstrak ZIP ini ke satu folder.
2. Buka GitHub Desktop, lalu pilih **File → Add local repository** dan arahkan ke folder hasil ekstraksi.
3. Jika diminta, pilih **Create a repository here**.
4. Lakukan commit seluruh berkas, lalu pilih **Publish repository**.
5. Buka repository di GitHub.com.
6. Masuk ke **Settings → Pages**.
7. Pada **Build and deployment**, pilih **Deploy from a branch**.
8. Pilih branch **main**, folder **/(root)**, lalu klik **Save**.
9. Tunggu proses deployment selesai. Tautan situs akan muncul pada halaman **Settings → Pages**.

### Menggunakan Git

Buat repository kosong di GitHub, buka terminal di folder ini, lalu jalankan:

```bash
git init
git add .
git commit -m "Publish virtual tour"
git branch -M main
git remote add origin https://github.com/USERNAME/NAMA-REPOSITORY.git
git push -u origin main
```

Setelah itu aktifkan Pages dari branch `main` dan folder `/(root)` seperti langkah di atas.

## Pengujian lokal

Tur perlu dibuka melalui HTTP, bukan langsung dengan membuka `index.html` sebagai `file://`.

```bash
python -m http.server 8000
```

Kemudian buka `http://localhost:8000/` pada browser.
