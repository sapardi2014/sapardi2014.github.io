---
layout: post
title: "Curl: Restfull Web Service Consumers"
date: 2014-03-06 18:37:41 +0700
comments: true
published: true
categories: Linux 
---

###CURL - Client Restfull Web Service Consumers
---

Restfull Web Service adalah teknologi SOA yang berbasis pada Rest. Terdapat beberapa operasi pada Rest diantaranya :

- GET
- POST
- PUT 
- DELETE

Pada sesi ini akan dibahas mengenai **curl** command di OS Linux. Curl adalah restfull client berbasis Linux yang dijalankan melalui command prompt / terminal. Seringkali untuk menguji Restfull Web Service menggunakan web browser atau add-on yang disediakan oleh web browser tersebut. Di Linux ada alternatif lain yang dapat melakukan proses tersebut.

Perintah dasar menggunakan **Curl** adalah:

	curl -X GET -D header.txt http://example.com/some/path

Perintah diatas akan melakukan HTTP GET request untuk URI http://example.com/some/path. Dan akan menyimpan hasil dari response kedalam file *header.txt* (lihat option -D) 

Beberapa *option* perintah **Curl** yang sering digunakan adalah :

- `-D filename`
		
        Menyimpan response header kedalam file *filename*

- `-i`
		Mengirim response header kedalam standard output, bersama dengan response body

- `--basic --user username:password` 
		Authenticate request menggunakan HTTP Basic authentication, dengan username dan password yang spesifik

-  `-H "header: value"`
		Mengatur request header header dengan value 

> **Notes**: Perhatikan *double quotes* yang akan passing semua header dalam *single string*. Untuk setting multiple request header dapat menggunakan multiple -H   

- `-T filename`
		Mengirim isi dari file filename sebagai body dari request PUT. Option ini berguna untuk proses upload file.

- `-k`
		Mengabaikan SSL certificate. Sangat berguna ketika berhubungan dengan server development dengan Self-signed Certificate. 


- `h`
		Untuk bantuan (help). Menampilkan semua option dari command Curl 


Jadi kesimpulannya Restfull Web Service tidak harus menggunakan web browser, bagi Anda yang menyukai dunia CLI di terminal Linux, ini adalah alternatif nya. Selamat mencoba, silahkan berikan saran atau komentar. 

###Referensi:

[Cara membuat Self-signed Certificate](http://software.endy.muhardin.com/aplikasi/membuat-self-signed-certificate/)

[Curl Cheat Sheet](http://blog.engelke.com/2009/10/20/curl-cheat-sheet/)





