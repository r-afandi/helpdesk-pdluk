---
title: "Chat Bantuan (Admin & Helpdesk)"
excerpt: "Panduan menangani percakapan bantuan dari pengguna AMDALNET."
---

<Cards columns={3}>
  <Card title="Daftar Chat" href="#1-daftar-chat" icon="fa-list">
    Melihat, mencari, dan memfilter chat masuk.
  </Card>
  <Card title="Membalas Chat" href="#3-membalas-chat" icon="fa-comments">
    Kirim pesan, lampiran, dan template balasan.
  </Card>
  <Card title="Pengaturan" href="#5-pengaturan-chat" icon="fa-gear">
    Template, SMTP, agen, jam operasional, hari libur.
  </Card>
</Cards>

## Siapa yang dapat menggunakan

| Fitur                                                          | Admin / Admin-child | Helpdesk (Agen)                             |
| :------------------------------------------------------------- | :-----------------: | :-----------------------------------------: |
| Melihat daftar chat                                            |    ✅ semua chat     | ✅ default: chat yang ditugaskan ke dirinya |
| Membalas & mengakhiri chat                                     |          ✅          |                     ✅                      |
| Menugaskan chat ke agen                                        |          ✅          |        ❌ (hanya melihat nama agen)         |
| Pengaturan (Template, SMTP, Agen, Jam Operasional, Hari Libur) |          ✅          |              Sesuai hak akses               |

> 📘 Akses menu
>
> Buka menu **Chat Bantuan** (ikon 💬) di sidebar setelah login.

## 1. Daftar Chat

![Daftar Chat](GANTI_DENGAN_URL_SCREENSHOT "Halaman daftar Chat Bantuan")

### Kolom tabel

| Kolom              | Keterangan                                                    |
| :----------------- | :------------------------------------------------------------ |
| **ID**             | Kode unik chat. |
| **Tanggal Mulai**  | Waktu pengguna memulai chat.                                  |
| **Nama, Email, Nama Instansi** | Data pengaju.                                     |
| **Update Terakhir** | Potongan pesan terakhir beserta waktunya.                    |
| **Status**         | 🔴 **Menunggu Admin**: pengguna menunggu balasan petugas.<br/>⚪ **Menunggu User**: petugas sudah membalas.<br/>⚫ **Selesai**: chat sudah diakhiri. |
| **Penugasan**      | Agen yang menangani chat.                                     |
| **Aksi**           | **Masuk Chat** (chat aktif) atau **Lihat Chat** (chat selesai). |

### Filter

| Filter        | Keterangan                                                                                   |
| :------------ | :------------------------------------------------------------------------------------------- |
| Pencarian     | ID, nama, email, No. HP, atau nama instansi. Hasil muncul otomatis setelah berhenti mengetik. |
| Status        | Bisa pilih lebih dari satu.                                                                  |
| Agen          | Pilih satu atau beberapa agen, atau **Belum ditugaskan**.                                    |
| Tanggal       | Rentang tanggal mulai chat.                                                                  |
| **Reset**     | Mengembalikan semua filter ke kondisi awal.                                                  |

<Tabs>
  <Tab title="Admin">
    Semua chat tampil secara default.
  </Tab>
  <Tab title="Helpdesk">
    Filter **Agen** otomatis berisi nama sendiri, sehingga hanya chat yang ditugaskan kepada Anda yang tampil. Hapus filter tersebut untuk melihat chat lain.
  </Tab>
</Tabs>

## 2. Menugaskan Chat ke Agen

> 🚧 Khusus Admin
>
> Helpdesk hanya dapat melihat nama agen yang ditugaskan.

1. Pada kolom **Penugasan**, klik dropdown di baris chat.
2. Cari agen berdasarkan nama atau email, lalu pilih.
3. Penugasan tersimpan otomatis dan muncul notifikasi _Penugasan berhasil diperbarui_.
4. Untuk melepas penugasan, klik ikon ✕ pada dropdown.

