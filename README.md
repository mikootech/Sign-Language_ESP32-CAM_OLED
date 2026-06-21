# 🤟 Sign-Language_ESP32-CAM_OLED 📺

> **Deskripsi:** Proyek Edge AIoT terintegrasi untuk mendeteksi dan menerjemahkan bahasa isyarat menggunakan kamera ESP32-CAM, memprosesnya dengan Machine Learning, dan menampilkan hasil inferensinya ke layar OLED secara *real-time*.

---

## 🎯 Target & Tujuan Pengembangan

Proyek ini dibagi menjadi 3 pilar utama arsitektur AIoT yang harus diselesaikan:

### 1. Perangkat Keras (Hardware Integration)
* **Pin Connection:** Konfigurasi interkoneksi bus I2C antara modul ESP32-CAM dengan Driver Layar OLED (SSD1306/SSH1106).
* **Power Management:** Memastikan stabilitas tegangan dan suplai arus untuk modul kamera OV2640 agar terhindar dari masalah *brownout* saat *booting* atau saat transmisi data.

### 2. Kecerdasan Buatan (Edge Machine Learning)
* **Model Training:** Proses pengumpulan dataset dan *training* model klasifikasi gambar untuk berbagai variasi gerakan tangan (bahasa isyarat).
* **Optimization:** Mengonversi model hasil *training* ke format yang sangat ringan (**TensorFlow Lite for Microcontrollers**) agar sanggup dieksekusi oleh memori SRAM ESP32 yang terbatas.

### 3. Pemrograman Sistem Embedded (Firmware Development)
* **Frame Capture:** Menulis *pipeline* untuk mengambil *frame* gambar mentah secara terus-menerus langsung dari sensor kamera.
* **On-Chip Inference:** Menjalankan beban kerja eksekusi model ML (inferensi) langsung di dalam prosesor internal *chip* ESP32 (*Edge Computing*).
* **Display Rendering:** Melakukan transmisi data karakter teks hasil konversi untuk ditampilkan pada panel OLED.

---

## 💻 Panduan Kolaborasi & Workflow Git

Setiap anggota tim **diwajibkan** untuk mengikuti standarisasi *workflow* repositori di bawah ini saat mengambil kode dasar (*cloning*) maupun saat mengirimkan hasil pembaruan (*pushing*).

### 📥 1. Prosedur Local Cloning
Gunakan Terminal, Git Bash, atau Command Prompt untuk mengunduh repositori proyek ke komputer/laptop lokal Anda:

```bash
# 1. Masuk ke direktori/folder kerja lokal Anda
cd nama-folder-anda

# 2. Unduh repositori resmi proyek dari GitHub
git clone [https://github.com/USERNAME/Sign-Language_ESP32-CAM_OLED.git](https://github.com/USERNAME/Sign-Language_ESP32-CAM_OLED.git)

# 3. Masuk ke dalam direktori repositori yang baru saja di-clone
cd Sign-Language_ESP32-CAM_OLED
```

### 🌿 2. Pembuatan Branch Baru (Wajib)
Sebelum menulis atau mengubah baris kode apa pun, buatlah *branch* baru yang sesuai dengan nama Anda sendiri untuk menjaga stabilitas kode utama (*main branch*):

```bash
# Membuat sekaligus berpindah ke branch kerja mandiri Anda
git checkout -b tugas-nama-anda
```

### 📤 3. Prosedur Commit & Push Kedalam Repositori
Setelah Anda menyelesaikan salah satu target pekerjaan, simpan perubahan tersebut dan kirimkan kembali ke GitHub dengan menjalankan perintah terstruktur berikut:

```bash
# 1. Cek status berkas/file apa saja yang telah mengalami modifikasi
git status

# 2. Tambahkan semua berkas yang diubah ke dalam staging area Git
git add .

# 3. Buat dokumentasi pesan commit yang jelas terkait tugas yang diselesaikan
git commit -m "Menyelesaikan target: [Penjelasan singkat pekerjaan Anda]"

# 4. Kirimkan hasil pekerjaan lokal Anda menuju upstream branch di GitHub
git push origin tugas-nama-anda
```

---

## 🛠️ Spesifikasi Kebutuhan Sistem & Komponen

* **Microcontroller:** ESP32-CAM Development Board
* **Camera Module:** Omnivision OV2640 Image Sensor
* **Display Panel:** 0.96" OLED Screen (Sistem Bus I2C / Driver SSD1306)
* **Hardware Tambahan:** FTDI Programmer (untuk *flashing* kode), Kabel Jumper, Breadboard.
* **Development Environment:** Arduino IDE / PlatformIO Ecosystem
* **Version Control:** Git Engine & GitHub Repository Container
