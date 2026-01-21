**SLIDE 1 – PEMBUKAAN**

“Assalamu’alaikum warahmatullahi wabarakatuh.”



Selamat pagi Bapak/Ibu dosen penguji.

Perkenalkan, Imam Ramadhani, mahasiswa Program Studi D-III Teknologi Informasi.

Pada kesempatan ini saya akan mempresentasikan proposal Tugas Akhir dengan judul:



“Klasifikasi Perilaku Berkendara Berbasis IoT untuk Peringatan Dini Risiko Keausan Komponen Kendaraan.”





**SLIDE 2 – LATAR BELAKANG**

* Saat ini, sistem perawatan kendaraan yang digunakan masyarakat masih bersifat konvensional, yaitu mengandalkan jarak tempuh dan jadwal servis berkala.
* Permasalahannya, kendaraan dengan jarak tempuh yang sama belum tentu memiliki kondisi komponen yang sama, karena gaya berkendara setiap pengemudi berbeda.Perilaku seperti:

         akselerasi tajam,

         pengereman mendadak,

         putaran mesin tinggi secara berulang



* dapat mempercepat keausan komponen seperti rem, ban, dan mesin, meskipun kendaraan belum waktunya servis.



* Namun, belum banyak sistem yang memantau perilaku berkendara secara langsung dan memberikan peringatan dini risiko keausan sebelum terjadi kerusakan.



**SLIDE 3 – RUMUSAN MASALAH**



* Berdasarkan latar belakang tersebut, maka rumusan masalah dalam penelitian ini adalah:

&nbsp;        Bagaimana mengintegrasikan sensor MPU6050, GPS, dan RPM pada mikrokontroler ESP32 secara sinkron?

&nbsp;        Bagaimana mengimplementasikan Rule-Based Expert System untuk korelasi gaya berkendara dengan risiko keausan?

&nbsp;        Bagaimana membangun sistem peringatan dini (Early Warning System) yang interaktif via aplikasi Android?



**SLIDE 4 – BATASAN MASALAH**

* Sistem hanya memanfaatkan data yang diperoleh dari sensor: MPU6050 getar dan giro,GPS Neo-6M , RPM mesin Optocoupler,dan DHT22 suhu.

Data sensor digunakan sebagai representasi perilaku berkendara dan kondisi operasional kendaraan, tanpa pengukuran langsung pada komponen mekanis.



* Memerlukan koneksi internet (WiFi/Hotspot) untuk sinkronisasi Firebase Realtime.

Sistem tidak mendukung pemantauan jarak jauh secara offline.



* Output sistem dibatasi pada peringatan dini risiko keausan komponen kendaraan, meliputi:kampas rem, ban, kopling, mesin, dan suspensi Tingkat risiko disajikan dalam tiga kategori:



**SLIDE 5 – TUJUAN PENELITIAN**

  

01\. Merancang dan mengimplementasikan perangkat IoT berbasis ESP32 yang mampu melakukan klasifikasi perilaku

berkendara secara mandiri (Edge Processing).

02\. Menyediakan platform peringatan dini (Early Warning System) yang informatif bagi pengendara untuk meningkatkan

kesadaran perawatan kendaraan secara preventif.



**SLIDE 6 – TINJAUAN PUSTAKA**

**SLIDE 7 – ARSITEKTUR SISTEM**



**SLIDE 8 - TOOLS PENGEMBANGAN**

**ESP32:** Mikrokontroler utama untuk membaca data sensor, menjalankan logika sistem pakar berbasis aturan, dan mengirim data ke cloud melalui Wi-Fi



**MPU6050:** Sensor akselerometer dan giroskop untuk mendeteksi akselerasi, pengereman, dan getaran kendaraan.



**GPS Neo-6M:** Digunakan untuk memperoleh data kecepatan dan lokasi kendaraan.



**Sensor RPM:** Digunakan untuk memantau putaran mesin sebagai indikator beban kerja mesin.



**DHT22:** Digunakan untuk memantau suhu sebagai indikator awal risiko panas berlebih.



**Arduino IDE:** Digunakan untuk pemrograman mikrokontroler ESP32, termasuk pembacaan sensor, pengolahan data, dan penerapan logika sistem pakar berbasis aturan.



**Flutter (Android):** Digunakan sebagai framework pengembangan aplikasi mobile berbasis Android untuk menampilkan data sensor, hasil klasifikasi perilaku berkendara, serta peringatan dini risiko keausan komponen kendaraan.



**Firebase:** Digunakan sebagai cloud database untuk penyimpanan data sensor, log aktivitas berkendara, serta sinkronisasi data secara real-time antara perangkat IoT dan aplikasi mobile.



**SLIDE 8 – LOGIKA SISTEM PAKAR**



**SLIDE 9 – METODE Pengembangan**

**Metode penelitian yang digunakan adalah penelitian rekayasa (engineering research) dengan pendekatan eksperimental.**

**Tahapan penelitian meliputi:**

* Analisis kebutuhan
* Perancangan sistem
* Implementasi perangkat keras dan aplikasi
* Pengujian sistem
* Evaluasi dan penyempurnaan



**SLIDE 10 – PENUTUP**



**Dashboard Utama (Speedometer \& Klasifikasi Gaya Berkendara)**



* Menampilkan speedometer digital secara real-time
* Menyajikan klasifikasi gaya berkendara:



&nbsp;       > Aman

&nbsp;       > Standar

&nbsp;       > Agresif



* Informasi diperoleh dari hasil pengolahan data sensor akselerometer dan GPS
* Berfungsi sebagai indikator awal kondisi berkendara saat ini



**Halaman Kesehatan Komponen Kendaraan**



**----Menampilkan progress bar kesehatan komponen, meliputi:**

* Kampas rem
* Ban
* Mesin
* Suspensi



**----Status ditampilkan dalam kategori:**

* Risiko Rendah
* Risiko Sedang
* Risiko Tinggi



**Halaman Log \& Riwayat Berkendara Kritis**

**---Menyimpan riwayat perilaku berkendara berisiko**

**---Informasi yang ditampilkan:**

* Waktu kejadian (timestamp)
* Jenis pelanggaran ambang batas
* Komponen yang berpotensi terdampak

**---Berfungsi sebagai:**

Media evaluasi perilaku berkendara

Dokumentasi kejadian kritis (Early Warning System)



