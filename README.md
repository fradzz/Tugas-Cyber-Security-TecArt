## Penugasan

**Nama:** I Putu Arvin Danendra Diputra  
**NIM:** 260530911030  
**Kategori CTF:** Web  



## 1. Tools Umum

 A. Pengujian WSL

Dokumentasi pengujian WSL.

![Pengujian WSL](images/Pengujian%201.jpeg)

 B. Software Pendukung

Dokumentasi penginstalan Ubuntu dari Microsoft Store.

![Software Pendukung](images/Software%20Pendukung.jpeg)

 C. Pengujian Python

Membuat script sederhana "test.py" memakai Python 3.

![Pengujian Python](images/Pengujian%20Python.jpeg)



## 2. Dokumentasi Challenge Wajib (Undo)

Step 1


Saya mulai challenge "Undo" di CyLab dan langsung melihat hint yang mengarahkan ke halaman "tr(1) - Linux Manual Page". Saya mencoba menginput "base64 --version" karena saya kira perintah "--version" bisa digunakan untuk melihat versi lama suatu teks / meng-undo teks, namun ternyata salah. Lalu saya mencoba menginput "base64 \b" namun belum berhasil juga. Pada percobaan terakhir menggunakan perintah "base64 -d", dan langkah ini berhasil.

![Undo Step 1 - Part 1](images/Undo%201.jpeg)  
![Undo Step 1 - Part 2](images/Undo%202.jpeg)

Step 2


Selanjutnya saya coba menginput "base64 tr" namun ternyata salah. Akhirnya ada clue yang meminta saya untuk mengetik "rev". Setelah saya coba, ternyata berhasil.

![Undo Step 2](images/Undo%203.jpeg)

Step 3


Selanjutnya saya coba menginput "-s" tapi ternyata salah, lalu sistemnya memberikan hint "tr '_ ' '-'". Awalnya di sini saya bingung agak lama dan mencoba beberapa perintah namun ternyata tetap salah. Akhirnya saya sadar ternyata cluenya adalah jawabannya tapi dibalik, jadi saya mencoba menginput "tr '-' '_'" dan berhasil.

![Undo Step 3](images/Undo%204.jpeg)

Step 4


Selanjutnya karena pertanyaannya masih sama dan cluenya masih mirip-mirip, saya bisa menyelesaikan Step 4 setelah sekali error untuk percobaan melihat hintnya dan menginput "tr '()' '{}'".

![Undo Step 4](images/Undo%205.jpeg)

Step 5


Selanjutnya, karena hintnya diminta apply ROT13, awalnya saya bingung dan mencoba menginput "rot13" namun ternyata salah. Setelahnya muncul hint untuk reverse, dan di sana saya mengikuti hintnya lalu berhasil untuk mendapatkan flag-nya.

![Undo Step 5 - Part 1](images/Undo%205.jpeg)  
![Undo Step 5 - Part 2](images/Undo%206.jpeg)

### Hasil pada Web CyLab
Dibawah ini adalah hasil tampilan setelah berhasil menyelesaikan challenge "Undo" di web CyLab:

![Undo Final 1](images/Undo%20Final%201.jpeg)  
![Undo Final 2](images/Undo%20Final%202.jpeg)



## 3. Dokumentasi Kategori: Web

Step 1


Saya memulai challenge dengan membuka link yang diberikan. Awalnya di sini saya cukup lama stuck mikir harus bagaimana, namun sesuai hint yang diberikan, saya mencoba menggunakan BurpSuite, lalu masuk ke tab Proxy dan mengaktifkan Intercept.

![Web Step 1](images/Web%201.jpeg)

Step 2


Saya mencoba untuk membuka browser melalui menu Intercept nya dan memasukkan URL yang diberikan. Karena tidak ada hint bagaimana cara mengisi datanya, jadi saya coba isi acak saja sekaligus mematikan fungsi Intercept di halaman registrasinya karena belum ada hasil.

![Web Step 2](images/Web%202.jpeg)  
![Web Step 3](images/Web%203.jpeg)

Step 3


Nah, sampai di halaman OTP setelah registrasi, saya mencoba menghidupkan kembali Intercept nya. Sesuai hint ke 2 di mana diminta untuk mengacak kode karena servernya tidak bisa menangani malfungsi server.

![Web Step 3](images/Web%204.jpeg)

Step 4


Setelah itu saya coba menekan tombol Forward dan muncullah halaman baru dengan flag di dalamnya.

### Hasil pada Web CyLab
Dibawah ini adalah hasil tampilan setelah berhasil menyelesaikan challenge kategori Web pada web CyLab:

![Web Final 1](images/Web%20Final%201.jpeg)  
![Web Final 2](images/Web%20Final%202.jpeg)



## 4. Referensi
* CyLab Security Academy - Challenge "Undo" & "IntroToBurp"
* Linux Manual Page (`tr(1)`)
* PortSwigger Burpsuite
