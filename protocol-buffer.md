---
description: >-
  Protocol buffer ( protobuf ) adalah metode serialisasi data yang terstruktur
  yang dibuat oleh Google.
---

# Protocol Buffer

### Apa itu Protobuf

Protobuf hanya bertugas di bagian serialisasi data saja, untuk komunikasi antar service atau antar aplikasi sendiri menggunakan GRPC.

{% hint style="info" %}
GRPC merupakan sebuah Remote Procedure Call (RPC) yang dibuat oleh google. \
GRPC menggunakan HTTP/2 untuk komunikasinya dan Protocol Buffers di bagian antarmuka ( skema )-nya.
{% endhint %}

Pada saat ini mungkin masih terasa membingungkan. Sebenarnya untuk apa protobuf ini?\
Layak-nya JSON merupakan payload / muatan / bentuk data yang sering digunakan dalam berkomunikasi (request / response) pada REST API.

<figure><img src=".gitbook/assets/Request Response - Rest JSON.png" alt=""><figcaption><p>Analogy - REST API With JSON</p></figcaption></figure>

Begitu juga Protobuf yang merupakan payload / muatan / bentuk data yang digunakan dalam berkomunikasi (request / response) pada GRPC Over HTTP/2.

<figure><img src=".gitbook/assets/Request Response - GRPC Protobuf.png" alt=""><figcaption><p>Analogy - GRPC Over HTTP 2 With Protobuf</p></figcaption></figure>

### Perbedaan Protobuf

| Protobuf                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | JSON                                                                                                                                           |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| \[nama\_file].proto                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | \[nama\_file].json                                                                                                                             |
| Harus dikompilasi skema-nya dengan kompilator protobuf yaitu _**protoc**_                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Tidak perlu dikompilasi.                                                                                                                       |
| <p>Memiliki sebuah aturan skema yang harus dikuti untuk bertukar informasi. <br>(Pesan Kompleks)</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | <p>Tidak memiliki sebuah aturan skema yang harus diikuti untuk bertukar informasi.<br>(Pesan Simple)</p>                                       |
| Tidak bisa dibaca karena mengunakan binary format.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Dapat dibaca karena mengunakan text format.                                                                                                    |
| Support beberapa bahasa pemograman. seperti C++, C#, Java, Kotlin, Objective-C, PHP, Python, Ruby, Dart dan Go.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Hampir disupport semua bahasa pemograman.                                                                                                      |
| Tipe data behubungan dengan skema yang dibuat.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Tipe data dibuat semua dalam text                                                                                                              |
| Bagus untuk komunikasi antar service.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Bagus untuk komunikasi server service dengan web service.                                                                                      |
| <p>Support banyak tipe data.</p><p></p><p>List Tipe Data:<br><a href="https://developers.google.com/protocol-buffers/docs/proto#scalar">https://developers.google.com/protocol-buffers/docs/proto#scalar</a><br><br>Tipe Data Syntax:<br><a href="https://developers.google.com/protocol-buffers/docs/overview#syntax">https://developers.google.com/protocol-buffers/docs/overview#syntax</a><br><br>Tipe Data Tambahan:<br><a href="https://developers.google.com/protocol-buffers/docs/overview#data-types">https://developers.google.com/protocol-buffers/docs/overview#data-types</a></p> | <p>Hanya support beberapa tipe data:</p><ul><li>String</li><li>Number</li><li>JSON Object</li><li>Array</li><li>Boolean</li><li>Null</li></ul> |

### Instalasi



### Sumber

{% embed url="https://dasarpemrogramangolang.novalagung.com/C-golang-protobuf-implementation.html" %}

{% embed url="https://www.educba.com/protobuf-vs-json/" %}

{% embed url="https://medium.com/programmer-geek/protobuf-vs-json-304c03a6ab92" %}
