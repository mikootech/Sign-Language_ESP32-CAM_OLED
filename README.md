🤟 Sign-Language_ESP32-CAM_OLED 📺
Deskripsi: Proyek untuk menerjemahkan bahasa isyarat menggunakan kamera ESP32-CAM dan menampilkan hasilnya ke layar OLED secara real-time.

🎯 Target & Tujuan Proyek
Proyek ini dibagi menjadi 3 target utama yang harus diselesaikan:

Pin Connection (Sambungan Perangkat Keras)

Menghubungkan pin ESP32-CAM ke Layar OLED (I2C).

Memastikan modul kamera OV2640 terpasang dengan benar dan mendapat suplai daya yang stabil.

Machine Learning (Pemrosesan Data)

Melakukan training model klasifikasi gambar untuk gerakan tangan (bahasa isyarat).

Mengonversi model menjadi format yang ringan (seperti TensorFlow Lite for Microcontrollers) agar bisa berjalan di ESP32.

Code ESP32 CAM (Pemrograman Perangkat)

Menulis kode program untuk mengambil frame gambar dari kamera.

Menjalankan inferensi model ML langsung di dalam chip ESP32.

Menampilkan teks hasil terjemahan ke layar OLED.

💻 Panduan Kerja untuk Peserta
Setiap peserta diwajibkan untuk mengikuti langkah-langkah di bawah ini untuk mengambil kode awal (clone) dan mengumpulkan hasil pekerjaan (push).

1. Langkah untuk Clone (Mengambil Proyek ke Laptop Anda)
Pastikan Anda sudah menginstal Git di perangkat Anda. Buka terminal atau Command Prompt (CMD), lalu jalankan perintah berikut secara berurutan:

Bash
# 1. Masuk ke direktori/folder tempat Anda ingin menyimpan proyek
cd nama-folder-anda

# 2. Clone repositori ini ke penyimpanan lokal Anda
git clone https://github.com/USERNAME/Sign-Language_ESP32-CAM_OLED.git

# 3. Masuk ke dalam folder proyek yang baru saja di-clone
cd Sign-Language_ESP32-CAM_OLED
2. Langkah Setelah Melakukan Perubahan / Koding
Setelah Anda menyelesaikan target (misal: menambahkan file kode, mengubah skema pin, atau memperbarui model), Anda harus membuat branch baru terlebih dahulu sebelum mengirimnya (opsional, tergantung alur kerja tim):

Bash
# Membuat dan pindah ke branch baru dengan nama Anda (contoh: tugas-jatmiko)
git checkout -b tugas-nama-anda
3. Langkah untuk Push (Mengirim Hasil Kerja ke Repositori)
Setelah file selesai diedit dan disimpan, jalankan perintah ini untuk mengirimkan perubahan Anda kembali ke GitHub:

Bash
# 1. Cek status file apa saja yang telah diubah
git status

# 2. Tambahkan semua file yang diubah ke dalam daftar persiapan
git add .

# 3. Buat catatan (commit) tentang apa yang telah Anda kerjakan
git commit -m "Menyelesaikan target nomor X: [Penjelasan singkat pekerjaan Anda]"

# 4. Kirim hasil pekerjaan Anda ke GitHub
# (Jika membuat branch baru, ganti 'main' dengan nama branch Anda)
git push origin tugas-nama-anda
🛠️ Persyaratan Sistem & Komponen
Hardware: ESP32-CAM, Kamera OV2640, Layar OLED I2C (SSD1306), FTDI Programmer, Kabel Jumper.

Software: Arduino IDE / PlatformIO, Git.
