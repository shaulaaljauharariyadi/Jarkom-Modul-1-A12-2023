# lapres Jarkom-Modul-1-A12-2023
- Shaula Aljauhara Riyadi 5025201265
- Lihardo Marson Purba 5025211238
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

## soal

2. Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

### jawaban

buka file .pcapng soal yang disediakan.

![Ss Soal2](images/Screenshot%202023-09-22%20102236.png)

kemudian filter tabel dengan mengetik "http" sehingga tabel hanya menampilkan log dengan protocol http.

![Ss Soal2.1](images/Screenshot%202023-09-22%20102356.png)

cari log dengan informasi "HTTP/sekian.sekian sekian" pada tabel tersebut untuk mencari nama server yang digunakan.lalu tekan header dari log tersebut untuk mencari untuk mengetahui server yang digunakan.

![Ss Soal2.2](images/Screenshot%202023-09-22%20102420.png)

dari gambar diatas bisa diketahui bahwa server yang digunakan pada portal praktikum jaringan komputer adalah server dari gunicorn.
Setelah mengetahui jawaban-jawaban yang dicari,kirim jawab tersebut ke netcat yang telah disediakan dengan bash(nc/ncat)

```bash
ncat sekian.sekian sekian.sekian
```

lalu setelah submit jawaban jika benar akan mendapatkan flag dan flag tersebut dapat disubmit pada platform pratikum yang digunakan.

kendala yang umum terjadi pada saat mengerjakan soal ini adalah kebingungan mencari pada log mana yang memiliki informasi server yang sedang digunakan dari banyaknya log yang terekam pada file tersebut.

## soal 

3. Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:
- Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?
- Protokol layer transport apa yang digunakan?

### jawaban
buka file .pcapng dari soal terkait 

![Ss Soal2](images/Screenshot%202023-09-22%20160659.png)

lalu filter dengan mengetik "udp.port==3702" karena soal meminta berapa packet yang ditangkap oleh port 3702.

![Ss Soal2](images/Screenshot%202023-09-22%20160714.png)

lalu hitung berapa banyak paket dengan destinasi "239.255.255.250" pada tabel itu.Setelah dihitung ada 21 paket yang dikirim
menuju destinasi ip address tersebut.lalu untuk protokol layer transport yang digunakan,seperti yang tertulis pada filter yang telah diketik yaitu "'udp'.port==3702",protokol layer transport yang digunakan yaitu menggunakan UDP atau User Diagram Protokol.

Setelah mengetahui jawaban-jawaban yang dicari,kirim jawab tersebut ke netcat yang telah disediakan dengan bash(nc/ncat)

```bash
ncat sekian.sekian sekian.sekian
```

lalu setelah submit jawaban jika benar akan mendapatkan flag dan flag tersebut dapat disubmit pada platform pratikum yang digunakan.

kendala yang umum terjadi pada saat mengerjakan soal ini adalah kebingungan mencari pada log mana yang memiliki informasi server yang sedang digunakan dari banyaknya log yang terekam pada file tersebut.


## soal

4. Berapa nilai checksum yang didapat dari header pada paket nomor 130?

### jawaban
buka file .pcapng soal terkait. 

![Ss Soal4](images/Screenshot%202023-09-22%20162435.png)

lalu scroll kebawah hingga menemukan log no 130.

![Ss Soal4.1](images/Screenshot%202023-09-22%20164939.png)

lalu tekan log tersebut untuk mengakses header dari log tersebut dan cari checksum dari log tersebut,biasanya berada di bagian "User diagram protocol".

![Ss Soal2](images/Screenshot%202023-09-22%20164830.png)

terlihat pada gambar diatas,terlihat informasi checksum yang diminta yaitu 0x18e5.

Setelah mengetahui jawaban-jawaban yang dicari,kirim jawab tersebut ke netcat yang telah disediakan dengan bash(nc/ncat)

```bash
ncat sekian.sekian sekian.sekian
```

lalu setelah submit jawaban jika benar akan mendapatkan flag dan flag tersebut dapat disubmit pada platform pratikum yang digunakan.

kendala yang umum terjadi pada saat mengerjakan soal ini adalah sedikit kebingungan mencari pada header bagian mana yang terdapat informasi terkait checksum tersebut sehingga harus melakukan sedikit konfigurasi settingan untuk dapat menemukan checksum yang dicari.

Untuk sisa soal kemungkinan telah dikerjakan oleh teman satu kelompok yang sampe sekarang belum melakukan kontak.

## soal 7
Berapa jumlah packet yang menuju IP 184.87.193.88?

## jawaban soal 7
- buka file .pcapng soal terkait.

![Ss Soal4](images/Screenshot%202023-09-22%20212848.png)

- kemudian masukkan filter dibawah
  
```bash
ip.dst==184.87.193.88
```

- berikut tampilan setelah paket difilter
- 
![Ss Soal4](images/Screenshot%202023-09-22%20213051.png)

## soal 8

Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)!

## jawaban soal 8

- buka file .pcapng soal terkait.

![Ss Soal4](images/Screenshot%202023-09-22%20212848.png)

- kemudian masukkan filter dibawah
  
```bash
tcp.dstport == 80 || udp.dstport == 80
```

- berikut hasil filter :
![Ss Soal4](images/Screenshot%202023-09-22%20214550.png)

- Kendala dalam pengerjaan soal ini adalah terkadang wireshark bisa error dalam menampilkan data sesuai filter, sehingga terkadang paket filteran tidak tampak sama sekali meskipun syntax filter benar.
  
## soal 9

Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!

## jawaban soal 9

- buka file .pcapng soal terkait.

![Ss Soal4](images/Screenshot%202023-09-22%20212848.png)

- kemudian masukkan filter dibawah
  
```bash
ip.src == 10.51.40.1 && ip.dst != 10.39.55.34
```

- kendala dalam pengerjaan soal ini sama seperti soal 8 dimana wireshark bisa error dalam menampilkan filter dan perlu direstart.

## soal 10

Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet, format [username]:[password]!

- buka file .pcapng soal terkait.

![Ss Soal4](images/Screenshot%202023-09-22%20215326.png)

- masukkan filter dibawah ini

```bash
telnet
```

- cari paket dan berikut hasil filter :

![Ss Soal4](images/Screenshot%202023-09-22%20215429.png)

- kendala dalam soal ini terletak pada pencarian username dan password yang tepat.
