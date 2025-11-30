# Data Mahasiswa Menggunakan MVC
MVC (Model–View–Controller) merupakan pola arsitektur dalam pemrograman yang
digunakan untuk memisahkan antara logika data, tampilan pengguna, dan pengendali alur
program. Tujuan penerapan pola ini adalah agar program menjadi lebih terstruktur, mudah
dikembangkan, dan setiap bagian memiliki tanggung jawab yang jelas.

Penjelasan masing-masing komponen:

• Model
Model merupakan bagian yang berfungsi untuk mengelola data dan berhubungan langsung
dengan database.

  Dalam proyek ini, bagian model terdiri atas dua kelas, yaitu:
  1. ModelMahasiswa.java – berfungsi untuk mendefinisikan struktur data mahasiswa,
  seperti id, npm, nama, semester, dan ipk. Kelas ini berisi atribut, konstruktor, serta
  getter dan setter untuk mengakses dan mengubah data.
  2. MahasiswaDAO.java – berperan sebagai penghubung antara aplikasi dan database
  MySQL. Kelas ini berisi berbagai fungsi seperti:

      ▪ checkConnection() untuk mengecek apakah koneksi ke database berhasil atau
    tidak.

      ▪ addMahasiswa() untuk menambahkan data mahasiswa ke tabel.

      ▪ getAllMahasiswa() untuk menampilkan seluruh data mahasiswa.

      ▪ updateMahasiswa() untuk memperbarui data mahasiswa.

      ▪ deleteMahasiswa() untuk menghapus data mahasiswa.

      ▪ closeConnection() untuk menutup koneksi database ketika program selesai
    dijalankan.

• View
View merupakan bagian yang berhubungan langsung dengan pengguna.
Pada proyek ini, kelas MahasiswaView.java berfungsi sebagai antarmuka berbasis console
(terminal). Di dalamnya terdapat menu pilihan seperti menampilkan data mahasiswa,
menambah data, memperbarui data, menghapus data, mengecek koneksi database, dan keluar
dari program.
View juga berperan dalam menerima input dari pengguna (misalnya NPM, nama, semester,
IPK) dan menampilkan hasil keluaran dari Controller.

• Controller
Controller berfungsi sebagai pengatur alur antara Model dan View.
Pada proyek ini, kelas MahasiswaController.java menerima perintah dari pengguna melalui
View, kemudian mengatur logika dan memanggil fungsi dari Model untuk diproses. Setelah
data berhasil diolah, hasilnya dikembalikan ke View untuk ditampilkan.
Kelas ini juga berfungsi untuk menambah, menampilkan, memperbarui, dan menghapus data
mahasiswa, serta memeriksa koneksi database.
Dengan penerapan pola MVC ini, aplikasi menjadi lebih mudah dipahami karena setiap
bagian memiliki fungsi yang terpisah dan tidak saling tumpang tindih.
