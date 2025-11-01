**Nama : Ahmad Ridhwan Ilham (312510222)**

**Mata Kuliah : Pengantar Pemrograman**

mohon maaf pak latihan 2 dan 3 tertukar dan file nya tidak bisa di rename


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

    **##LATIHAN 3.PY**

# Kalkulator Keuntungan Usaha

Program Python untuk menghitung dan menganalisis keuntungan usaha selama 8 bulan pertama dengan fluktuasi persentase laba yang berbeda-beda setiap periode.

##  Cara Menjalankan

### Langkah-langkah

1. **Simpan file program**
   ```bash
   # Simpan kode sebagai profit_calculator.py
   ```

2. **Jalankan program**
   ```bash
   python profit_calculator.py
   ```

3. **Lihat hasil perhitungan**
   Program akan otomatis menampilkan:
   - Rincian laba per bulan
   - Total keuntungan
   - Modal akhir
   - Persentase keuntungan

## Output Program

### Contoh Output

```
*** KALKULATOR KEUNTUNGAN USAHA 8 BULAN ***

============================================================
PERHITUNGAN KEUNTUNGAN USAHA
============================================================
Modal Awal: Rp 100.000.000
============================================================

RINCIAN PER BULAN:
------------------------------------------------------------
Bulan    Laba %     Laba Bulan          Total Modal         
------------------------------------------------------------
1        0          Rp 0                Rp 100.000.000      
         Belum ada laba

2        0          Rp 0                Rp 100.000.000      
         Belum ada laba

3        1          Rp 1.000.000        Rp 101.000.000      
         Laba 1%

4        1          Rp 1.000.000        Rp 102.000.000      
         Laba 1%

5        5          Rp 5.000.000        Rp 107.000.000      
         Laba meningkat menjadi 5%

6        5          Rp 5.000.000        Rp 112.000.000      
         Laba meningkat menjadi 5%

7        5          Rp 5.000.000        Rp 117.000.000      
         Laba meningkat menjadi 5%

8        3          Rp 3.000.000        Rp 120.000.000      
         Laba turun menjadi 3%

============================================================
RINGKASAN KEUNTUNGAN
============================================================
Modal Awal           : Rp 100.000.000
Total Keuntungan     : Rp 20.000.000
Total Modal + Laba   : Rp 120.000.000
Persentase Keuntungan: 20.00%
============================================================
```

##  Struktur Kode

### Fungsi Utama

#### `format_rupiah(angka)`
Memformat angka menjadi format mata uang Rupiah dengan pemisah titik.

**Parameter:**
- `angka` (int/float): Nilai yang akan diformat

**Return:**
- String dengan format Rupiah (contoh: "Rp 1.000.000")

#### `hitung_keuntungan_usaha()`
Fungsi utama yang melakukan perhitungan keuntungan usaha selama 8 bulan.

**Return:**
- `total_keuntungan` (float): Total keuntungan selama 8 bulan
- `total_modal` (float): Modal akhir (modal awal + keuntungan)

### Logika Perhitungan

```python
# Persentase laba dihitung dari MODAL AWAL (Rp 100.000.000)
laba_bulan = modal_awal * (persentase_laba / 100)

# Total keuntungan = akumulasi laba dari bulan 1-8
# Total modal = modal awal + total keuntungan
```

##  Analisis Keuntungan

### Breakdown Keuntungan per Periode

| Periode | Persentase Laba | Durasi | Laba per Bulan | Total Laba Periode |
|---------|-----------------|--------|----------------|-------------------|
| Bulan 1-2 | 0% | 2 bulan | Rp 0 | Rp 0 |
| Bulan 3-4 | 1% | 2 bulan | Rp 1.000.000 | Rp 2.000.000 |
| Bulan 5-7 | 5% | 3 bulan | Rp 5.000.000 | Rp 15.000.000 |
| Bulan 8 | 3% | 1 bulan | Rp 3.000.000 | Rp 3.000.000 |
| **TOTAL** | - | **8 bulan** | - | **Rp 20.000.000** |

### Key Insights

-  **Total Keuntungan**: Rp 20.000.000 (20% dari modal awal)
-  **Rata-rata Laba per Bulan**: Rp 2.500.000
-  **Periode Paling Menguntungkan**: Bulan 5-7 (kontribusi 75% dari total laba)
-  **Periode Break-even**: Bulan 1-2 (belum ada laba)

##  Kustomisasi

### Mengubah Modal Awal

Edit variabel `modal_awal` di dalam fungsi:

```python
modal_awal = 100_000_000  # Ubah sesuai kebutuhan
```

### Mengubah Persentase Laba

Modifikasi kondisi di dalam loop `for bulan in range(1, 9)`:

```python
elif bulan == 3 or bulan == 4:
    persentase_laba = 1  # Ubah persentase di sini
```

### Menambah Durasi Perhitungan

Ubah range loop untuk menghitung lebih dari 8 bulan:

```python
for bulan in range(1, 13):  # Untuk 12 bulan
```

##  Catatan Penting

- Persentase laba **selalu dihitung dari modal awal** (Rp 100.000.000), bukan dari modal berjalan
- Program ini adalah simulasi dan tidak memperhitungkan:
  - Biaya operasional
  - Pajak
  - Inflasi
  - Risiko usaha lainnya
- Cocok untuk pembelajaran dan perencanaan bisnis sederhana


##  Kontribusi

Silakan fork dan submit pull request untuk perbaikan atau penambahan fitur!

---
