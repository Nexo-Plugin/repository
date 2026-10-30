# Nexo Plugin

Katalog plugin NexoBill. Berkas `repository.json` dibaca oleh Plugin Manager di NexoBill.
Isinya hanya nama, deskripsi, dan versi. Kode plugin ada di repo privat masing-masing dan hanya bisa diunduh oleh akun GitHub yang diberi akses.

## Kontak pembelian

Bagian `contact` di `repository.json` dipakai tombol Beli di Plugin Manager:

- `whatsapp`: nomor, boleh diawali 0 atau 62 (contoh `085895398951`)
- `telegram`: username, boleh memakai @ (contoh `@Exoforb`)

Bila salah satu dikosongkan, pilihannya tidak muncul. Bila keduanya kosong, tombol Beli tidak muncul. Tombol hanya tampil untuk plugin dengan `"access": "paid"`.

## Gambar plugin (galeri slide)

Gambar disimpan di repo ini, satu folder per plugin, lalu didaftarkan di `repository.json`:

```
images/genieacs-manager/1.png
images/genieacs-manager/2.png
images/mikromon/1.png
```

```json
{
  "id": "genieacs-manager",
  "images": [
    "images/genieacs-manager/1.png",
    "images/genieacs-manager/2.png"
  ]
}
```

Mengubah gambar:

- Ganti isi gambar: timpa file `images/<id-plugin>/N.png` dengan nama yang sama, lalu push. Bila gambar tidak berubah di panel, tambahkan angka baru pada nama file (misalnya `1-v2.png`) dan ubah daftarnya.
- Tambah atau kurangi gambar: ubah daftar `images`. Urutan daftar = urutan slide.
- Setelah push, klik Muat ulang di Plugin Manager (tanpa itu, panel memperbarui sendiri maksimal 6 jam kemudian).

Aturan:

- Format: png, jpg, webp, atau gif. Maksimal 8 gambar per plugin.
- Yang diterima hanya path relatif di repo ini atau alamat `https://i.imgur.com/<id>.png`. Alamat lain ditolak.
- Kartu menampilkan gambar dengan rasio lebar 21:9, bagian atas gambar diutamakan. Klik gambar untuk membuka ukuran penuh.
- Plugin tanpa gambar menampilkan ikon plugin sebagai pengganti.
