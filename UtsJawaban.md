Brillian David Maulana Akhsan (135410104)


1. - Cassandra DBMS
   - Mongo DB
   - HBase


2. - contoh masalah big data yang digunakan untuk mengelola data pada customer bukalapak untuk keperluan analisis dengan menggunakan
     sofware Apache Spark sebagai engine untuk memproses data dalam sekala besar meliputi Big Data dan Machine Learning. lalu
     menggunakan Cassandra untuk manajemen database berbasis NoSQL.
   
   - cara instalasi nya yaitu :
      1. download filenya di https://spark.apache.org/downloads.html
      2. setelah berhasil didownload, lalu ekstrak file spark yang sudah didownload tadi ke "C:/".
      3. setting variabel untuk spark agar terintregasi dengan windows dengan cara buka My Computer -> Klik kanan -> Properties ->
         advanced system settings -> environment variables. Klik New untuk membuat variabel baru.
         buat variabel baru bernama SPARK_HOME lalu arahkan ke root instalasi pada lokasi spark yg telah saya install.
         kemudian menambahkan spark ke variabel PATH : cari variabel Path lalu klik edit tambahkan "%SPARK_HOME%\bin".
      4. menjalankan spark shell : cari spark-shell lalu run as administrator.
      5. dengan menggunakan spark-chell, saya dapat melakukan read dan write pada HDFS. untuk mengakses HDFS perlu mengubah dengan
         perintah : spark.read.json("hdfs://<Hadoop's default FS/<Directory>/<file.json>")
         
   - big data dalam e-commerce untuk menganalisis konsumen, operasional, potensi pasar, hingga inovasi produk.
     analisis data ini memberikan framework secara keseluruhan mengenai profil konsumen dan potensi yang dapat digali sebagai strategi
     pengembangan bisnis. salah satu implementasinya, data konsumen dikumpulkan dari interaksi mereka di dalam website bukalapak yang
     kemudian dianalisis untuk memaksimalkan strategi konversi penjualan. pengolahan data ini dapat meningkatkan efisiensi, profit, dan
     loyalitas konsumen.
     dengan big data kita dapat meningkatkan pengalaman belanja konsumen dengan memberikan pengalaman belanja yang memuaskan.
     contohnya, saat konsumen mengunjungi sebuah website bukalapak, mereka tidak hanya berniat untuk langsung berbelanja, tapi juga
     mencari-cariwawasan informasi pada produk apa yang kira-kira mereka butuhkan. daengan data, bukalapak dapat memberikan rekomendasi
     produk yang sesuai dengan minat konsumen berdasarkan histori pencariannya yang tersimpan pada database di bukalapak.
     data yang terkumpul di dalam database bukalapak juga bisa memberikan strategi promosi yang lebih baik dengan melakukan
     personalisasi belanja. misal data histori konsumen yang sudah terdaftar dianalisis kategori produk apa yang paling diminati.
     ketika ada promosi belanja online seperti 11/11 atau harbolnas (Hari Belanja Online Nasional), bukalapak dapat melakukan
     personalisasi dengan memberikan diskon-diskon yang relevan bagi konsumen terdaftar.
     
   - arsitektur DBMS pada cassandra. cassandra memiliki peer-to-peer sistem terdistribusi di seluruh node, dan data
     didistribusikan di antara semua node dalam sebuah cluster. semua node dalam sebuah cluster memainkan peran yang sama.
     setiap node independen dan pada saat yang sama saling berhubungan ke node lain dapat menerima membaca dan menulis permintaan, entah
     dimana letak data di cluster. ketika sebuah node performanya turun, read/write dapat dilakukan dari node lain dalam jaringan.
     replikasi data di Cassandra disebut dengan istilah Gossip Protocol dimana satu atau lebih node dalam sebuah Cluster sebagai replika
     untuk bagian tertentu dari data. jika terdeteksi bahwa beberapa node datanya out of date, Cassandra akan mengembalikan nilai terbaru
     untuk klien. setelah mendapatkan nilai kembalian terbaru, cassandra melakukan perbaikan membaca di latar belakang untuk memperbarui
     nilai-nilai yang out of date.
