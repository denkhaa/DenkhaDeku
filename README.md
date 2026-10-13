# Denkha Market — Website Top Up

## Isi website
- Beranda Denkha dengan banner aesthetic dan pilihan Free Fire / Free Fire MAX.
- Daftar paket dari gambar: membership mingguan/bulanan, custom Rp198/diamond, serta paket 5 sampai 30000 diamond dan harga yang diberikan.
- Pilih produk, kuantitas, input ID, kontak, kode voucher, ringkasan, animasi status, dan rincian order.

## Agar benar-benar menerima QRIS
QRIS live tidak dapat dibuat dari kode website saja. Pemilik harus mempunyai akun merchant terverifikasi dari payment gateway (contoh Midtrans/Xendit), lalu mengintegrasikan API checkout dan webhook verifikasi di backend. Jangan memasukkan server key ke HTML publik. Cek nickname otomatis juga membutuhkan API resmi/supplier yang sah. Voucher diskon 100% harus divalidasi server-side; implementasi browser saja tidak aman untuk transaksi nyata.

File `index.html` adalah front-end. Sebelum integrasi provider selesai, UI sengaja tidak menampilkan QR palsu atau mengklaim pembayaran berhasil.


## QRIS yang diberikan
Gambar QRIS yang kamu unggah disimpan di `assets/qris-wardayz.jpg` dan ditampilkan pada bagian pembayaran. Website menampilkan status **MENUNGGU VERIFIKASI**; ini bukan konfirmasi pembayaran otomatis. Pastikan kamu berwenang memakai QRIS tersebut, nama merchant cocok, dan nominal diverifikasi di aplikasi pembayaran. Untuk status otomatis, integrasikan payment gateway resmi dan webhook server-side.


### Update tampilan
Tampilan diperbarui mengikuti referensi video: banner hero, kartu produk gelap dua kolom, pemilihan game dan modal checkout. Perpindahan menuju QRIS memiliki animasi hitung 1–15 dengan jeda 0,23 detik per langkah (sekitar 3,45 detik). Status tetap menunggu verifikasi karena website belum terhubung ke payment gateway.
