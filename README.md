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

## Deskripsi Umum
Tugas Besar 1 Strategi Algoritma ini bertujuan untuk mengimplementasikan bot pada permainan _Diamonds_. Permainan _Diamonds_ merupakan permainan sederhana yang memiliki objektif bagi pemain untuk mendapatkan _Diamonds_ sebanyak-banyaknya pada papan permainan.

Bot yang dibuat akan menggunakan algoritma _**Greedy**_ dengan tujuan utama mendapatkan _Diamond_ sebanyak-banyaknya agar dapat memenangkan permainan.

## Penjelasan Algoritma
Program ini menerapkan algoritma greedy by distance dalam permainan Diamonds. Pendekatan ini bertujuan untuk mengumpulkan semua diamond dengan cara yang efisien berdasarkan jarak terpendek.
Langkah-langkah utama algoritma:

- Bot memulai dari posisi awal yang telah ditentukan.
- Pada setiap iterasi, bot akan mencari diamond terdekat berdasarkan jarak Euclidean atau Manhattan.
- Bot bergerak menuju diamond tersebut.
- Diamond diambil, kemudian proses diulang sampai batas waktu habis

Algoritma ini memprioritaskan solusi lokal optimal (jarak terdekat) yang diharapkan menghasilkan hasil mendekati solusi optimal secara keseluruhan.

## Requirement Program dan Instalasi Tertentu
Untuk dapat menjalankan game Diamonds dan mengembangkan bot, berikut adalah kebutuhan perangkat lunak yang harus dipasang:
Game Engine:
- Node.js
- Docker Desktop
- Yarn (dapat dipasang via npm): npm install --global yarn

Bot:
- Python

## Command atau Langkah-langkah untuk Compile atau Build Program Menjalankan Game Engine

- Download source code game engine dan extract.
- Masuk ke direktori hasil ekstraksi: yarn
- Setup environment variable:
	Windows: ./scripts/copy-env.bat
	Linux/macOS: chmod +x ./scripts/copy-env.sh
		     ./scripts/copy-env.sh
- Setup database:
	Jalankan Docker Desktop
	Jalankan: docker compose up -d database
- Setup database:
	Windows: ./scripts/setup-db-prisma.bat
	Linux/macOS: chmod +x ./scripts/setup-db-prisma.sh
		     ./scripts/setup-db-prisma.sh
- Build dan jalankan:
  npm run build
  npm run start

- Buka http://localhost:8082/ di browser untuk melihat tampilan frontend.

Catatan: Proses setup (step 1–6) hanya perlu dilakukan satu kali. Selanjutnya cukup jalankan npm run start dengan Docker aktif.
