## __1. Business Problem Understanding__ 
---
### **Transaksi Transportasi Publik Transjakarta**
__Latar Belakang__

Transjakarta adalah moda transportasi massal yang mendukung aktivitas di Ibu Kota Jakarta. Transjakarta memiliki sistem *Bus Rapid Transit* (BRT), yang artinya bus angkutan cepat.

Transjakarta memiliki lintasan sejauh 230,9 km dan memiliki 252 halte yang tersebar dalam 14 koridor (rute utama). Kini Transjakarta beropresi selama 24 jam di seluruh koridornya.

__Pernyataan Masalah__

PT Transportasi Jakarta ingin memperoleh informasi mengenai aktivitas Transjakarta pada April 2024 untuk mengukur minat dan pola penggunaan Transjakarta di masyarakat.

`Fokus Analiss`
1. Demografi pelanggan Transjakarta selama April 2023
2. Pola dan preferensi pelanggan
3. Aktivitas sistem transportasi seperti, koridor dan halte: efektifitas dan efisiensi sistem


## __2. Keterangan Kolom__
|No| Nama Kolom | Keterangan |
|--|------------|------------|
|1| transID | id transaksi yang unik untuk setiap transaksi | 
|2| payCardID | Pengidentifikasi utama pelanggan. Kartu yang digunakan pelanggan sebagai tiket masuk dan keluar|
|3| payCardBank| Nama penerbit bank kartu pelanggan| 
|4| payCardName| Nama yang terdaftar di kartu|
|5| payCardSex| Jenis kelamin pelanggan yang terdaftar di kartu|
|6| payCardBirthDate| Tanggal lahir pelanggan|
|7| corridorID | ID koridor/rute ID sebagai kunci pengelompokkan rute| 
|8| corridorName| nama koridor/nama rute berisi Awal dan Selesai untuk setiap rute | 
|9| direction| 0 untuk pergi, 1 untuk kembali. Arah rute| 
|10| tapInStops| *Tap In* (entrance) Stops ID untuk mengidentifikasi nama perhentian|
|11| tapInStopsName| *Tap In* (entrance) nama perhentian tempat pelanggan *tap in*.
|12| tapInStopsLat| Garis Lintang Tap In Stop|
|13| tapInStopsLon| Bujur Tap In Stop|
|14| stopStartSeq| Urutan pemberhentian, pemberhentian pertama, pemberhentian kedua, dll. Terkait dengan arah.|
|15| tapInTime| Waktu *tap in*. Tanggal dan waktu. 
|16| tapOutStops| *Tap Out* (*Exit*) Stops ID untuk mengidentifikasi nama perhentian|
|17| tapOutStopsName| *Tap out* (*Exit*) nama perhentian tempat pelanggan *tap out*|
|18| tapOutStopsLat| Garis Lintang Perhentian *Tap Out*|
|19| tapOutStopsLon| Garis Bujur dari *Tap Out Stop*|
|20| stopEndSeq| Urutan pemberhentian, pemberhentian pertama, pemberhentian kedua, dll. Terkait dengan arah|
|21| tapOutTime| Waktu keluar. Tanggal dan waktu|
|22| payAmount| umlah yang dibayar pelanggan. Beberapa gratis. Beberapa tidak.

## __3. Data Cleaning and Transformaation Summary__
1. Ubah tipe data
2. Imputasi missing value
3. Drop missing value
4. Check outlier
5. Menambah kolom

Additional Columns

|No| Nama Kolom | Keterangan |
|--|------------|------------|
|1| age | Umur pelanggan berdasarkan tahun lahir dan tanggal transaksi | 
|2| stopRange | Jumlah perhentian untuk dapat sampai ke tujuan perhentian|
|3| dateIn| Tanggal Tap In| 
|4| dayIn| Nama hari Tap In|
|5| timeHourMinuteIn| Waktu Tap In (dalam jam)|
|6| timeHourMinuteOut| Waktu Tap Out (dalam jam)|
|7| travelDuration | Durasi perjalanan dalam menit|
|8| custTripFreq | Frekuensi perjalanan dalam sebulan|
|9| rfm_level | Segmentasi berdasarkan resensi, frekuensi, dan monetary pelanggan dalam sebulan|

## __4. Analysis Summary__
1. Analisis Deskriptif
2. Analisis Inferensial: chi-square (untuk melihat hubungan antara dua variabel kategorikal)

## __5. Kesimpulan dan Rekomendasi__
Selengkapnya pada Jupyter notebook

