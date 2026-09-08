NIM : 260530911030
Nama : I Putu Arvin Danendra Diputra
Divisi : Cyber Security


Penugasan

**Nama:** I Putu Arvin Danendra Diputra  
**NIM:** 260530911030  
**Kategori CTF:** Web  

---

## 1. Tools Umum

 A. Pengujian WSL
Pengujian dilakukan untuk memastikan lingkungan WSL (Linux) berjalan dengan baik.
![Pengujian WSL](Pengujian%201.jpeg)

 B. Software Pendukung
Pemasangan software dan dependensi pendukung lingkungan pengerjaan.
![Software Pendukung](Software%20Pendukung.jpeg)

 C. Pengujian Python
Membuat dan menjalankan script sederhana "test.py" menggunakan Python 3.
![Pengujian Python](Pengujian%20Python.jpeg)

---

## 2. Dokumentasi Challenge Wajib (Undo)

Step 1
Saya memulai challenge "Undo" di CyLab dan langsung melihat hint yang mengarahkan ke halaman "tr(1) - Linux Manual Page". Saya mencoba menginput "base64 --version" karena saya kira perintah "--version" bisa digunakan untuk melihat versi lama / meng-undo teks, namun ternyata salah. Lalu saya mencoba menginput "base64 \b" namun belum berhasil juga. Pada percobaan terakhir menggunakan perintah "base64 -d", langkah ini berhasil.

![Undo Step 1 - Part 1](Undo%201.jpeg)  
![Undo Step 1 - Part 2](Undo%202.jpeg)

Step 2
Selanjutnya saya mencoba menginput "base64 tr" namun ternyata salah. Akhirnya ada clue yang meminta saya untuk mengetik "rev". Setelah saya coba, ternyata berhasil.

![Undo Step 2](Undo%203.jpeg)

Step 3
Selanjutnya saya mencoba menginput "-s" tapi ternyata salah, lalu diberikan hint "tr '_ ' '-'". Awalnya di sini saya bingung agak lama dan mencoba beberapa perintah namun ternyata tetap salah. Akhirnya saya sadar ternyata clue-nya adalah jawabannya, jadi saya mencoba menginput "tr '-' '_'" dan berhasil.

![Undo Step 3](Undo%204.jpeg)

Step 4
Selanjutnya karena pertanyaannya masih sama dan clue-nya masih mirip-mirip, saya bisa menyelesaikan Step 4 setelah sekali error untuk percobaan melihat hint-nya dan menginput "tr '()' '{}'".

![Undo Step 4](Undo%205.jpeg)

Step 5
Selanjutnya, karena hint-nya diminta apply ROT13, awalnya saya bingung dan mencoba menginput "rot13" namun ternyata salah. Setelahnya muncul hint untuk reverse, dan di sana saya mengikuti hint-nya lalu berhasil untuk mendapatkan flag-nya.

![Undo Step 5 - Part 1](Undo%205.jpeg)  
![Undo Step 5 - Part 2](Undo%206.jpeg)

### Hasil pada Web CyLab
Dibawah ini adalah hasil tampilan setelah berhasil menyelesaikan challenge "Undo" di web CyLab:

![Undo Final 1](Undo%20Final%201.jpeg)  
![Undo Final 2](Undo%20Final%202.jpeg)

---

## 3. Dokumentasi Kategori: Web

Step 1
Saya memulai challenge dengan membuka link yang diberikan. Awalnya di sini saya cukup lama stuck harus bagaimana, namun sesuai hint yang diberikan, saya mencoba menggunakan BurpSuite, lalu masuk ke tab Proxy dan mengaktifkan Intercept.

![Web Step 1](Web%201.jpeg)

Step 2
Saya mencoba untuk membuka browser melalui menu Intercept-nya dan memasukkan URL yang diberikan. Karena tidak ada hint bagaimana cara mengisi datanya, jadi saya coba isi acak saja sekaligus mematikkan fungsi Intercept di halaman registrasinya karena belum ada hasil.

![Web Step 2](Web%202.jpeg)  
![Web Step 3](Web%203.jpeg)

Step 3
Nah, sampai di halaman OTP setelah registrasi, saya mencoba menghidupkan kembali Intercept-nya. Sesuai hint ke-2 di mana diminta untuk mengacak kode karena servernya tidak bisa menangani malfungsi server.

![Web Step 3](Web%204.jpeg)

Step 4
Setelah itu saya coba Forward dan muncullah halaman baru dengan flag di dalamnya.

### Hasil pada Web CyLab
Dibawah ini adalah hasil tampilan setelah berhasil menyelesaikan challenge kategori Web pada web CyLab:

![Web Final 1](Web%20Final%201.jpeg)  
![Web Final 2](Web%20Final%202.jpeg)

---

## 4. Referensi
* CyLab Security Academy - Challenge "Undo" & "Web"
* Linux Manual Page (`tr(1)`)
* PortSwigger Burpsuite
