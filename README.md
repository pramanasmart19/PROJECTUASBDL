# PROJECTUASBDL
Sistem Informasi Toko Buku Pramana
UAS Mata Kuliah Basis Data Lanjutan Kadek Agung Manik Pramana - 2201010088

ERD (Entity Relationship Diagram)


Deskripsi Proyek Projek basis data yang saya buat yakni membangun sistem basis data yang efisien dan terstruktur untuk mengelola data toko Buku, yang mencakup pelanggan, produk, pesanan, dan detail pesanan. Komponen yang digunakan yakni:
Basis data Tabel Customer: Menyimpan informasi pelanggan seperti ID, nama, alamat, dan nomor telepon. Tabel Produk: Menyimpan informasi produk seperti ID, nama produk, harga, dan stok. Tabel Order: Menyimpan informasi pesanan seperti ID pesanan, ID pelanggan, dan tanggal pesanan. Tabel Detail: Menyimpan detail setiap pesanan seperti ID detail pesanan, ID pesanan, ID produk, dan jumlah produk.

Fungsi Agregat SUM: Menghitung total penjualan. COUNT: Menghitung jumlah total pesanan. AVG: Menghitung rata-rata jumlah barang yang dipesan.

Trigger dan View Trigger: Mengurangi stok produk secara otomatis setiap kali ada pesanan baru. View: Menyediakan ringkasan pesanan.

Index Dibuat untuk meningkatkan kinerja query pada kolom-kolom yang sering digunakan dalam pencarian dan join

Penjelasan
Membuat database Database yang saya buat, saya namai dengan db_uas DB

Membuat dan memasukkan data pada tabel Saya membuat 4 tabel, diantaranya:

Tabel Customer (tb_customer) Berisi customer_id, nama, alamat, dan no_telp DB DAN TB CUSTOMER - Copy Pengisian data TB CUSTOMER INSERT

Tabel produk (produk) Berisi produk_id, nama_produk, harga, stok TB PRODUK Pengisian data TB PRODUK INSERT

Tabel Order (tb_order) Berisi order_id, customer_id, tanggal TB ORDER Pengisian data TB ORDER INSERT

Tabel detail (tb_detail) Berisi detail_id, order_id, produk_id, kuantitas TB DETAIL Pengisian data TB DETAIL INSERT

Trigger Memiliki fungsi untuk mengurangi stok produk secara otomatis setiap kali ada pesanan baru yang dimasukkan ke dalam tb_detail

View

Untuk menampilkan informasi pesanan lengkap dengan detailnya dalam bentuk yang lebih mudah dipahami
View menggabungkan data dari beberapa tabel untuk memberikan gambaran lengkap setiap pesanan yang dilakukan Screenshot 2024-06-26 182043
Agregat

Agregat tersebut menggunakan operator SUM dan digunakan untuk melihat total penjualan per produk 

Agregat ini menggunakan operator COUNT yang digunakan untuk melihat jumlah pesanan per pelanggan 

Agregat ini menggunakan operator AVARAGE yang digunakan untuk melihat rata-rata jumlah produk yang dipesan 

Agregat ini menggunakan operator SIM yang digunakan untuk melihat total penjualan per hari Screenshot 

Index Index membantu mempercepat operasi query dengan membuat struktur data yang memungkinkan pencarian lebih cepat.

Index pada kolom customer_id di tb_order tborder

Index pada kolom order_id di tb_detail rbdetail

Index pada kolom produk_id di tb_detail tbdetail2

Index pada kolom nama_produk di tb_produk produk

Left Join Menggabungkan dua tabel dan mengembalikan semua baris dari tabel kiri, serta baris yang cocok dari tabel kanan inner left

Inner Join Menggabungkan dua tabel dan hanya mengembalikan baris yang memiliki kecocokan di kedua tabel inner join

Subquery Membantu memecah query yang rumit menjadi bagian-bagian yang lebih mudah dipahami dan dikelola serta digunakan dalam klausa WHERE, HAVING, FROM, dan SELECT untuk membandingkan dan menyaring data. inner join

Having Untuk menyaring hasil agregat setelah menggunakan group by having

Wildcard Digunakan dalam klausa LIKE untuk mencari pola dalam teks. % digunakan untuk mencocokkan nol atau karakter, dan _ digunakan untuk mencocokkan satu karakter wildcard

Dump Proses ekspor data dari sebuah database ke dalam format yang dapat disimpan, dipisahkan, atau diimpor kembali.
