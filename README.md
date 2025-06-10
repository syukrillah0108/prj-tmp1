# Konsep

### Alur Kerja Sistem

![Work Flow](concept/img/wokflow.svg)

#### Deskripsi Konsep Sistem IoT Monitoring Tanaman

Sistem ini merupakan solusi berbasis IoT (Internet of Things) yang dirancang untuk melakukan monitoring kondisi tanaman secara real-time menggunakan handphone. Sistem bekerja dengan cara mengumpulkan data lingkungan dari berbagai sensor, mengolah data menggunakan mikrokontroler, dan mengirimkannya ke cloud system agar dapat diakses oleh pengguna melalui aplikasi di smartphone.

#### **Komponen dan Alur Kerja:**

1. **Sensor Suhu**
   * Mengukur temperatur udara di sekitar tanaman.
   * Data suhu dikirim ke mikrokontroler.
2. **Sensor Kelembapan**
   * Mengukur tingkat kelembapan udara atau tanah.
   * Informasi ini penting untuk menentukan kebutuhan air tanaman.
3. **Sensor pH**
   * Mengukur tingkat keasaman tanah.
   * Memberikan gambaran tentang kesesuaian pH tanah untuk pertumbuhan tanaman.
4. **Sensor Nutrisi**
   * Mengukur kadar nutrisi dalam tanah.
   * Data ini digunakan untuk mengetahui apakah tanaman memerlukan tambahan pupuk.
5. **Mikrokontroler**
   * Berfungsi sebagai pusat kendali yang mengumpulkan semua data dari sensor suhu, kelembapan, pH, dan nutrisi.
   * Memproses data dan mengirimkannya ke cloud system.
6. **Cloud System**
   * Menyimpan dan mengelola data dari mikrokontroler.
   * Data disajikan dalam bentuk yang dapat dimengerti dan diakses melalui aplikasi di smartphone.
7. **Smartphone**
   * Digunakan oleh pengguna untuk memonitor kondisi tanaman dari jarak jauh secara real-time.
   * Memberikan notifikasi atau informasi penting terkait kondisi tanaman.

### Alur Data Sistem

![Work Flow](concept/img/dataflow.svg)

Diagram ini menggambarkan alur data dalam sistem IoT yang digunakan untuk memantau tanaman secara real-time menggunakan perangkat mobile. Alur ini menunjukkan bagaimana data dari sensor dikumpulkan, diproses, disimpan, dan ditampilkan kepada pengguna.

#### **1. Device Layer (Perangkat)**

* **Sensor Data**

  Sensor-sensor (seperti suhu, kelembapan, pH, dan nutrisi) mendeteksi kondisi lingkungan dan menghasilkan data.
* **Controller (Mikrokontroler)**

  Mikrokontroler menerima data dari sensor, memprosesnya, dan menyiapkannya untuk dikirim ke cloud server.

#### **2. Cloud Server Layer**

* **Server**

  Menerima data dari mikrokontroler, melakukan pengelolaan, validasi, dan pengolahan lebih lanjut.
* **Data Store (Database)**

  Data dari sensor disimpan dalam database agar bisa diakses kapan saja oleh pengguna atau aplikasi.

#### **3. Mobile Apps Layer**

* **API (Application Programming Interface)**

  API bertugas menjadi penghubung antara database/cloud server dengan aplikasi monitoring di handphone. Data dikirim ke API untuk diambil oleh aplikasi.
* **Monitoring (Aplikasi Mobile)**

  Pengguna dapat melihat data tanaman secara real-time melalui aplikasi yang terhubung ke API. Ini memungkinkan pemantauan jarak jauh dan pengambilan keputusan cepat.


### **Ringkasan Alur:**

**Sensor** → **Controller** → **Server** → **Database** → **API** → **Monitoring (Mobile App)**

Sistem ini memungkinkan pengguna untuk:

* Memantau kondisi tanaman dari mana saja
* Mendapatkan data yang selalu diperbarui
* Mengambil tindakan berbasis data aktual seperti menyiram, memberi pupuk, atau mengecek pH tanah
