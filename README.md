# Tugas Besar 1 Strategi Algoritma - Team7
## Pemanfaatan Algoritma Greedy dalam Permainan Diamonds

## Kelompok Team7
| No. | Nama                     |   NIM    |
|:---:|:-------------------------|:--------:|
| 1.  | Muhammad Daffansyah Desuandi | 123140127 |
| 2.  | Falih Faiq Fadhlurrahman    | 123140129 |
| 3.  | Khairul Rijal Syauqi    | 123140143 |

## Daftar Isi
1. [Deskripsi Umum](#deskripsi-umum)
2. [Penjelasan Algoritma](#penjelasan-algoritma)
3. [Penggunaan Program](#penggunaan-program)

## Deskripsi Umum
Tugas Besar 1 Strategi Algoritma ini bertujuan untuk mengimplementasikan bot pada permainan _Diamonds_. Permainan _Diamonds_ merupakan permainan sederhana yang memiliki objektif bagi pemain untuk mendapatkan _Diamonds_ sebanyak-banyaknya pada papan permainan.

Bot yang dibuat akan menggunakan algoritma _**Greedy**_ dengan tujuan utama mendapatkan _Diamond_ sebanyak-banyaknya agar dapat memenangkan permainan.

## Penjelasan Algoritma
1. Prioritaskan strategi Greedy by Value-to-Distance Ratio karena pendekatan ini mengoptimalkan jumlah poin yang diperoleh dalam setiap langkah gerakan bot. Bot akan selalu memilih diamond yang memiliki rasio nilai terhadap jarak tertinggi, sehingga setiap langkah memberikan imbal hasil (poin) terbaik. Ini memberikan efisiensi tinggi, terutama dalam pertandingan yang waktunya sangat terbatas.

2. Jika tidak ada diamond yang memiliki rasio nilai-jarak yang menguntungkan secara signifikan, maka bot akan beralih ke pendekatan Greedy by Shortest Distance, yaitu memilih diamond terdekat tanpa memperhatikan nilainya, agar tetap bisa mengumpulkan diamond secara cepat dan memaksimalkan jumlah pengambilan.

3. Dalam situasi di mana tidak ada diamond yang dekat maupun yang memiliki rasio tinggi, maka bot akan menerapkan pendekatan Greedy by Chasing Distant High-Value Diamonds, yaitu mengejar diamond yang sangat jauh namun memiliki poin tinggi (misalnya red diamond), jika secara kalkulasi rasio masih lebih baik dibanding alternatif lain.

4. Jika seluruh opsi diamond memiliki rasio yang rendah atau tidak ada yang layak diambil, maka bot akan menuju red button apabila jaraknya lebih dekat dibandingkan diamond yang tersedia. Ini bertujuan untuk melakukan reset peta agar mendapatkan kemungkinan spawn diamond yang lebih menguntungkan.

5. Ketika inventory bot sudah cukup terisi (misalnya ≥3 diamond), bot akan memprioritaskan untuk kembali ke base. Namun, jika di sepanjang jalur menuju base masih ada diamond yang secara rasio nilai-jarak masih menguntungkan dan inventory belum penuh, bot akan mengambil diamond tersebut terlebih dahulu. Selain itu, jika terdapat teleporter yang dapat mempersingkat total jarak ke base, maka bot akan menggunakan teleporter tersebut sebagai strategi optimalisasi rute.
