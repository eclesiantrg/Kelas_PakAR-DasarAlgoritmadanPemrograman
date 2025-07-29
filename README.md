# Nama : Eclesia Ollevia Putri Maura Natarang (24110310018)
# Prodi : Bisnis Digital 2A

# 📦 Tugas 2 – Dokumentasi Teknis Inventori Toko

## 1. Struktur File & Fungsi

Program ini dibuat dalam 1 file Python aja (`inventori.py`). Di dalamnya ada beberapa fungsi yang dibikin supaya programnya rapi dan gampang dibaca. Nama-nama variabel juga disingkat biar simpel, misalnya `b` itu artinya barang.

Fungsi-fungsi yang dipakai:
- `add_barang()` → nambahin data barang (kode, nama, stok, harga)
- `lihat_all()` → nampilin semua barang
- `edit_stok()` → ubah stok dan harga barang
- `dlte_barang()` → hapus barang
- `report_stok()` → laporan stok dari terbanyak
- `laporan_ringkas()` → total jenis dan nilai barang
- `cari_barang()` → cari barang berdasarkan kode
- `save_data()` dan `load_data()` → simpen dan ambil data dari file JSON

---

## 2. Library yang Dipakai

- **`json`** → buat simpen dan ambil data dari file `inventori.json`
- **`time`** → buat ngukur waktu proses (dipake di tampilan data & laporan, biar tau performa program)

---

## 3. Alur Jalan Program

- Pas program dijalanin, data yang lama dimuat dulu dari `inventori.json` (kalau filenya ada).
- Abis itu, menu utama ditampilin ke pengguna.
- Pengguna bisa pilih: tambah, lihat, edit, hapus, laporan, cari barang, atau keluar.
- Kalau milih **"simpan & keluar"**, data langsung disimpen ke file JSON, dan program selesai.
- Di dalam kodenya udah ada komentar-komentar biar gampang ngerti alur tiap bagian.
- Beberapa bagian program udah dioptimasi (misalnya pake `time` buat ngukur durasi proses).

---

# 📘 Tugas 3 - User Manual Aplikasi Inventori Sederhana

## ✅ 1. Cara Menjalankan Aplikasi
1. Pastikan Python sudah terinstal di komputer kamu.

2. Simpan file program ini sebagai main.py.

3. Jalankan melalui terminal atau CMD:
   python main.py
   
4. File data akan otomatis disimpan dalam inventori.json.

## ✅ 2. Contoh Input
Menu: Tambah Barang (1)
Kode barang: BRG001
Nama barang: Bolpen
Jumlah stok: 100
Harga barang: 2000

## ✅ 3. Cara Edit & Hapus Data
Edit (Menu 3)

- Masukkan kode barang yang ingin diedit, lalu isi stok dan harga baru.

- Hapus (Menu 4)

- Masukkan kode barang yang ingin dihapus. Barang akan langsung dihapus dari inventori.

---

## 🔍Tugas 4 - Pengujian & Evaluasi

### Skenario 1: Tambah dan Lihat Barang
- Langkah:
  1. Pilih menu [1] Tambah Barang
  2. Input 5 barang:
     - 001 - Cimory (Stok: 150, Harga: 6500)
     - 002 - Oreo (Stok: 150, Harga: 8000)
     - 003 - Coklat Silverqueen (Stok: 100, Harga: 20000)
     - 004 - Yogurt (Stok: 40, Harga: 7000)
     - 005 - Air Mineral (Stok: 1000, Harga: 3000)
  3. Pilih menu [2] Lihat Semua Barang
- Hasil:
  - Semua barang berhasil ditambahkan dan ditampilkan dengan benar.
  - Ditampilkan dalam waktu: 0.000041 detik
- Status: ✅ Berhasil

---

### Skenario 2: Edit dan Hapus Barang
- Langkah:
  1. Pilih menu [3] Edit Stok & Harga
     - Kode: 004
     - Stok baru: 20
     - Harga baru: 6000
  2. Pilih menu [4] Hapus Barang
     - Kode: 004
  3. Pilih menu [2] Lihat Semua Barang
- Hasil:
  - Data Yogurt berhasil diubah, lalu dihapus
  - Tidak muncul lagi di daftar barang
- Status: ✅ Berhasil

---

### Skenario 3: Laporan Stok
- Langkah:
  1. Pilih menu [5] Laporan Stok
- Hasil:
  - Daftar barang diurutkan dari stok terbanyak ke terkecil:
    1. Air Mineral (1000)
    2. Cimory (150)
    3. Oreo (150)
    4. Coklat Silverqueen (100)
  - Proses cepat: 0.000035 detik
- Status: ✅ Berhasil

---

### Skenario 4: Laporan Ringkas
- Langkah:
  1. Pilih menu [6] Laporan Ringkas
- Hasil:
  - Total jenis barang: 4
  - Total nilai inventori: Rp7.175.000
- Status: ✅ Berhasil

---

### Skenario 5: Pencarian Barang
- Langkah:
  1. Pilih menu [7] Cari Barang
     - Kode: 002
- Hasil:
  - Barang ditemukan: Oreo (Stok: 150, Harga: 8000)
- Status: ✅ Berhasil

---

### Skenario 6: Simpan & Keluar
- Langkah:
  1. Pilih menu [8] Simpan & Keluar
- Hasil:
  - Data disimpan, aplikasi keluar dengan normal
- Status: ✅ Berhasil

