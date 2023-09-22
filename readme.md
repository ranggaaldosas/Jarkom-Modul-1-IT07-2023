# Praktikum Modul 1 Jaringan Komputer

Praktikum Modul 1 Jaringan Komputer - **IT07**

## Authors

| Nama                                                | NRP        |
| --------------------------------------------------- | ---------- |
| [Rangga Aldo](https://www.github.com/ranggaaldosas) | 5027211059 |
| [Maulana Ilyasa](https://www.github.com/xxx)        | 5027211065 |

> .pcap file can be downloaded [here](https://drive.google.com/drive/folders/1Jm2cuNbowi4W20roqYETuWLNqjSAEgQx)

## Laporan Resmi Modul 1

### Soal 1

1. Lakukan dengan display filter ftp || ftp-data
2. Ditemukan suatu packet unik dari hasil filtering tersebut, lalu dicek
3. Jawab pertanyaan sesuai hasil filtering tersebut

<p align="center">
    <img src="https://i.ibb.co/hZBs225/IMG-4129.jpg" width=250 length=250>

**`FLAG: Jarkom2023{string}`**

---

### Soal 2

1. liat header pada web nya
<p align="center">
    <img src="https://i.ibb.co/hZBs225/IMG-4129.jpg" width=250 length=250>

2. terlihat server nya bernama gunicorn, input gunicorn di netcat.

3. masukin gunicorn di nc

**`FLAG: Jarkom2023{string}`**

---

### Soal 3

1. liat header pada web nya
<p align="center">
    <img src="https://i.ibb.co/hZBs225/IMG-4129.jpg" width=250 length=250>

2. terlihat server nya bernama gunicorn, input gunicorn di netcat.

3. masukin gunicorn di nc

**`FLAG: Jarkom2023{string}`**

---


### Soal 4

1. Di wireshark dicari paket nomor 130
2. Lalu pada User Datagram Protocol carikan Checksum
3. Dan didapatkan `Checksum: 0x18e5 [unverified]`

<p align="center">
    <img src=https://i.ibb.co/DpF1Ns6/image.png>
    
4. masukkan 0x18e5  di nc

<p align="center">
    <img src=https://i.ibb.co/6nVdD32/image.png>

**`FLAG: Jarkom2023 {ch3cksum_is_u5eful_0xcf67}`**

---

### Soal 5

1. liat header pada web nya
<p align="center">
    <img src=https://i.ibb.co/hZBs225/IMG-4129.jpg" width=250 length=250>

2. terlihat server nya bernama gunicorn, input gunicorn di netcat.

3. masukin gunicorn di nc

**`FLAG: Jarkom2023{string}`**

---

### Soal 6

1. liat header pada web nya
<p align="center">
    <img src=https://i.ibb.co/hZBs225/IMG-4129.jpg" width=250 length=250>

2. terlihat server nya bernama gunicorn, input gunicorn di netcat.

3. masukin gunicorn di nc

**`FLAG: Jarkom2023{string}`**

---

### Soal 7

1. masukkan file pcap yang diberikan lalu pada display filter di wireshark #ip.dst == 184.87.193.88
2. lalu setelah dimasukkan akan terlihat ada 6 packet yg tersedia
3. masukkan nc dan berikan jawaban 6 seperti jumlah paket yang tersedia

<p align="center">
    <img src=https://i.ibb.co/nM0cQGC/image.png>
<p align="center">
    <img src=https://i.ibb.co/wJ63krd/image.png>
    
**`FLAG: Jarkom2023 {oV6983GapVZCD5U0zO_4n0th3r_f1lt3ring}`**

---

### Soal 8

1. liat header pada web nya
<p align="center">
    <img src=https://i.ibb.co/hZBs225/IMG-4129.jpg" width=250 length=250>

2. terlihat server nya bernama gunicorn, input gunicorn di netcat.

3. masukin gunicorn di nc

**`FLAG: Jarkom2023{string}`**

---

### Soal 9

1. Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!
2. Kueri filter yang sesuai permintaan soal yaitu ip.src == 10.51.40.1 && ip.dst != 10.39.55.34

<p align="center">
    <img src="https://i.ibb.co/mBDQKkM/image.png">


**`FLAG: Jarkom2023{y3s_its_PjNkQiNhRkQ_qu3ry1ng}`**

---

### Soal 10

1.pertama setelah masukkan file pcap gunakan filter telnet di wireshark
2.brute force tiap kemungkinan username dan password
3.Lalu setelah melakukan sekian percobaan maka ditemukan jawaban yang benar dhafin:kesayangannyak0k0

<p align="center">
    <img src="https://i.ibb.co/Hp27c6d/image.png">

<p align="center">
    <img src=https://i.ibb.co/58T8GdN/image.png>

**`FLAG: Jarkom2023{t3lnet_is_95AB8yzxAx3B2xB5C_N0tsecu2e}`**

---











