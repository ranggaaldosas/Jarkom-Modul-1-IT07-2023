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
   <p align="center">
    <img src="https://i.ibb.co/c82NmMB/1695384489491.jpg">
4. Jawab pertanyaan sesuai hasil filtering tersebut
<p align="center">
    <img src="https://i.ibb.co/tL6nBbD/1695384514023.jpg">
    
**`FLAG: Jarkom2023{ada_di_screenshot}`**

---

### Soal 2

1. liat header pada web nya
<p align="center">
    <img src="https://i.ibb.co/ZGYXZWT/1695384527680.jpg">

2. terlihat server nya bernama gunicorn, input gunicorn di netcat.

3. masukin gunicorn di nc
<p align="center">
    <img src="https://i.ibb.co/BwjpxmZ/1695384542387.jpg">

**`FLAG: Jarkom2023{ada_di_screenshot}`**

---

### Soal 3

1. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?
2. Dari pertanyaan tsb, filter dengan cara berikut ip.addr == 239.255.255.250 && udp.port == 3702 sehingga didapatkan capture paket sesuai dengan permintaan soal kemudian dihitung dan didapatkan 21 paket dan terlihat protocol nya adalah UDP
   <p align="center">
    <img src="https://i.ibb.co/Y8jWJCK/1695384554735.jpg">
4. Masukkan di nc
   <p align="center">
    <img src="https://i.ibb.co/xzy1535/1695384563405.jpg">


**`FLAG: Jarkom2023{ada_di_screenshot}`**

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
1. download file pcap, dan telusuri di wireshark, dapet encoded base64 password
   <p align="center">
    <img src="https://i.ibb.co/jyHFwq4/1695385182942.jpg">
2. pass zip == 5implePas5word
   <p align="center">
    <img src="https://i.ibb.co/2vBk385/1695385214245.jpg">
   <p align="center">
    <img src="https://i.ibb.co/mvs6zsQ/1695385226520.jpg">
3. jawab pertanyaan sesuai di nc nya
   <p align="center">
    <img src="https://i.ibb.co/v3ydc0c/1695385238540.jpg">
   <p align="center">
    <img src="https://i.ibb.co/7r4FxmN/1695385250984.jpg">
   - Berapa packet -> wireshark statistics, terlihat 60
   - port common untuk SMTP -> 25
   - IP mana yang merupakan public -> hanya ada 2 IP yaitu 10.10.1.4 dan 74.53.140.153, karna 10.10.1.4 masuk ke rentang IP Private, jadi jawabanya 74.53.140.153

**`FLAG: Jarkom2023{ada_di_screenshot}`**

---

### Soal 6

1. Sesuai hint soal “server SOURCE ADDRESS 7812”, kami mencari packet bernomor 7812 di file pcap tersebut
   <p align="center">
    <img src="https://i.ibb.co/8cdNnRw/1695385278020.jpg">
3. kami mendapatkan source address nya adalah 104.18.14.101, sesuai hint, yaitu a1z26, kami mencoba mendecode source address tersebut
10 = J, 4 = D, 18 = R, 14 = N, 10 = J, 1 = A
4. Dikarenakan terdapat hint “SOURCE ADDRESS ADALAH KUNCI SEMUANYA.” alias JDRNJA, kami memasukkan hal tersebut di netcat, lalu kami mendapatkan flag tersebut
   <p align="center">
    <img src="https://i.ibb.co/QJDDBQf/1695385265541.jpg"

**`FLAG: Jarkom2023{ada_di_screenshot}`**


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

1. pada soal yang tertera  disuruh lakukan kueri filter. filternya menggunakan `tcp.dstport == 80 || udp.dstport == 80` sesuai clue
2. lakukan netcat
<p align="center">
    <img src="https://i.ibb.co/Vgsh8RP/1695385964838.jpg">
   
**`FLAG: Jarkom2023{ada_di_screenshot}`**

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











