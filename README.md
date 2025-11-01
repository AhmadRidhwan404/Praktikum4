**Nama : Ahmad Ridhwan Ilham (312510222)**

**Mata Kuliah : Pengantar Pemrograman**

    **#LATIHAN 1.py**
# Generator Bilangan Acak Kurang dari 0.5

Program Python sederhana untuk menghasilkan sejumlah bilangan acak yang nilainya lebih kecil dari 0.5.

##  Deskripsi

Program ini menghasilkan `n` bilangan acak dengan nilai kurang dari 0.5. Jumlah bilangan (`n`) ditentukan oleh pengguna saat program dijalankan. Program menggunakan kombinasi loop `while` dan `for` untuk menghasilkan dan menampilkan bilangan acak.

##  Fitur

- Input jumlah bilangan acak secara dinamis saat runtime
- Menghasilkan bilangan acak antara 0 dan 0.5
- Menampilkan hasil dengan format yang rapi dan terurut
- Presisi 6 digit desimal untuk setiap bilangan

##  Cara Menggunakan


### Langkah-langkah

1. **Simpan kode program** dalam file dengan nama `BILANGAN ACAK YANG TIDAK LEBIH KECIL DARI 0,5.py`

2. **Jalankan program** melalui terminal/command prompt:
   ```bash
   python random_generator.py
   ```

3. **Masukkan jumlah bilangan** yang diinginkan saat diminta:
   ```
   Masukkan jumlah bilangan acak (n): 5
   ```

4. **Lihat hasil** yang ditampilkan:
   ```
   5 bilangan acak yang lebih kecil dari 0.5:
   1. 0.234567
   2. 0.123456
   3. 0.456789
   4. 0.098765
   5. 0.345678
   ```

##  Contoh Output

```
Masukkan jumlah bilangan acak (n): 3

3 bilangan acak yang lebih kecil dari 0.5:
1. 0.123456
2. 0.456123
3. 0.234890
```

##  Cara Kerja Program

1. **Import Module**: Program mengimpor fungsi `random()` dari modul `random`
2. **Input Pengguna**: Meminta pengguna memasukkan nilai `n` (jumlah bilangan yang diinginkan)
3. **Generasi Bilangan**: 
   - Menggunakan `while` loop untuk menghasilkan bilangan acak
   - Hanya menyimpan bilangan yang kurang dari 0.5
   - Mengabaikan bilangan >= 0.5 dan mencoba lagi
4. **Tampilkan Hasil**: Menggunakan `for` loop untuk menampilkan semua bilangan yang telah dikumpulkan

##  Struktur Kode

```python
from random import random          # Import fungsi random
n = int(input(...))                # Input dari pengguna
bilangan_acak = []                 # List untuk menyimpan hasil
i = 0                              # Counter untuk while loop

while i < n:                       # Loop hingga dapat n bilangan
    angka = random()               # Generate bilangan acak
    if angka < 0.5:                # Filter hanya < 0.5
        bilangan_acak.append(angka)
        i += 1

for j in range(len(bilangan_acak)): # Tampilkan hasil
    print(...)
```

##  Konsep yang Digunakan

- **Import Module**: Menggunakan fungsi `random()` dari library Python
- **Input Runtime**: Nilai `n` ditentukan saat program berjalan
- **While Loop**: Untuk menghasilkan bilangan hingga memenuhi syarat
- **For Loop**: Untuk menampilkan hasil dengan iterasi
- **Conditional Statement**: Memfilter bilangan yang sesuai kriteria
- **List**: Menyimpan koleksi bilangan acak

##  Catatan

- Bilangan yang dihasilkan adalah bilangan desimal acak antara 0.0 dan 0.5
- Setiap kali program dijalankan akan menghasilkan bilangan yang berbeda
- Program akan terus mencoba hingga mendapatkan `n` bilangan yang memenuhi kriteria (< 0.5)

      **##LATIHAN 2.PY**

# Simulasi Mesin ATM

Program simulasi mesin ATM sederhana yang dibuat menggunakan Python. Program ini memungkinkan pengguna untuk melakukan operasi dasar ATM seperti tarik tunai, cek saldo, dan keluar dari sistem.

##  Fitur

- **Tarik Tunai**: Melakukan penarikan uang dari saldo
- **Cek Saldo**: Melihat saldo yang tersedia
- **Format Rupiah**: Menampilkan nilai uang dalam format Rupiah (Rp)
- **Validasi Input**: Memvalidasi input pengguna untuk mencegah error
- **Notifikasi Saldo Habis**: Memberitahu pengguna ketika saldo telah habis

##  Cara Menjalankan

### Langkah-langkah

1. **Clone atau download file program**
   ```bash
   # Pastikan Anda memiliki file atm_simulator.py
   ```

2. **Jalankan program**
   ```bash
   python atm_simulator.py
   ```

3. **Ikuti instruksi di layar**
   - Pilih menu yang diinginkan (1-3)
   - Masukkan jumlah penarikan jika memilih menu Tarik Tunai
   - Program akan terus berjalan hingga Anda memilih menu Keluar

## Penggunaan

### Menu Utama

```
========================================
SELAMAT DATANG DI ATM
========================================
1. Tarik Tunai
2. Cek Saldo
3. Keluar
========================================
```

### 1. Tarik Tunai
- Pilih menu 1
- Masukkan jumlah uang yang ingin ditarik
- Program akan memvalidasi apakah saldo mencukupi
- Saldo akan berkurang sesuai jumlah penarikan

### 2. Cek Saldo
- Pilih menu 2
- Program akan menampilkan saldo terkini

### 3. Keluar
- Pilih menu 3
- Program akan menampilkan saldo akhir dan menutup aplikasi

##  Contoh Penggunaan

```
*** SIMULASI MESIN ATM ***
Saldo awal Anda: Rp 1.000.000

========================================
SELAMAT DATANG DI ATM
========================================
1. Tarik Tunai
2. Cek Saldo
3. Keluar
========================================
Pilih menu (1-3): 1

Saldo tersedia: Rp 1.000.000
Masukkan jumlah penarikan: Rp 250000

----------------------------------------
Transaksi Berhasil!
Jumlah penarikan: Rp 250.000
Sisa saldo: Rp 750.000
----------------------------------------
```

##  Struktur Kode

### Fungsi-fungsi Utama

- **`format_rupiah(angka)`**: Memformat angka menjadi format Rupiah dengan pemisah titik
- **`tampilkan_menu()`**: Menampilkan menu ATM di layar
- **`main()`**: Fungsi utama yang menjalankan logika program


##  Saldo Awal

Saldo awal default adalah **Rp 1.000.000**. Anda dapat mengubahnya dengan memodifikasi variabel `saldo` di dalam fungsi `main()`:

```python
saldo = 1000000  # Ubah nilai ini sesuai kebutuhan
```


**Catatan**: Program ini adalah simulasi sederhana untuk tujuan pembelajaran dan tidak terhubung dengan sistem perbankan nyata.

    **##LATIHAN 2.PY**

