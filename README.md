# Jarkom-Modul-1-C09-2022

Praktikum Probstat Modul 2

```
Andi Muhammad Rafli - 5025201089
Adinda -
Achmad Ferdiansyah -
```

### Soal 1

> Sebutkan web server yang digunakan pada "monta.if.its.ac.id"!

a. Pada display filter, carilah “http.host contains monta.if.its.ac.id”, tampilannya akan seperti ini :

<img width="337" alt="image" src="https://user-images.githubusercontent.com/102727966/192096356-3c61a066-9875-4467-997c-cd2c4a21db09.png">

b. Klik kanan pada package manapun, klik kanan untuk pilih follow dan http stream sehingga memunculkan gambar sebagai berikut :

<img width="339" alt="image" src="https://user-images.githubusercontent.com/102727966/192096375-7cf25eae-6b6e-411a-ad98-9b40347b8df9.png">

c. Liat pada server : nginx/1.10.3

### Soal 2

> Ishaq sedang bingung mencari topik ta untuk semester ini , lalu ia datang ke website monta dan menemukan detail topik pada website “monta.if.its.ac.id” , judul TA apa yang dibuka oleh ishaq ?

a. Pada display filter, carilah “http.host contains monta.if.its.ac.id”, tampilannya akan seperti ini :

<img width="468" alt="image" src="https://user-images.githubusercontent.com/102727966/192096438-d7926a6c-e8db-411f-8579-7ae349fe6f9b.png">

b. Kemudian pilih file dengan klik export object dan klik HTTP

<img width="468" alt="image" src="https://user-images.githubusercontent.com/102727966/192096459-e6a41f0a-c8c8-4bbf-89a0-950edbe493f1.png">
 
c. Pilihlah file dengan nama 194 yang mana artinya file tersebut mengandung detail topik dan save dengan format html

<img width="468" alt="image" src="https://user-images.githubusercontent.com/102727966/192096491-7cb76545-ad77-43f9-920f-85ae624f72c2.png">

d. Bukalah file yang telah didownload tadi dan akan langsung menuju website

<img width="468" alt="image" src="https://user-images.githubusercontent.com/102727966/192096592-b48265e3-383e-42c0-a1a7-4f73f46f4809.png">

### Soal 3

> Filter sehingga wireshark hanya menampilkan paket yang menuju port 80!

a. Ketikkan <strong>tcp.dstport == 80</strong> pada kotak display filters

<img width="468" alt="image" src="https://user-images.githubusercontent.com/102727966/192097148-c917cbd3-3832-45f0-bedb-cb3d9241dfb1.png">

### Soal 4

> Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21!
> a. Ketikkan <strong>tcp.srcport == 21</strong> pada display filters

<img width="468" alt="image" src="https://user-images.githubusercontent.com/102727966/192097201-830a2634-520f-47a6-9376-82f016055dba.png">

### Soal 6

> Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id !
> a. Diperlukan IP address lipi.go.id dengan cara buka web lipi.go.id

<img width="468" alt="image" src="https://user-images.githubusercontent.com/102727966/192097275-9591b688-960e-452f-984b-646fe4785e43.png">

b. Lalu buka terminal/CMD dan ketikkan ping lipi.go.id maka akan terlihat IP addressnya

<img width="468" alt="image" src="https://user-images.githubusercontent.com/102727966/192097287-969ecff2-2c43-4393-bede-c8f6b64142b4.png">

c. Salin IP address webnya 203.160.128.158

d. Lalu ketikkan ke display filters wireshark ip.dst == 203.160.128.158

<img width="468" alt="image" src="https://user-images.githubusercontent.com/102727966/192097322-e4562c99-e323-402c-9179-feb0b0d4f111.png">

e. Maka akan muncul seluruh paket yang menuju ke alamat IP lipi.go.id

### Soal 8

> Telusuri aliran paket dalam file .pcap yang diberikan, cari informasi berguna berupa percakapan antara dua mahasiswa terkait tindakan kecurangan pada kegiatan praktikum. Percakapan tersebut dilaporkan menggunakan protokol jaringan dengan tingkat keandalan yang tinggi dalam pertukaran datanya sehingga kalian perlu menerapkan filter dengan protokol yang tersebut.
> a. Search protokol dengan keandalan tertinggi