> 🚧 Catatan
>
> - Hanya **agen aktif** yang bisa dipilih.
> - Chat berstatus **Selesai** tidak dapat ditugaskan ulang.

## 3. Membalas Chat

Klik **Masuk Chat**. Ruang chat terbuka di **tab baru**; mengklik chat yang sama lagi akan memakai tab yang sama.

![Ruang Chat](GANTI_DENGAN_URL_SCREENSHOT "Tampilan ruang chat")

### Header

- Nama pengaju dan kode chat. Klik kode untuk menyalinnya.
- Label status chat.
- Tombol 🔄 **Muat ulang**.

> 🚧 Pesan tidak muncul otomatis
>
> Klik 🔄 di kanan atas untuk melihat balasan terbaru dari pengguna.

### Mengirim pesan

| Aksi                | Cara                                                    |
| :------------------ | :------------------------------------------------------ |
| Kirim pesan         | **Enter** atau tombol ➤ (maks. **1.000 karakter**)      |
| Baris baru          | **Shift + Enter**                                       |
| Layar sentuh        | Enter membuat baris baru; gunakan tombol ➤              |
| Emoji               | Tombol 😊                                               |
| Link                | Otomatis bisa diklik                                    |

### Lampiran

Klik 📎 lalu pilih **Gambar**, **Video**, atau **Dokumen**, atau seret file langsung ke area chat.

| Jenis   | Format         | Ukuran maks.   |
| :------ | :------------- | :------------- |
| Gambar  | JPG, JPEG, PNG | 10 MB per file |
| Dokumen | PDF, DOCX, ZIP | 10 MB per file |
| Video   | MP4, MOV, WEBM | 50 MB per file |

Maksimal **5 file per pesan**. Sebelum dikirim, file tampil di layar pratinjau; Anda bisa menambah atau menghapus file dan menulis keterangan.

Lampiran yang diterima bisa dibuka, **diunduh**, atau **disalin link-nya** melalui ikon ▾ di samping file.

### Template balasan

<Tabs>
  <Tab title="Lewat Menu">
    1. Klik tombol **☰ Menu** di kiri kolom ketik.
    2. Pilih template di bagian **Template balasan**.
  </Tab>
  <Tab title="Lewat perintah /">
    1. Ketik `/` diikuti judul template, contoh: `/salam`.
    2. Pilih dengan ↑ ↓, lalu tekan **Enter** atau **Tab**.
    3. Tekan **Esc** untuk membatalkan.
  </Tab>
</Tabs>

Isi template masuk ke kolom ketik dan masih bisa diedit sebelum dikirim. Gunakan **Hapus template** di Menu untuk mengosongkannya kembali.

## 4. Mengakhiri Chat

1. Klik **☰ Menu** lalu **Akhiri chat**. Kolom ketik berubah menjadi mode _Tulis pesan penutup_. Jika sudah ada template dengan slot `salam-penutup`, isinya otomatis terisi.
2. Tulis atau sesuaikan pesan penutup, lalu klik kirim.
3. Konfirmasi **Kirim & Akhiri**.

Untuk membatalkan sebelum mengirim, klik **☰ Menu** lalu **Batal akhiri chat**.

> ❗️ Tidak dapat dibatalkan
>
> Chat yang sudah diakhiri **tidak dapat dibuka kembali** dan tidak bisa menerima pesan baru. Riwayatnya tetap bisa dilihat lewat **Lihat Chat**.

> 📘 Jika pesan terkirim tetapi chat gagal diakhiri, chat tetap terbuka. Ulangi langkah mengakhiri chat.

## 5. Pengaturan Chat

Klik tombol ⚙️ **Pengaturan** di kanan atas halaman Chat Bantuan.

