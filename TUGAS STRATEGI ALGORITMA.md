## Strategi Algoritma

## Tugas pada pertemuan 2 ini anda diminta untuk menuliskan kode program untuk menghitung rata-rata dari beberapa bilangan kemudian 
lakukan pengukuran dengan menghitung waktu yang dilakukan untuk melakukan perhitungan rata-rata tersebut. Waktu yang disarankan menggunakan 
satuan mikrosecond atau milisecond.

```cpp
import time 
print ("\nProgram Mencari Nilai Rata-Rata dan Terbesar")
print ("\n============================================")
n = int(input("\nBanyak Data: "))

print()
data = []
jumlah = 0
start_time = time.time()
for i in range(n):
    temp = int(input("Masukkan data ke-%d: "% (i+1)))
    data.append(temp)
    nilaiTerbesar = data[0]
    nilaiTerkecil = data[0]
    if (data[i] > nilaiTerbesar):
        nilaiTerbesar=data[i]
    elif (data[i] < nilaiTerbesar):
        nilaiTerkecil = data[i]
    jumlah += data[i]
    rata = jumlah / n
end_time = time.time()

print("\n============================================")
print("\nNilai Terbesar : ", nilaiTerbesar)
print("Nilai Terkecil : ", nilaiTerkecil)
print("Nilai Rata-rata :",rata)

waktu_mikro = (end_time - start_time) * 1000000
print("Waktu yang diperlukan:", waktu_mikro, "mikrosekon")
```
