# Nexo Plugin

Katalog plugin NexoBill. Berkas `repository.json` dibaca oleh Plugin Manager di NexoBill.
Isinya hanya nama, deskripsi, dan versi. Kode plugin ada di repo privat masing-masing dan hanya bisa diunduh oleh akun GitHub yang diberi akses.

## Kontak pembelian

Bagian `contact` di `repository.json` dipakai tombol Beli di Plugin Manager:

- `whatsapp`: nomor, boleh diawali 0 atau 62 (contoh `085895398951`)
- `telegram`: username, boleh memakai @ (contoh `@Exoforb`)

Bila salah satu dikosongkan, pilihannya tidak muncul. Bila keduanya kosong, tombol Beli tidak muncul. Tombol hanya tampil untuk plugin dengan `"access": "paid"`.
