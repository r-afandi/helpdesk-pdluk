# Chat Bantuan (Admin & Helpdesk)

Panduan menangani percakapan bantuan dari pengguna AMDALNET.

## Siapa yang dapat menggunakan

| Fitur | Admin / Admin-child | Helpdesk (Agen) |
|---|:---:|:---:|
| Melihat daftar chat | ✅ semua chat | ✅ default: chat yang ditugaskan ke dirinya |
| Membalas & mengakhiri chat | ✅ | ✅ |
| Menugaskan chat ke agen | ✅ | ❌ (hanya melihat nama agen) |
| Pengaturan (Template, SMTP, Agen, Jam Operasional, Hari Libur) | ✅ | Sesuai hak akses |

?> Buka menu **Chat Bantuan** (ikon 💬) di sidebar setelah login.

## 1. Daftar Chat

<!-- ![Daftar Chat](images/daftar-chat.png) -->

### Kolom tabel

- **ID**: kode unik chat.
- **Tanggal Mulai**: waktu pengguna memulai chat.
- **Nama, Email, Nama Instansi**: data pengaju.
- **Update Terakhir**: potongan pesan terakhir beserta waktunya.
- **Status**:
  - 🔴 **Menunggu Admin**: pengguna menunggu balasan petugas.
  - ⚪ **Menunggu User**: petugas sudah membalas, menunggu pengguna.
  - ⚫ **Selesai**: chat sudah diakhiri.
- **Penugasan**: agen yang menangani chat.
- **Aksi**: **Masuk Chat** (chat aktif) atau **Lihat Chat** (chat selesai).

### Filter

| Filter | Keterangan |
|---|---|
| Pencarian | ID, nama, email, No. HP, atau nama instansi. Hasil muncul otomatis setelah berhenti mengetik. |
| Status | Bisa pilih lebih dari satu. |
| Agen | Pilih satu atau beberapa agen, atau **Belum ditugaskan**. |
| Tanggal | Rentang tanggal mulai chat. |
| **Reset** | Mengembalikan semua filter ke kondisi awal. |

?> **Filter default.** Helpdesk: filter Agen otomatis berisi nama sendiri, sehingga hanya chat yang ditugaskan kepadanya yang tampil. Hapus filter tersebut untuk melihat chat lain. Admin: semua chat tampil.

## 2. Menugaskan Chat ke Agen (khusus Admin)

1. Pada kolom **Penugasan**, klik dropdown di baris chat.
2. Cari agen berdasarkan nama atau email, lalu pilih.
3. Penugasan tersimpan otomatis dan muncul notifikasi *Penugasan berhasil diperbarui*.
4. Untuk melepas penugasan, klik ikon ✕ pada dropdown.

!> Hanya **agen aktif** yang bisa dipilih. Chat berstatus **Selesai** tidak dapat ditugaskan ulang.

## 3. Membalas Chat

Klik **Masuk Chat**. Ruang chat terbuka di **tab baru**; mengklik chat yang sama lagi akan memakai tab yang sama.

<!-- ![Ruang Chat](images/ruang-chat.png) -->

### Header

- Nama pengaju dan kode chat. Klik kode untuk menyalinnya.
- Label status chat.
- Tombol 🔄 **Muat ulang**. Pesan baru **tidak muncul otomatis**, jadi klik tombol ini untuk melihat balasan terbaru dari pengguna.

### Mengirim pesan

- Ketik pesan (maks. **1.000 karakter**), lalu tekan **Enter** atau tombol kirim ➤.
- **Shift + Enter** membuat baris baru.
- Di perangkat layar sentuh, Enter membuat baris baru; gunakan tombol kirim.
- Tombol 😊 untuk menyisipkan emoji.
- Link di dalam pesan otomatis bisa diklik.

### Lampiran

Klik 📎 lalu pilih **Gambar**, **Video**, atau **Dokumen**, atau seret file langsung ke area chat.

| Jenis | Format | Ukuran maks. |
|---|---|---|
| Gambar | JPG, JPEG, PNG | 10 MB per file |
| Dokumen | PDF, DOCX, ZIP | 10 MB per file |
| Video | MP4, MOV, WEBM | 50 MB per file |

Maksimal **5 file per pesan**. Sebelum dikirim, file tampil di layar pratinjau; Anda bisa menambah atau menghapus file dan menulis keterangan.

Lampiran yang diterima bisa dibuka, **diunduh**, atau **disalin link-nya** melalui ikon ▾ di samping file.

### Template balasan

Ada dua cara memakai template:

