# Manajemen State di Flutter: Perbandingan

Repository ini berisi dua proyek yang mendemonstrasikan:
1. **Ephemeral State Management** menggunakan `StatefulWidget`.
2. **App State Management** menggunakan package `scoped_model`.

## Observasi
### Ephemeral State Management:
- **Definisi**: Pengelolaan state lokal di dalam satu widget atau layar.
- **Kelebihan**:
  - Sederhana untuk diimplementasikan.
  - Cocok untuk kasus yang tidak membutuhkan pengelolaan state di luar widget itu sendiri.
- **Kekurangan**:
  - Tidak bisa berbagi state antar widget atau layar.
  - Tidak efisien untuk aplikasi yang kompleks.

### App State Management:
- **Definisi**: Pengelolaan state secara global, sehingga dapat diakses oleh berbagai widget di seluruh aplikasi.
- **Kelebihan**:
  - Mempermudah berbagi state di seluruh aplikasi.
  - Cocok untuk aplikasi besar dan kompleks.
- **Kekurangan**:
  - Memerlukan konfigurasi tambahan, seperti penambahan package `scoped_model`.

## Kelebihan App State Management
1. **User Authentication**: Status login pengguna dapat digunakan di seluruh aplikasi tanpa perlu mengirim data dari satu widget ke widget lainnya.
2. **Keranjang Belanja**: Data keranjang belanja dapat diakses dan diperbarui di berbagai layar tanpa duplikasi kode.
3. **Pengaturan Global**: Mengelola preferensi pengguna seperti tema aplikasi, bahasa, atau notifikasi secara efisien.

## Kesimpulan
- **Ephemeral State Management** cocok untuk aplikasi sederhana atau state yang hanya relevan pada satu widget.
- **App State Management** sangat penting untuk membangun aplikasi Flutter yang skalabel dan mudah dikelola, terutama untuk kasus penggunaan yang kompleks, seperti autentikasi pengguna atau pengelolaan data yang digunakan di seluruh aplikasi.

## Cara Menjalankan Proyek
1. Clone repository ini ke perangkat Anda.
2. Buka masing-masing proyek di terminal:
   - Untuk `ephemeral_state_codelab`, jalankan:
     ```bash
     flutter run
     ```
   - Untuk `app_state_codelab`, jalankan:
     ```bash
     flutter run
     ```
3. Bandingkan perilaku state pada kedua proyek.

## Catatan Tambahan
- Untuk menggunakan `scoped_model`, pastikan menambahkan dependensi berikut di `pubspec.yaml`:
  ```yaml
  dependencies:
    scoped_model: ^2.0.0
