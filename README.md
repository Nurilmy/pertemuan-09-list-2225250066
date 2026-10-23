# Pertemuan 09 - List dan Pengolahan Data Numerik

Nama: Nuril Ilmy
NIM: 2225250066
Kelas: 3E

## Tujuan
Mengolah kumpulan data numerik dengan list Python.

## Struktur Program
- `latihan/01_buat_list.py` : membuat dan membaca list
- `latihan/02_indeks_slicing.py` : indeks dan slicing
- `latihan/03_manipulasi_list.py` : ubah, tambah, sisip, hapus elemen
- `latihan/04_agregasi_nilai.py` : total, rata-rata, minimum, maksimum
- `latihan/05_filter_kelulusan.py` : menyaring nilai yang lulus
- `latihan/06_fungsi_statistik.py` : fungsi rata-rata
- `praktik/analisis_nilai_mahasiswa.py` : analisis nilai mahasiswa

## Cara Menjalankan
```
python3 praktik/analisis_nilai_mahasiswa.py
```
(Di Windows gunakan `python`.)

## Test Case
| Data | Yang diperiksa | Hasil yang diharapkan | Hasil aktual | Status |
|------|----------------|-----------------------|--------------|--------|
| [60, 70, 80] | Rata-rata | 70.00 | 70.00 | Lulus |
| [60, 70, 80] | Minimum / maksimum | 60 / 80 | 60 / 80 | Lulus |
| [60, 70, 80] | Jumlah lulus | 3 | 3 | Lulus |
| [59, 60, 61] | Batas kelulusan | 2 lulus | 2 lulus | Lulus |
| [] | Penanganan list kosong pada fungsi rata_rata | Tidak error | 0 (tidak error) | Lulus |

## Refleksi
Satu hal yang saya pahami tentang indeks/list:
Indeks pada list Python dimulai dari 0, bukan 1, sehingga elemen pertama diakses
dengan `nilai[0]` dan elemen terakhir dengan `nilai[-1]`. Pada slicing seperti
`nilai[1:4]`, indeks batas akhir (4) tidak ikut diambil, jadi hasilnya hanya
elemen indeks 1, 2, dan 3.

Satu kesalahan yang berhasil saya perbaiki:
Awalnya saya mengira `nilai[1:4]` ikut mengambil elemen indeks 4. Setelah
mencoba dan membandingkan dengan hasil di terminal, saya memahami bahwa batas
akhir slicing tidak termasuk. Saya juga menambahkan pengecekan `len(data) == 0`
pada fungsi `rata_rata` agar tidak terjadi ZeroDivisionError saat list kosong.

