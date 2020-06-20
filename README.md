# NodeJsDotDev

## Perkenalan Node.js

Daftar Isi
* [ Jumlah pustaka yang sangat banyak ](#)
* [ Contoh Aplikasi Node.js](#)
* [ Para rangkakerja dan alat-alat](#)

Node.js adalah sebuah sumber-terbuka dan lingkungan waktulari JavaScript yang lintas-platform

Node.js melarikan mesin JavaScript V8, yakni inti dari Google Chrome, di luar browser. Hal ini memungkinkan kinerja Node.js menjadi sangat bagus dan memuaskan.

Sebuah aplikasi Node.js berlari di dalam sebuah proses tunggal, tanpa menciptakan sebuah thread yang baru untuk setiap permintaan. Node.js menyediakan serangkaian primitif I/O yang bersifat asinkronis di dalam pustaka standarnya yang mencegah kode JavaScript menghambat dan pada umumnya pustaka-pustaka di dalam Node.js ditulis menggunakan paradigma nirhambat, yang membuat prilaku menghambat adalah sebuat pengecualian ketimbang sebuah hal yang wajar.

Ketika Node.js melakukan sebuah operasi I/O, seperti membaca dari jaringan, mengakses sebuah database atau sistem berkas, alih-alih menghambat thread dan membuang siklus CPU menunggu, Node.js akan melanjutkan operasi-operasi ketika jawaban kembali.

Hal ini memungkinkan Node.js menangani ribuan koneksi secara bersamaan dengan satu server tanpa menimbulkan beban untuk mengelola thread yang bersifat konkuren, yang mungkin saja adalah sebuah sumber bug-bug yang signifikan.

Node.js mempunyai sebuah keunggulan yang khas karena jutaan pengembang frontend yang menulis JavaScript untuk peramban adalah dapat menulis kode di sisi server selain di sisi client tanpa keharusan untuk belajar bahasa pemrograman yang sama sekali berbeda sekarang.