<Accordion title="Template Chat" icon="fa-message">
  Balasan siap pakai untuk petugas.

  1. Klik **Tambah Template**.
  2. Isi **Judul**, **Slot**, dan **Isi** (maks. 1.000 karakter).
  3. Klik **Simpan**.

  **Slot** menandai fungsi template (huruf kecil, angka, `_` atau `-`, maks. 20 karakter). Slot rekomendasi:

  | Slot             | Kegunaan                               |
  | :--------------- | :------------------------------------- |
  | `salam-pembuka`  | Salam pembuka                          |
  | `jawaban-cepat`  | Jawaban yang sering dipakai            |
  | `tindak-lanjut`  | Pesan tindak lanjut                    |
  | `salam-penutup`  | Otomatis terisi saat **Akhiri chat**   |
  | `luar-jam-kerja` | Balasan di luar jam operasional        |

  Setiap slot rekomendasi hanya bisa dipakai satu template. Edit atau hapus template melalui ikon ⋯ pada kartu template.
</Accordion>

<Accordion title="SMTP" icon="fa-envelope">
  Akun email untuk mengirim notifikasi chat ke pengguna.

  1. Klik **Tambah SMTP**.
  2. Isi **Nama Akun, Nama Pengirim, Alamat Pengirim, Host, Port, Enkripsi** (Tanpa / TLS / SSL), **Username, Password**.
  3. (Opsional) Isi **Kirim Email Test**, lalu klik **Kirim Test** untuk menguji koneksi.
  4. Klik **Simpan**.

  Melalui menu ⋯:

  - **Jadikan default**: hanya satu akun yang menjadi default.
  - **Edit**: kosongkan Password jika tidak ingin mengubahnya.
  - **Hapus**: akun default tidak bisa dihapus.
</Accordion>

<Accordion title="Agen Chat" icon="fa-users">
  Mengelola petugas yang menangani chat.

  - **Tambah Agen**: cari pengguna berdasarkan nama atau email, lalu **Simpan**.
  - **Status**: aktifkan atau nonaktifkan agen dengan switch. Agen nonaktif tidak bisa dipilih di kolom Penugasan.
  - **Chat Aktif**: jumlah chat yang sedang ditangani agen.
  - **Hapus**: mengeluarkan agen dari daftar.
</Accordion>

<Accordion title="Jam Operasional" icon="fa-clock">
  Chat yang masuk di luar jam ini menerima **balasan otomatis**.

  1. Nyalakan switch untuk hari kerja, lalu atur jam **buka** dan **tutup**.
  2. Hari yang switch-nya mati dianggap **Tutup**.
  3. Klik **Simpan**.
</Accordion>

<Accordion title="Hari Libur" icon="fa-calendar">
  Daftar tanggal libur layanan chat.

  1. Klik **Tambah Libur**.
  2. Pilih **Tanggal** dan isi **Keterangan** (contoh: _Cuti Bersama Idul Fitri_).
  3. Klik **Simpan**.

  Daftar bisa difilter berdasarkan tahun, bulan, dan keterangan. Gunakan **Ubah** atau **Hapus** di kolom Aksi.
</Accordion>

## FAQ

<Accordion title="Pesan dari pengguna tidak muncul?" icon="fa-circle-question">
  Klik 🔄 di kanan atas ruang chat. Pesan tidak diperbarui otomatis.
</Accordion>

<Accordion title="Dropdown Penugasan tidak bisa diklik?" icon="fa-circle-question">
  Hanya Admin yang bisa menugaskan, dan chat yang sudah Selesai tidak bisa diubah.
</Accordion>

<Accordion title="Tidak bisa mengirim pesan?" icon="fa-circle-question">
  Pastikan pesan tidak kosong dan chat belum diakhiri.
</Accordion>

<Accordion title="Lampiran ditolak?" icon="fa-circle-question">
  Periksa format, ukuran (10 MB, atau 50 MB untuk video), dan jumlah file (maks. 5).
</Accordion>
