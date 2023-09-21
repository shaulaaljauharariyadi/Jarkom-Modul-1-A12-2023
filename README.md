# lapresJarKom1
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

![Ss Soal1.2](images/Screenshot%202023-09-21%20104746.png)

lalu cari Sequence number(raw) dan Acknowledge number(raw) dari log STOR tersebut 



