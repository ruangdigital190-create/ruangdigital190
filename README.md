# RUANGDIGITAL190 — GitHub Pages

Website katalog statis untuk **RUANGDIGITAL190**. Dibuat dalam satu file utama `index.html` (HTML, CSS, dan JavaScript sudah menyatu).

## Fitur

- Katalog aplikasi premium dan top up game.
- Logo aplikasi/game ditampilkan melalui URL logo eksternal.
- Filter kategori dan kolom pencarian.
- Klik **Lihat Detail** untuk membuka popup paket, keterangan, harga, dan stok.
- Tombol **Cek Harga WA** pada setiap produk.
- Tombol WhatsApp mengambang yang bisa digeser.
- Tidak ada keranjang belanja.
- Harga, stok, deskripsi, paket, metode pembayaran, dan nomor WhatsApp bisa diedit dari kode.
- Siap dipasang di GitHub Pages.

## Sebelum dipublikasikan: ubah nomor WhatsApp

Buka `index.html`, cari:

```js
const STORE = {
  name: "RUANGDIGITAL190",
  whatsapp: "6285725423328",
```

Nomor ditulis dengan kode negara, tanpa tanda `+`, spasi, atau strip. Contoh Indonesia: `6281234567890`.

## Cara mengubah harga dan stok

Cari bagian `const PRODUCTS = [...]`.

Contoh satu varian:

```js
{ name: "Privat — 1 Bulan", price: 25000, stock: "Ready", note: "Akses privat" }
```

- `price: 25000` berarti harga Rp25.000.
- `price: null` berarti tampil sebagai **Tanya Admin**.
- `stock: "Ready"` berarti tersedia.
- `stock: "Slow"` berarti stok/proses terbatas.
- `stock: "Habis"` berarti tidak tersedia.

Untuk mengubah nama produk, deskripsi, paket, atau logo, edit properti produk yang sama pada bagian `PRODUCTS`.

**Catatan:** website statis ini tidak memiliki database/admin panel online. Perubahan pada file lokal belum otomatis mengubah website publik. Setelah mengedit `index.html`, unggah/commit perubahan ke repository GitHub agar versi publik ikut diperbarui.

## Logo dan gambar

Logo aplikasi/game menggunakan URL dari Simple Icons dan favicon domain resmi. Gambar logo membutuhkan koneksi internet agar dapat dimuat. Jika suatu logo dari sumber tertentu tidak tersedia, kode akan mencoba URL fallback favicon.

## Cara upload ke GitHub

1. Masuk ke https://github.com dan login.
2. Klik tombol **New repository**.
3. Isi nama repository, misalnya `ruangdigital190`.
4. Pilih **Public** agar website bisa diakses publik.
5. Klik **Create repository**.
6. Di halaman repository, klik **Add file** → **Upload files**.
7. Unggah `index.html`, `README.md`, dan `.nojekyll` dari paket ini.
8. Klik **Commit changes**.

## Cara mengaktifkan GitHub Pages

1. Buka repository yang baru dibuat.
2. Masuk ke **Settings** → **Pages**.
3. Pada bagian **Build and deployment**, pilih **Deploy from a branch**.
4. Pilih branch **main** dan folder **/(root)**.
5. Klik **Save**.
6. Tunggu proses publikasi selesai. Link website akan muncul pada bagian GitHub Pages, biasanya berbentuk:

   `https://USERNAME.github.io/ruangdigital190/`

Ganti `USERNAME` dengan username GitHub milikmu.

## Cara memperbarui katalog setelah website online

1. Edit `index.html` di komputer atau langsung dari GitHub.
2. Ubah data pada bagian `STORE` atau `PRODUCTS`.
3. Simpan dan lakukan **Commit changes**.
4. Tunggu GitHub Pages selesai melakukan deployment ulang.

## Catatan penting

- Pastikan seluruh harga, masa aktif, dan status stok benar sebelum dipublikasikan.
- Konfirmasikan detail layanan dan pembayaran dengan pelanggan sebelum transaksi.
- Jangan memasukkan password akun pelanggan ke halaman publik.
