# ⠃⠗⠁⠊⠇⠇⠑ Braille Translator

Aplikasi web **Braille Translator** berbasis HTML, CSS, dan JavaScript tanpa backend dan tanpa database. Aplikasi dapat dijalankan langsung di browser melalui localhost.

## 📁 Struktur File

Letakkan file berikut dalam satu folder yang sama:

```text
braille-translator/
├── index.html      # Halaman utama translator
├── braille.html    # Halaman informasi/referensi Braille A–Z
└── README.md       # Dokumentasi dan tutorial instalasi
```

> **Catatan:** `braille.html` adalah halaman **informasi/referensi**, bukan halaman input translator. Tabel A–Z digunakan untuk melihat pasangan huruf dan simbol Braille.

---

## ✨ Fitur

### Halaman utama — `index.html`

- 📝 **Teks → Braille** secara otomatis.
- ⠃⠗⠁⠊⠇⠇⠑ **Braille → Teks**.
- ⌨️ Keyboard Braille 6 titik.
- 🖥️ Mode **Perkins** menggunakan keyboard fisik komputer/laptop.
- 📳 Dukungan getaran pada perangkat yang kompatibel.
- 📋 Copy hasil/input.
- 🔊 Text-to-Speech untuk hasil teks.
- 🌐 Menu bahasa:
  - 🇮🇩 Indonesia
  - 🇬🇧 English
  - 🇮🇳 Hindi
  - 🇲🇾 Malaysia
- 🎨 3 mode tampilan:
  - ☀️ Light
  - 🌙 Dark
  - 👁️ Low Vision

### Halaman informasi — `braille.html`

- 🔤 Tabel referensi Braille **A–Z**.
- Nomor titik Braille untuk setiap huruf.
- Tidak mengirim atau memasukkan data ke kotak input translator.
- 🌐 Menu bahasa yang mengikuti konsep halaman utama.
- 🎨 3 mode tampilan: Light, Dark, Low Vision.
- ⌨️ Shortcut keyboard untuk berpindah tampilan dan kembali ke halaman utama.

---

## ⌨️ Shortcut

### `index.html`

| Shortcut | Fungsi |
|---|---|
| `Alt + B` | Buka/kembali ke halaman Referensi Braille |
| `Alt + 1` | Mode Light |
| `Alt + 2` | Mode Dark |
| `Alt + 3` | Mode Low Vision |
| `Alt + L` | Fokus ke menu Bahasa |

### `braille.html`

| Shortcut | Fungsi |
|---|---|
| `Alt + B` | Kembali ke halaman utama |
| `Alt + 1` | Mode Light |
| `Alt + 2` | Mode Dark |
| `Alt + 3` | Mode Low Vision |
| `Alt + L` | Fokus ke menu Bahasa |

> Shortcut menggunakan kombinasi `Alt`, sehingga umumnya tidak mengganggu pengetikan pada input atau textarea.

---

# 🚀 Tutorial Install di Localhost

## Metode 1 — Python HTTP Server

Metode ini paling sederhana dan tidak membutuhkan Apache/XAMPP.

### 1. Install Python

Pastikan Python sudah tersedia.

Cek dengan:

```bash
python --version
```

atau pada sebagian sistem:

```bash
python3 --version
```

### 2. Buat folder project

Contoh:

```text
C:\braille-translator\
```

atau Linux/macOS:

```text
~/braille-translator/
```

Masukkan file:

```text
index.html
braille.html
README.md
```

ke folder tersebut.

### 3. Buka Terminal / Command Prompt

Masuk ke folder project.

**Windows:**

```bat
cd C:\braille-translator
```

**Linux/macOS:**

```bash
cd ~/braille-translator
```

### 4. Jalankan server lokal

Windows/macOS/Linux:

```bash
python -m http.server 8000
```

Jika command `python` tidak tersedia, coba:

```bash
python3 -m http.server 8000
```

### 5. Buka di browser

Akses:

```text
http://localhost:8000/
```

Halaman utama akan membuka:

```text
http://localhost:8000/index.html
```

Halaman referensi:

```text
http://localhost:8000/braille.html
```

### 6. Menghentikan server

Kembali ke terminal kemudian tekan:

```text
Ctrl + C
```

---

# 🟢 Metode 2 — VS Code + Live Server

Metode ini cocok untuk pengembangan karena halaman otomatis dapat dimuat ulang setelah perubahan.

### 1. Install Visual Studio Code

Buka project folder `braille-translator` di VS Code.

### 2. Install extension Live Server

Cari extension:

```text
Live Server
```

Kemudian install.

### 3. Jalankan

Klik kanan `index.html` → **Open with Live Server**.

Browser biasanya akan membuka alamat seperti:

```text
http://127.0.0.1:5500/index.html
```

`braille.html` dapat dibuka dari link Referensi Braille atau langsung melalui alamat:

```text
http://127.0.0.1:5500/braille.html
```

---

# 🟦 Metode 3 — XAMPP / Apache

