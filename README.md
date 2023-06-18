# UAS_Python_V3922039_Renasya
Renasya Nanda Fafirly (V3922039) TI E

Langakh pertama saya mengambil data (scrapping data) dari salah satu E-Commerce yaitu bukalapak. untuk kategori datanya adalah tas. melakukan scraping data produk dari API Bukalapak menggunakan permintaan HTTP dengan modul requests dan menyimpan hasilnya ke dalam file CSV. dengan import csv, os, dan requests. Skrip ini menggunakan tiga modul yaitu csv untuk manipulasi file CSV, os untuk manipulasi sistem file, dan requests untuk melakukan permintaan HTTP ke API Bukalapak.

Langkah kedua meminta input dari pengguna dengan memasukkan script:
key = input('Masukkan keyword: ')
key = key.replace(' ', '_')
Skrip ini meminta pengguna untuk memasukkan kata kunci produk yang ingin dicari. Kata kunci tersebut kemudian diubah dengan mengganti spasi menjadi garis bawah ('_') agar sesuai dengan format yang digunakan dalam URL API.

Langkah ketiga membuat direktori 'hasil'
if not os.path.exists('hasil'):
    os.makedirs('hasil')
Skrip ini memeriksa apakah direktori 'hasil' sudah ada. Jika tidak, maka akan membuat direktori tersebut untuk menyimpan file CSV yang akan dihasilkan.

Langkah keempat membuat file csv

Langkah kelima mengambil data produk dari API Bukalapak
Skrip tersebut melakukan permintaan GET ke API Bukalapak dengan menggunakan URL https://api.bukalapak.com/multistrategy-products. Setiap halaman yang akan diambil ditentukan oleh variabel page dalam rentang range(1, 3). Dalam setiap permintaan, parameter yang diberikan mencakup kata kunci pencarian, jumlah produk per halaman, posisi awal indeks produk, dan beberapa parameter lainnya. Respons API dikembalikan dalam format JSON dan data produk diambil dari atribut 'data' dalam respons tersebut.

Langkah keenam memproses data produk

Langkah ke tujuh menyimpan data produk ke file csv

Langkah terakhir menampilkan informasi produk
untuk informasi yang ditampilkan adalah  nomor produk, nama produk, harga, dan alamat toko.

Dengan demikian, skrip tersebut melakukan scraping data produk dari API Bukalapak berdasarkan kata kunci yang dimasukkan oleh pengguna. Data produk yang ditemukan disimpan dalam file CSV dengan nama sesuai dengan kata kunci. Setiap baris dalam file CSV berisi informasi produk seperti nama, harga, dan alamat toko.
