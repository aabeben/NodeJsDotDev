# NodeJsDotDev

## Perkenalan Node.js

Daftar Isi
* [ Jumlah pustaka yang sangat banyak ](#jumlah-pustaka-yang-sangat-banyak)
* [ Contoh Aplikasi Node.js](#contoh-aplikasi-nodejs)
* [ Para rangkakerja dan alat-alat](#)

Node.js adalah sebuah sumber-terbuka dan lingkungan waktulari JavaScript yang lintas-platform

Node.js melarikan mesin JavaScript V8, yakni inti dari Google Chrome, di luar browser. Hal ini memungkinkan kinerja Node.js menjadi sangat bagus dan memuaskan.

Sebuah aplikasi Node.js berlari di dalam sebuah proses tunggal, tanpa menciptakan sebuah thread yang baru untuk setiap permintaan. Node.js menyediakan serangkaian primitif I/O yang bersifat asinkronis di dalam pustaka standarnya yang mencegah kode JavaScript menghambat dan pada umumnya pustaka-pustaka di dalam Node.js ditulis menggunakan paradigma nirhambat, yang membuat prilaku menghambat adalah sebuat pengecualian ketimbang sebuah hal yang wajar.

Ketika Node.js melakukan sebuah operasi I/O, seperti membaca dari jaringan, mengakses sebuah database atau sistem berkas, alih-alih menghambat thread dan membuang siklus CPU menunggu, Node.js akan melanjutkan operasi-operasi ketika jawaban kembali.

Hal ini memungkinkan Node.js menangani ribuan koneksi secara bersamaan dengan satu server tanpa menimbulkan beban untuk mengelola thread yang bersifat konkuren, yang mungkin saja adalah sebuah sumber bug-bug yang signifikan.

Node.js mempunyai sebuah keunggulan yang khas karena jutaan pengembang frontend yang menulis JavaScript untuk peramban adalah dapat menulis kode di sisi server selain di sisi client tanpa keharusan untuk belajar bahasa pemrograman yang sama sekali berbeda sekarang.

## Jumlah Pustaka Yang Sangat Banyak

npm dengan struktur yang sederhana telah membantu membiakkan ekosistem Node.js, dan sekarang registri npm menaungi lebih dari 1.000.000 paket sumber-terbuka yang dapat anda gunakan secara gratis.

## Contoh Aplikasi Node.js

Contoh lazim Hello World versi Node.js ialah sebuah server jejaring:
```javascript
const hostname = '127.0.0.1'
const port = process.env.PORT

const server = http.createServer((req, res) => {
  res.statusCode = 200
  res.setHeader('Content-Type', 'text/plain')
  res.end('Hello World!\n')
})

server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`)
})
``` 
Kode ini pertama kali menyisipkan [module **http**](https://nodejs.org/api/http.html) Node.js.

Node.js mempunyai sebuah pustaka standar yang luar biasa, termasuk dukungan kelas satu untuk jaringan.

Metode **`creatServer()`** **`http`** menciptakan sebuah server HTTP dan kembali berserta hasilnya.

Server disetel untuk mendengarkan pada port dan nama host tertentu. Ketika server telah siap, fungsi panggil-lagi dipanggil, dalam hal ini memberitahukan kita bahwa server sedang berlari.

Kapanpun sebuah permintaan diterima, [**`event request`**](https://nodejs.org/api/http.html#http_event_request) dipanggil, sedang menyediakan dua buah objek: sebuah permintaan (sebuah objek [**`http.IncomingMessage`**](https://nodejs.org/api/http.html#http_class_http_incomingmessage)) dan sebuah jawaban (sebuah objek [**`http.ServerResponse`**](https://nodejs.org/api/http.html#http_class_http_serverresponse)).

Dua objek itu adalah hal mendasar untuk menangani panggilan HTTP.

Yang pertama menyediakan rincian permintaan. Pada contoh sederhana ini, tidak digunakan, tetapi anda dapat mengakses kepala-kepala permintaan dan data permintaan.

Yang kedua digunakan untuk mengembalikan data ke si pemanggil.

Pada kasus ini dengan:
```javascript
res.statusCode = 200
```
Kita menyetel properti statusCode ke nilai 200, untuk mengindikasikan sebuah jawaban yang sukses.

Kita menyetel kepala Content-Type:
```javascript
res.setHeader('Content-Type', 'plain/text')
```
dan kita menutup jawaban, menambahkan isi sebagai sebuah argumen ke ``end()``:
```javascript
res.end('Hello World\n')
```