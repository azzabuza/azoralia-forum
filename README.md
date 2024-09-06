# Forum Diskusi Sederhana Berbasis Web

Ini adalah aplikasi forum diskusi berbasis web yang menggunakan **Firebase Realtime Database** untuk menyimpan dan menampilkan pesan dalam forum. Aplikasi ini memungkinkan pengguna untuk memposting thread diskusi dan menampilkan semua thread yang ada di halaman forum.

## Fitur Utama
- Pengguna dapat memposting thread baru.
- Pesan akan otomatis tersimpan di Firebase Realtime Database.
- Semua thread yang sudah diposting akan ditampilkan dalam forum secara real-time.
  
## Teknologi yang Digunakan
- **HTML5, CSS3**: Struktur dan tampilan antarmuka aplikasi.
- **JavaScript (ES6+)**: Logika aplikasi dan interaksi dengan Firebase.
- **Firebase**: Backend untuk autentikasi dan penyimpanan data.
  - **Firebase Authentication**: Mengautentikasi pengguna.
  - **Firebase Realtime Database**: Menyimpan thread yang dikirimkan pengguna.

## Prasyarat
Sebelum memulai instalasi, pastikan Anda sudah memiliki:
- Akun **Firebase** dan sudah membuat **Firebase Project**.
- File **Firebase Config** (berisi `apiKey`, `authDomain`, `projectId`, dll.) yang akan digunakan dalam aplikasi.

## Instalasi

1. **Kloning Repositori**
   ```bash
   git clone https://github.com/azzabuza/azoralia-forum.git
   cd azoralia-forum
   ```

2. **Inisialisasi Firebase Project**
   - Buka [Firebase Console](https://console.firebase.google.com/).
   - Buat project baru di Firebase.
   - Aktifkan **Firebase Authentication** dengan metode login menggunakan akun **Google**.
   - Aktifkan **Realtime Database** dengan mode **Test Mode** untuk kemudahan pengembangan awal.
   - Salin konfigurasi Firebase yang berisi informasi seperti `apiKey`, `authDomain`, dan lainnya.

3. **Konfigurasi Firebase**
   - Buka file `index.html`.
   - Pada bagian `firebaseConfig`, masukkan konfigurasi Firebase Anda:
     ```javascript
     const firebaseConfig = {
         apiKey: "your-api-key",
         authDomain: "your-auth-domain",
         projectId: "your-project-id",
         storageBucket: "your-storage-bucket"
     };
     ```

4. **Jalankan Aplikasi**
   - Untuk menjalankan aplikasi secara lokal, cukup buka file `index.html` di browser.
   - Anda bisa menggunakan **Live Server** di Visual Studio Code atau langsung membuka file tersebut dengan klik dua kali.

5. **Deploy ke Hosting**
   - Anda bisa menggunakan platform hosting seperti **Netlify** atau **Vercel** untuk mendepoy aplikasi ini.
   - Jika menggunakan **Firebase Hosting**, lakukan langkah berikut:
     - Instal **Firebase CLI**:
       ```bash
       npm install -g firebase-tools
       ```
     - Login ke akun Firebase:
       ```bash
       firebase login
       ```
     - Inisialisasi Firebase Hosting:
       ```bash
       firebase init
       ```
     - Deploy aplikasi:
       ```bash
       firebase deploy
       ```

## Struktur Direktori

```
.
├── index.html       # Halaman utama forum
├── asset/           # Folder berisi gambar/icon yang digunakan di forum
└── README.md        # Dokumentasi aplikasi
```

## Kontribusi
Jika Anda ingin berkontribusi dalam pengembangan proyek ini, silakan fork repositori dan kirimkan pull request. Kami menerima kontribusi berupa penambahan fitur, perbaikan bug, atau peningkatan performa.

## Lisensi
Aplikasi ini dirilis di bawah lisensi MIT. Silakan lihat file `LICENSE` untuk informasi lebih lanjut.
