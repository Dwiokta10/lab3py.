# Dwi Okta Ramadhani
# TI.24.A.1

# Program 1 
Import library random untuk menghasilkan angka acak from random import random
# Deskripsi Program
Program ini dibuat menggunakan bahasa python dengan fitur:
1. Inisialisasi:
- Import library random untuk menghasilkan bilangan acak.
- Menerima input N dari pengguna (jumlah bilangan acak yang harus kurang dari 0.5).
2. Inisialisasi Variabel:
- Buat variabel count untuk menghitung bilangan acak yang valid (kurang dari 0.5). Awalnya, count = 0.
3. Pengulangan
- Gunakan loop while yang berjalan hingga count mencapai N.
- Dalam loop, gunakan random() untuk menghasilkan bilangan acak.
# Kode Program
```python
from random import random

# Meminta input jumlah bilangan acak yang lebih kecil dari 0.5
n = int(input("Masukkan nilai N: "))
count = 0

# Loop untuk menghasilkan dan menampilkan bilangan acak yang kurang dari 0.5
while count < n:
    num = random()
    if num < 0.5:
        count += 1
        print(f"data ke-{count} => {num}")

print("Selesai")

```
# Output Program
![Flowchart](https://github.com/Dwiokta10/lab3py./blob/main/outputke1.png)
# Cara Kerja Program
Input Pengguna: Pengguna diminta untuk memasukkan sebuah angka N yang menunjukkan jumlah bilangan acak kurang dari 0.5 yang harus ditampilkan.
Pengulangan dan Logika:
- Loop berjalan tanpa batas awalnya, tetapi berhenti secara kondisional setelah count mencapai nilai N.
- Setiap bilangan acak dihasilkan menggunakan fungsi random(), yang memberikan nilai float antara 0.0 dan 1.0.
- Jika bilangan yang dihasilkan kurang dari 0.5, nilai tersebut dihitung dalam count, ditampilkan, dan diberi nomor urut.
Keluar dari Loop: Ketika count mencapai nilai N, loop berhenti, dan program mencetak pesan "Selesai".

# Program 2
Menghitung keuntungan pengusaha investasi
# Deskripsi Program
Program ini dibuat menggunakan bahasa python dengan fitur:
1. Inisialisasi modal awal
2. Inisialisasi total laba: Variabel total_laba disiapkan untuk menjumlahkan semua laba bulanan
3. Looping per bulan
- Menggunakan perulangan for bulan in range
4. Menampilkan laba bulanan: Setiap laba bulanan ditampilkan menggunakan fungsi print().
5. Mengakumulasi total laba: Laba bulanan dijumlahkan ke dalam variabel total_laba.
# Kode Program
```python
print("Laba per bulan:")

# Menghitung laba per bulan
for bulan in range(1, 9):
    if bulan == 1 or bulan == 2:
        laba = 0  # Bulan pertama dan kedua belum ada laba
    elif bulan == 3 or bulan == 4:
        laba = modal_awal * 0.01  # Bulan ketiga dan keempat laba 1%
    elif bulan == 5 or bulan == 6:
        laba = modal_awal * 0.05  # Bulan kelima dan keenam laba 5%
    elif bulan == 7:
        laba = modal_awal * 0.05  # Bulan ketujuh laba tetap 5%
    elif bulan == 8:
        laba = modal_awal * 0.03  # Bulan kedelapan laba turun menjadi 3%
    
    print(f"Laba bulan ke-{bulan} sebesar: {laba}")
    total_laba += laba  # Menambahkan laba bulanan ke total laba

print(f"Total laba adalah: {total_laba}")
```
# Output Program
![Flowchart](https://github.com/Dwiokta10/lab3py./blob/main/output2.png)

# Cara Kerja Program
1. Input dan inisialisasi:
- Nilai modal awal Rp100.000.000 diatur dalam variabel modal_awal.
- Variabel total_laba disiapkan untuk menghitung akumulasi laba.
2. Proses perulangan:
- Setiap bulan dihitung laba sesuai dengan ketentuan.
- Untuk bulan pertama dan kedua, laba 0.
- Mulai bulan ketiga, laba dihitung dengan persentase yang sesuai.
- Laba ditambahkan ke total_laba setiap iterasi.
3. Output:
- Laba per bulan ditampilkan langsung.
- Setelah perulangan selesai, total laba yang dikumpulkan selama 8 bulan dicetak.

# Program 3
Membuat ATM sederhana 
# Deskripsi Program
Program ini dibuat menggunakan bahasa python dengan fitur:
while True,if,int(input, except ValueError,break,else
# Kode Program
```python
def atm():
    saldo = 1000000  # Initial balance
    while True:
        print(f"Saldo saat ini: Rp {saldo}")
        print("1. Tarik Uang")
        print("2. Keluar")
        
        pilihan = input("Pilih menu (1/2): ")
        
        if pilihan == '1':
            try:
                jumlah_penarikan = int(input("Masukkan jumlah penarikan: "))
                if jumlah_penarikan <= saldo:
                    saldo -= jumlah_penarikan
                    print("Penarikan berhasil!")
                else:
                    print("Saldo tidak mencukupi.")
            except ValueError:
                print("Input tidak valid. Masukkan angka.")
        elif pilihan == '2':
            print("Terima kasih telah menggunakan ATM!")
            break
        else:
            print("Pilihan tidak valid. Coba lagi.")
        print()

# Run the ATM function
atm()
```
# Output Program
![Flowchart](
# Cara Kerja Program
1. Inisialisasi Saldo:
- Program dimulai dengan saldo awal sebesar Rp 1.000.000.
2. Tampilan Menu:
- Program terus menampilkan saldo dan dua pilihan menu (Tarik Uang atau Keluar) selama loop berjalan.
3. Pilihan Menu:
- Jika pengguna memilih 1, mereka diminta untuk memasukkan jumlah penarikan:
         - Jika jumlah penarikan lebih kecil atau sama 
           dengan saldo, saldo dikurangi dengan jumlah 
           tersebut, dan transaksi berhasil.
         -Jika jumlah penarikan lebih besar dari saldo, 
           pengguna mendapatkan pesan bahwa saldo tidak 
           mencukupi.
- Jika pengguna memilih 2, program keluar dari loop dan mencetak pesan penutup.
- Jika input tidak valid (bukan angka atau pilihan lain selain 1 dan 2), program mencetak pesan error.
4. Cek Kesalahan Input:
- Program menangani kesalahan input angka menggunakan try-except untuk menghindari error akibat masukan tidak valid.
5. Berhenti:
- Program berhenti jika pengguna memilih menu "Keluar". dengan menampilkan pesan "Terima kasih telah menggunakan ATM"
