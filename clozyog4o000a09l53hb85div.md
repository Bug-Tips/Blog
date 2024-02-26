---
title: "Tutorial instalasi Burp Suite di linux"
seoTitle: "Tutorial instalasi Burp Suite"
seoDescription: "Pada artikel ini kita akan membahas bagaimana cara instalasi Burp Suite di sistem operasi linux."
datePublished: Sat Feb 24 2024 16:00:00 GMT+0000 (Coordinated Universal Time)
cuid: clozyog4o000a09l53hb85div
slug: tutorial-instalasi-burp-suite-di-linux
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1708844576256/318a9cf5-440c-4980-ae5f-4dd5c18db8a0.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1708844792912/c74b409c-058d-446b-a352-1beec0e94fed.png
tags: tools, burpsuite, ethicalhacking

---

## Instalasi

Sebelum melakukan instalasi, pastikan kalian sudah mendownload file Burp Suitenya terlebih dahulu di website resmi Burp Suite atau langsung kunjungi link [berikut](https://portswigger.net/burp/releases/community/latest).

Jika kalian sudah mendownload filenya, silahkan buka terminal dan kunjungi lokasi file tersebut, umumnya terletak pada directory Download.

Ubah izin file agar dapat dieksekusi dengan perintah berikut:

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Sesuaikan nama filenya dengan yang kalian download</div>
</div>

```bash
chmod +x burpsuite_community_linux_v2023_12_1_5.sh
```

Selanjutnya, jalankan file tersebut dengan perintah:

```bash
./burpsuite_community_linux_v2023_12_1_5.sh
```

Setelah itu, jendela instalasi akan muncul. Klik **next** untuk melanjutkan proses.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708836239293/876c4bf8-b859-4d91-a6cf-dc52b284b3a3.png align="center")

Kemudian kalian akan diminta untuk memilih lokasi dimana Burp Suitenya akan di install, kalian dapat merubah lokasinya atau biarkan secara default.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708836903270/d0cd84ed-759b-4798-a80e-9362ef54d5cb.png align="center")

Selanjutnya, pilih lokasi symlink untuk Burp Suite, kalian bisa biarkan secara default. Klik **next** dan tunggu hingga proses instalasi selesai.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708837423028/da685fd8-5174-4434-b2d8-f12a39f0bb0f.png align="center")

Jika proses instalasinya berjalan dengan lancar, maka akan tampak seperti di atas. klik **finish** untuk mengakhiri proses instalasinya.

## Menjalankan Burp Suite

Silahkan buka Burp Suite yang telah kalian install, untuk versi communitynya kalian hanya dapat menggunakan temporary project. Berikut adalah tampilannya.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708841010070/22b79f4e-cf02-40d2-8839-f6356c66acbc.png align="center")

Jika kalian hanya ingin menggunakan browser bawaan dari Burp Suite, cukup buka tab **Proxy**, lalu klik **Open Browser**. Namun jika ingin menggunakan browser yang biasa kalian gunakan, maka diperlukan beberapa tahap lanjutan seperti mengatur proxy dan menginstall sertifikat Burp Suite pada browser kalian terlebih dahulu.

Berikut adalah bagaimana cara mengatur proxy dan menginstall sertifikat pada browser firefox.

### Mengatur Proxy di Firefox

Pertama pergi ke pengaturan, lalu pada kolom pencarian ketikkan **proxy.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708842831879/7d557423-0fd0-4c95-bc65-d00de01dd6a7.png align="center")

Ubah pengaturan proxynya dari **Use system proxy settings** menjadi **Manual proxy configuration**, dan isi **HTTP Proxynya** menjadi **127.0.0.1** dan **port** menjadi **8080**, jangan lupa centang juga **Also use this proxy for HTTPS.**

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Jika kalian sudah tidak menggunakan Burp Suite maka kembalikan pengaturan proxynya ke <strong>Use system proxy settings.</strong></div>
</div>

### Instalasi Sertifikat Burp Suite di Firefox

Pastikan proxy kalian sudah aktif, lalu kunjungi halaman berikut [http://burp/](http://burp/)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708843354808/04887e8d-6093-402f-85bd-30217b6c2196.png align="center")

Silahkan unduh **CA Certificate** nya. lalu pergi ke pengaturan firefox kalian, dan ketikkan **Certificate.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708843592830/1b238692-e2bc-4f04-b423-fa21d53a952d.png align="center")

Klik **View Certificates** lalu buka tab **Authorities**, dan **import** sertifikat yang sebelumnya sudah kalian download.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708843678958/d1cedb05-ae12-4a66-a9f1-7ababfb72173.png align="center")

Jika sudah silahkan buka halaman [https://example.com](https://example.com) dan pastikan bahwa kalian bisa melihat history http kalian pada menu **Proxy-&gt;HTTP History** di Burp Suite.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1708843941664/97d9bcdd-a91f-4841-b652-b6901654d4f0.png align="center")

Selamat kalian sudah berhasil menginstall Burp Suite. Mungkin itu saja yang bisa saya sampaikan pada artikel kali ini, semoga bermanfaat.