<img width="413" alt="image" src="https://user-images.githubusercontent.com/102727966/192097479-930a80dd-4b54-4897-8a8d-3a2704a76f94.png">

b. Protokol paling andal yaitu TCP
c. Masuk ke wireshark dan ketik pada display filter tcp untuk cari protokol TCP

<img width="468" alt="image" src="https://user-images.githubusercontent.com/102727966/192097515-9d0e69af-eaf8-4f7f-8441-831829f7171b.png">

d. Ada informasi mencurigakan yang muncul di pojok kanan bawah, dan terjadi antara ip

<img width="468" alt="image" src="https://user-images.githubusercontent.com/102727966/192097537-d519241f-8725-474c-9c42-d9446bb1f369.png">
v r55

e. Coba cek di filter, ketik ip.host == 127.0.0.1 && ip.host == 127.0.1.1 lalu klik kanan salah satu paket–>follow-->TCP Stream

<img width="468" alt="image" src="https://user-images.githubusercontent.com/102727966/192097552-c3605315-6b3d-4a07-b3bd-8396a9ef2bc9.png">

f. Ternyata ditemukan indikasi kecurangan

### Soal 9

> Terdapat laporan adanya pertukaran file yang dilakukan oleh kedua mahasiswa dalam percakapan yang diperoleh, carilah file yang dimaksud! Untuk memudahkan laporan kepada atasan, beri nama file yang ditemukan dengan format [nama_kelompok].des3 dan simpan output file dengan nama “flag.txt”.
> a. Kata kuncinya adalah file, dari percakapan no. 8, kemungkinan ada percakapan yang mengandung kata “file”, coba filter dengan mengetik tcp contains “file” lalu klik kanan->follow->TCP Stream.

<img width="444" alt="image" src="https://user-images.githubusercontent.com/102727966/192097587-0406451a-634f-48c9-a7bf-cfe33cbd9d88.png">

b. Dari percakapan didapatkan informasi “file berupa salt” beserta cara decrypt filenya, password berupa nama karakter anime kembar lima huruf kecil semua, dan pengiriman file ke port “9002”.
c. Informasi pertama, cari file salt dengan mengetikkan tcp.port == 9002 atau tcp.srcport == 9002

<img width="401" alt="image" src="https://user-images.githubusercontent.com/102727966/192097608-3c4051c0-af1e-497c-8369-ae88e40cd7c0.png">

d. Maka akan tampil port “9002” sebagai src atau pengirim, dan disini terdapat 3 port tujuan yaitu [45800, 45822, 45824], salah satu port adalah filenya.
e. Klik kanan dstport “45800”, maka akan muncul saltnya
f. Pada bagian “show data as” pilih tipenya menjadi raw dan save as C09.des3
g. Informasi selanjutnya yaitu mencari kemungkinan password dari nama karakter anime kembar 5 (Gotoubun no Hayanome).
h. Kemungkinan: [“itsuki”, “yotsuba”, “miku”, “nino”, “ichika”, “raiha”, “fuutarou”, “uesugi”, “nakano”] => password yg benar “nakano”.
i. Lalu decrypt dengan mengikuti cara yang ada pada percakapan.
j. Buka terminal (disini kami menggunakan git bash), lalu ketik openssl des3 -d -salt -in C09.des3 -out flag.txt -k nakano.

<img width="375" alt="image" src="https://user-images.githubusercontent.com/102727966/192097668-beb644d3-4b48-4a33-867a-9d1a37b13bdb.png">

### Soal 10

> Temukan password rahasia (flag) dari organisasi bawah tanah yang disebutkan di atas!
> a. Buka File hasil decrypt => “flag.txt”
> b. Passwordnya: JaRkOm2022{8uK4N_CtF_k0k_h3h3h3}

<img width="317" alt="image" src="https://user-images.githubusercontent.com/102727966/192097681-e2ab5241-3405-43b0-a87b-5e2a7de23f1d.png">
