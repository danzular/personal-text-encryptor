# personal-text-encryptor
A personal browser-based text encryption tool with Deterministic and GCM modes.

# Personal Text Encryptor (PTE)

**Versi:** V1.2  
**Format:** Single-file HTML application  
**Hosting yang direncanakan:** GitHub Pages

Personal Text Encryptor (PTE) adalah alat berbasis browser untuk mengenkripsi dan mendekripsi teks secara personal. Aplikasi disiapkan sebagai satu file HTML agar mudah disimpan, dipindahkan, dan dijalankan melalui browser modern.

## Fitur

- Antarmuka bertema gelap.
- Dua pilihan metode:
  - **PTE1 — Deterministic:** mode enkripsi deterministik.
  - **PTE2 — GCM:** mode enkripsi berbasis GCM.
- Satu aplikasi HTML untuk kedua mode.
- Gerbang akses harian pada halaman awal.
- Tanggal untuk gerbang akses diambil dari layanan waktu server, sesuai implementasi aplikasi.
- Dapat dijalankan melalui browser tanpa instalasi aplikasi khusus.

> Catatan: Detail algoritma, parameter kriptografi, format keluaran, dan kompatibilitas harus mengikuti implementasi HTML V1.2 yang dipublikasikan. README ini tidak menetapkan atau mengubah spesifikasi kriptografi aplikasi.

## Cara menggunakan

1. Buka URL GitHub Pages aplikasi.
2. Ikuti gerbang akses yang ditampilkan pada halaman awal.
3. Pilih mode **PTE1 — Deterministic** atau **PTE2 — GCM**.
4. Masukkan teks dan informasi yang diminta oleh aplikasi.
5. Jalankan proses enkripsi atau dekripsi.
6. Simpan hasil dan informasi yang diperlukan untuk proses dekripsi di kemudian hari.

**Penting:** Untuk mendekripsi data, gunakan metode dan parameter yang sesuai dengan proses enkripsi awal. Kehilangan passphrase/kunci atau parameter yang diwajibkan aplikasi dapat menyebabkan data tidak dapat dipulihkan.

## Deployment ke GitHub Pages

Repository dapat disimpan sebagai **Private**, sementara website GitHub Pages yang dipublikasikan melalui paket GitHub biasa harus dianggap **publik**.

1. Letakkan file aplikasi di root repository.
2. Ubah nama file aplikasi menjadi `index.html`.
3. Buka **Settings → Pages** pada repository.
4. Pada **Build and deployment**, pilih **Deploy from a branch**.
5. Pilih branch `main` dan folder `/ (root)`.
6. Simpan pengaturan dan tunggu proses deployment selesai.
7. Buka URL Pages yang ditampilkan GitHub.

Struktur repository yang disarankan:

```text
personal-text-encryptor/
├── index.html
├── README.md
└── CHANGELOG.md
```

## Batasan dan keamanan

- GitHub Pages menyajikan website secara publik. Jangan menganggap URL atau source HTML sebagai rahasia.
- Gerbang akses di sisi HTML bukan autentikasi server dan tidak dapat mencegah seseorang mengunduh atau memeriksa source code.
- Jangan menanamkan password pribadi, secret key, token, atau kredensial rahasia ke dalam HTML maupun repository.
- Jangan menganggap mode enkripsi deterministik setara dengan enkripsi yang menggunakan nonce/IV acak. Pahami konsekuensi mode yang dipilih sebelum menyimpan data sensitif.
- Simpan salinan cadangan file HTML dan data terenkripsi di lokasi yang aman.
- Pastikan file V1.2 yang dipublikasikan telah diuji untuk skenario enkripsi dan dekripsi sebelum digunakan menyimpan data penting.

## Versi

Lihat [CHANGELOG.md](CHANGELOG.md) untuk catatan perubahan tiap versi.
