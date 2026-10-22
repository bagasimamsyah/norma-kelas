# Norma Kelas: panduan memasang (repository baru)

Aplikasi ini **terpisah** dari Komitmen Quest. Repository `komitmen-quest` tidak perlu diubah atau dihapus.

- **Database Supabase:** tidak perlu disetel lagi. Aplikasi ini memakai database yang sama, yang sudah terpasang.
- **config.js:** sudah terisi.

## Langkah 1: Buat repository baru di GitHub
1. Buka github.com, klik tombol **+** di kanan atas, lalu pilih **New repository**.
2. Isi *Repository name* dengan `norma-kelas`, lalu klik **Create repository**.
3. Di halaman berikutnya, klik tautan **uploading an existing file**.
4. Ekstrak file zip terlebih dahulu. Lalu seret **isi** folder `norma-kelas` ke halaman GitHub:
   - `index.html`
   - `config.js`
   - `PANDUAN-SETUP.md`
   - folder `vendor`
5. Klik **Commit changes**.

## Langkah 2: Tayangkan di Vercel
1. Buka vercel.com, lalu pilih **Add New…** → **Project**.
2. Cari repositori `norma-kelas`, lalu klik **Import**.
3. Pada *Framework Preset*, pilih **Other**, lalu klik **Deploy**.
4. Anda akan mendapat tautan baru, misalnya `norma-kelas.vercel.app`.

Tidak perlu mengisi Environment Variables. Jangan memakai kunci *service_role* atau *secret*.

## Cara memakai di kelas
1. **Pengajar** (di laptop):
   - Buka tautan Vercel, lalu klik **Saya pengajar**.
   - Isi nama kelas, lalu klik **Buat kelas baru**.
   - Papan langsung terbuka. Tekan **Layar penuh** dan tayangkan di Zoom atau proyektor.
2. **Peserta** (di HP):
   - Scan QR di papan. Kode kelas akan terisi otomatis.
   - Isi nama, pilih 3 norma, lalu tekan **Kirim**.
   - Janji pribadi boleh diisi, boleh juga dikosongkan.
3. Papan diperbarui setiap 3 detik. Norma yang paling banyak dipilih tampil paling besar.

## Tombol di papan (hanya muncul di laptop pembuat kelas)
| Tombol | Fungsi |
|---|---|
| Tutup / Buka pengisian | Menghentikan atau membuka kiriman baru |
| Moderasi kata | Klik kata di papan untuk menyembunyikannya |
| Tampilkan kata tersembunyi | Mengembalikan semua kata yang disembunyikan |
| Reset jawaban | Menghapus semua jawaban kelas ini. Klik 2 kali untuk konfirmasi |
| Tampilkan janji | Menampilkan janji peserta, tanpa nama |
| Salin tautan kendali | Membuka papan dengan tombol pengatur di laptop lain. **Jangan dibagikan ke peserta** |

## Mengubah daftar norma
1. Di GitHub, buka `index.html`, lalu klik ikon pensil.
2. Cari baris `const NORMS = [`. Ubah, tambah, atau hapus teks di antara tanda kutip. Panjang tiap norma maksimal 40 karakter, dan antarnorma dipisahkan koma.
3. Klik **Commit changes**. Vercel akan memperbarui situs dalam sekitar 1 menit.

## Catatan
- Satu HP dihitung satu suara. Jika peserta mengubah pilihan, kiriman lamanya diganti, bukan ditambah.
- Kode kelas dari Komitmen Quest juga berlaku di aplikasi ini, dan sebaliknya.