1. Klik tombol **☰ Menu** di kiri kolom ketik, lalu pilih template di bagian **Template balasan**.
2. Ketik **`/`** diikuti judul template (contoh: `/salam`). Pilih dengan ↑ ↓, lalu tekan **Enter** atau **Tab**. **Esc** untuk membatalkan.

Isi template masuk ke kolom ketik dan masih bisa diedit sebelum dikirim. Gunakan **Hapus template** di Menu untuk mengosongkannya kembali.

## 4. Mengakhiri Chat

1. Klik **☰ Menu** lalu **Akhiri chat**. Kolom ketik berubah menjadi mode *Tulis pesan penutup*. Jika sudah ada template dengan slot `salam-penutup`, isinya otomatis terisi.
2. Tulis atau sesuaikan pesan penutup, lalu klik kirim.
3. Konfirmasi **Kirim & Akhiri**.

Untuk membatalkan sebelum mengirim, klik **☰ Menu** lalu **Batal akhiri chat**.

!> Chat yang sudah diakhiri **tidak dapat dibuka kembali** dan tidak bisa menerima pesan baru. Riwayatnya tetap bisa dilihat lewat **Lihat Chat**.

?> Jika pesan terkirim tetapi chat gagal diakhiri, chat tetap terbuka. Ulangi langkah mengakhiri chat.

## 5. Pengaturan Chat

Klik tombol ⚙️ **Pengaturan** di kanan atas halaman Chat Bantuan.

### 5.1 Template Chat

Balasan siap pakai untuk petugas.

1. Klik **Tambah Template**.
2. Isi **Judul**, **Slot**, dan **Isi** (maks. 1.000 karakter).
3. Klik **Simpan**.

**Slot** menandai fungsi template (huruf kecil, angka, `_` atau `-`, maks. 20 karakter). Slot rekomendasi:

| Slot | Kegunaan |
|---|---|
| `salam-pembuka` | Salam pembuka |
| `jawaban-cepat` | Jawaban yang sering dipakai |
| `tindak-lanjut` | Pesan tindak lanjut |
| `salam-penutup` | Otomatis terisi saat **Akhiri chat** |
| `luar-jam-kerja` | Balasan di luar jam operasional |

Setiap slot rekomendasi hanya bisa dipakai satu template. Edit atau hapus template melalui ikon ⋯ pada kartu template.

### 5.2 SMTP

Akun email untuk mengirim notifikasi chat ke pengguna.

1. Klik **Tambah SMTP**.
2. Isi **Nama Akun, Nama Pengirim, Alamat Pengirim, Host, Port, Enkripsi** (Tanpa / TLS / SSL), **Username, Password**.
3. (Opsional) Isi **Kirim Email Test**, lalu klik **Kirim Test** untuk menguji koneksi.
4. Klik **Simpan**.

Melalui menu ⋯:

- **Jadikan default**: hanya satu akun yang menjadi default.
- **Edit**: kosongkan Password jika tidak ingin mengubahnya.
- **Hapus**: akun default tidak bisa dihapus.

### 5.3 Agen Chat

Mengelola petugas yang menangani chat.

- **Tambah Agen**: cari pengguna berdasarkan nama atau email, lalu **Simpan**.
- **Status**: aktifkan atau nonaktifkan agen dengan switch. Agen nonaktif tidak bisa dipilih di kolom Penugasan.
- **Chat Aktif**: jumlah chat yang sedang ditangani agen.
- **Hapus**: mengeluarkan agen dari daftar.

### 5.4 Jam Operasional

Chat yang masuk di luar jam ini menerima **balasan otomatis**.

1. Nyalakan switch untuk hari kerja, lalu atur jam **buka** dan **tutup**.
2. Hari yang switch-nya mati dianggap **Tutup**.
3. Klik **Simpan**.

### 5.5 Hari Libur

Daftar tanggal libur layanan chat.

1. Klik **Tambah Libur**.
2. Pilih **Tanggal** dan isi **Keterangan** (contoh: *Cuti Bersama Idul Fitri*).
3. Klik **Simpan**.

Daftar bisa difilter berdasarkan tahun, bulan, dan keterangan. Gunakan **Ubah** atau **Hapus** di kolom Aksi.

## FAQ

**Pesan dari pengguna tidak muncul?**
Klik 🔄 di kanan atas ruang chat. Pesan tidak diperbarui otomatis.

**Dropdown Penugasan tidak bisa diklik?**
Hanya Admin yang bisa menugaskan, dan chat yang sudah Selesai tidak bisa diubah.

**Tidak bisa mengirim pesan?**
Pastikan pesan tidak kosong dan chat belum diakhiri.

**Lampiran ditolak?**
Periksa format, ukuran (10 MB / 50 MB untuk video), dan jumlah file (maks. 5).