Gunakan metode ini bila project akan dikembangkan bersama project PHP/Apache lain.

### 1. Install XAMPP

Pastikan Apache dapat dijalankan.

### 2. Salin project

Masukkan folder project ke:

```text
C:\xampp\htdocs\braille-translator\
```

Sehingga menjadi:

```text
C:\xampp\htdocs\braille-translator\index.html
C:\xampp\htdocs\braille-translator\braille.html
C:\xampp\htdocs\braille-translator\README.md
```

### 3. Jalankan Apache

Buka XAMPP Control Panel dan klik **Start** pada Apache.

### 4. Buka aplikasi

```text
http://localhost/braille-translator/
```

Halaman referensi:

```text
http://localhost/braille-translator/braille.html
```

---

# 🔧 Tidak Ada Build / Package Manager

Project ini merupakan aplikasi web statis. Tidak diperlukan:

- Node.js
- `npm install`
- Composer
- Database
- PHP untuk menjalankan fitur translator
- Framework frontend

Cukup letakkan file HTML di satu folder dan jalankan melalui web server lokal.

---

# 🌐 Bahasa

Pilihan bahasa tersedia melalui menu **Bahasa**. Pengaturan bahasa disimpan menggunakan `localStorage` browser sehingga preferensi dapat dipertahankan pada penggunaan berikutnya.

Bahasa yang disediakan pada project:

```text
id = Indonesia
 en = English
 in = Hindi
 ms = Malaysia
```

> Kode `in` digunakan oleh project untuk bahasa Hindi sesuai implementasi yang ada pada file HTML.

---

# 🎨 Mode Tampilan

Tersedia tiga mode visual:

1. **Light** — tampilan terang.
2. **Dark** — tampilan gelap.
3. **Low Vision** — kontras tinggi dengan ukuran Braille lebih besar.

Pengaturan tema juga disimpan di browser menggunakan `localStorage`.

---

# 🔤 Halaman `braille.html`

Halaman ini dibuat khusus sebagai **referensi/informasi**.

Tabel menyediakan:

```text
Huruf → Simbol Braille → Nomor titik
```

Contoh:

```text
A → ⠁ → titik 1
B → ⠃ → titik 1-2
C → ⠉ → titik 1-4
```

Tabel tidak digunakan sebagai mekanisme input translator. Tujuannya adalah membantu pengguna mempelajari dan mengenali bentuk Braille A–Z.

---

# 🧪 Pengujian Setelah Install

Setelah localhost aktif, cek bagian berikut:

### Halaman utama

- Buka `index.html`.
- Ketik contoh:

```text
Braille
```

- Pastikan hasil Braille muncul otomatis.
- Ganti ke **Braille → Teks** dan uji Unicode Braille.
- Uji Light, Dark, dan Low Vision.
- Uji menu Bahasa.
- Uji `Alt + B`, `Alt + 1`, `Alt + 2`, `Alt + 3`, dan `Alt + L`.

### Halaman referensi

- Buka `braille.html`.
- Pastikan tabel A–Z tampil.
- Pastikan tidak ada kolom input translator pada halaman tersebut.
- Uji pergantian bahasa.
- Uji tiga mode tampilan.
- Uji shortcut.
- Klik **Kembali ke Translator** untuk kembali ke `index.html`.

---

# 🛠️ Troubleshooting

## Port 8000 sudah digunakan

Gunakan port lain, misalnya:

```bash
python -m http.server 8080
```

Kemudian buka:

```text
http://localhost:8080/
```

## Halaman tidak berubah setelah edit

Lakukan hard refresh:

```text
Ctrl + F5
```

atau:

```text
Ctrl + Shift + R
```

## Shortcut tidak bekerja

Pastikan browser sedang berada pada halaman project dan gunakan kombinasi:

```text
Alt + 1
Alt + 2
Alt + 3
Alt + B
Alt + L
```

## Tampilan bahasa/tema kembali ke default

Project menyimpan pengaturan menggunakan `localStorage`. Menghapus site data/browser storage akan menghapus preferensi tersebut.

---

# 📌 Catatan Pengembangan

Untuk deployment sederhana, cukup upload:

```text
index.html
braille.html
```

`README.md` hanya untuk dokumentasi dan tidak diperlukan oleh browser agar aplikasi berjalan.

Aplikasi dapat di-host pada web server statis karena tidak menggunakan backend.

live demo
NonTTS
https://bahrizalmulyawan.github.io/braille1/
TTS
https://bahrizalmulyawan.github.io/braille2/


---

## ✅ Quick Start

```bash
# 1. Masuk folder project
cd braille-translator

# 2. Jalankan localhost
python -m http.server 8000


## ✅ Live Demo
```bash
NonTTS
https://bahrizalmulyawan.github.io/braille1/
TTS
https://bahrizalmulyawan.github.io/braille2/


Selamat menggunakan **Braille Translator**! ⠃⠗⠁⠊⠇⠇⠑
