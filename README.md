# lapres Jarkom-Modul-1-A12-2023
- Shaula Aljauhara Riyadi 5025201265
-
## soal
1. User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.

- Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut?
- Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut?
- Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
- Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
### jawaban
mula-mula buka file .pcapng yang telah disediakan pada modul soal

![Ss Soal1](images/Screenshot%202023-09-21%20102039.png)

kemudian filter tabel dengan menggunakan searchbar dengan bendera biru disampingnya dengan menuliskan "ftp" sehingga tabel wireshark akan menampilkan log dengan protocol FTP saja 

![Ss Soal1.1](images/Screenshot%202023-09-21%20103352.png)

untuk menyelesaikan soal a dan b,cari log yang bertuliskan request: STOR yang mana command STOR adalah command untuk mengunggah file pada protokol FTP

![Ss Soal1.2](images/Screenshot%202023-09-21%20104215.png)

lalu tekan log tersebut hingga muncul header yang berisi informasi dari  log tersebut

![Ss Soal1.3](images/Screenshot%202023-09-21%20104746.png)

lalu cari Sequence number(raw) dan Acknowledge number(raw) dari log STOR tersebut 

![Ss Soal1.4](images/Screenshot%202023-09-21%20104746.png)

pada gambar diatas telah terlihat berapa sequence number(raw) dan aknowledge number(raw) dari log STOR yang terekam.
untuk soal c dan d lakukan hal yang sama seperti yang dilakukan pada log STOR untuk mencari sequence number(raw) dan acknowledge number(raw) tapi lakukan pada log persis dibawah log STOR yang mana log tersebut merupakan log response dari request STOR pada log sebelumnya 

![Ss Soal1.5](images/Screenshot%202023-09-21%20105704.png)

![Ss Soal1.6](images/Screenshot%202023-09-21%20110334.png)

pada gambar terakhir terlihat Sequence number(raw) dan Acknowledge number(raw) dari log response dari request STOR  tersebut.Setelah mengetahui jawaban-jawaban yang dicari,kirim jawab tersebut ke netcat yang telah disediakan dengan bash(nc/ncat) 
```bash
ncat sekian.sekian sekian.sekian
```
lalu setelah submit jawaban jika benar akan mendapatkan flag dan flag tersebut dapat disubmit pada platform pratikum yang digunakan.
kendala yang umum terjadi ketika mengerjakan soal ini adalah kurang teliti ketika mencari sequence dan acknowledge number dari log STOR yang ditanyakan.jadi ketika soal menanyakan sequence number(raw) dan acknowledge number(raw) dari log tersebut tapi menjawab soal dengan sequence number dan acknowledge number yang biasa tanpa ada tanda raw pada informasi tersebut.

2. Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!
### jawaban
buka file .pcapng soal yang disediakan.
![Ss Soal2](images/Screenshot%202023-09-22%20102236.png)
kemudian filter tabel dengan mengetik "http" sehingga tabel hanya menampilkan log dengan protocol http.
![Ss Soal2](images/Screenshot%202023-09-22%20102356.png)
cari log dengan informasi "HTTP/sekian.sekian sekian" pada tabel tersebut untuk mencari nama server yang digunakan.lalu tekan header dari log tersebut untuk mencari untuk mengetahui server yang digunakan.
![Ss Soal2](images/Screenshot%202023-09-22%20102420.png)
dari gambar diatas bisa diketahui bahwa server yang digunakan pada portal praktikum jaringan komputer adalah server dari gunicorn.
Setelah mengetahui jawaban-jawaban yang dicari,kirim jawab tersebut ke netcat yang telah disediakan dengan bash(nc/ncat) 
```bash
ncat sekian.sekian sekian.sekian
```
lalu setelah submit jawaban jika benar akan mendapatkan flag dan flag tersebut dapat disubmit pada platform pratikum yang digunakan.
kendala yang umum terjadi pada saat mengerjakan soal ini adalah kebingungan mencari pada log mana yang memiliki informasi server yang sedang digunakan dari banyaknya log yang terekam pada file tersebut.

3. Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:
Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?
Protokol layer transport apa yang digunakan?
### jawaban
