# IRUDINI Custom Blocklist 🛡️

**IRUDINI Custom Blocklist** adalah daftar filter DNS kustom yang dirancang khusus untuk memblokir iklan operator seluler (Telkomsel & Indosat/IOH), pelacak perilaku (*trackers*), dan telemetri di Indonesia. Daftar ini dioptimalkan untuk penggunaan pada **AdGuard Home**, **Pi-hole**, atau aplikasi **AdGuard** (Android/iOS/Windows).

## 🚀 Fitur Utama
* **Anti-Operator Ads**: Memblokir injeksi iklan, pop-up, dan banner dari Telkomsel dan Indosat Ooredoo Hutchison (IOH).
* **Privacy Focused**: Menutup celah pelacakan dari pihak ketiga seperti CleverTap, MoEngage, Adjust, dan Appier yang sering tertanam di aplikasi operator.
* **Clean Experience**: Menghilangkan elemen promosi yang mengganggu di dalam aplikasi MyTelkomsel dan myIM3.
* **High Compatibility**: Menggunakan sintaks standar AdGuard DNS yang kompatibel dengan berbagai penyaring DNS modern.

## 📋 Cara Pemasangan

### 1. Menggunakan AdGuard Home (Rekomendasi)
1.  Buka Dashboard **AdGuard Home** Anda.
2.  Masuk ke menu **Filters** > **DNS blocklists**.
3.  Klik tombol **Add blocklist** > **Add a custom list**.
4.  Masukkan nama: `IRUDINI Custom Blocklist`.
5.  Masukkan URL Raw berikut:
    ```text
    [https://raw.githubusercontent.com/irudini88/DNS-filtering/main/IRUDINI_v1.txt](https://raw.githubusercontent.com/irudini88/DNS-filtering/main/IRUDINI_v1.txt)
    ```
6.  Klik **Save**.

### 2. Menggunakan Aplikasi AdGuard (Android/iOS)
1.  Buka **Settings** > **Content Blocking** > **Filters**.
2.  Pilih **Custom filters** > **Add custom filter**.
3.  Tempelkan URL Raw di atas dan klik **Subscribe**.

## 🛠️ Struktur Filter
Daftar ini mencakup beberapa kategori utama:
* **Telkomsel Advanced**: Domain iklan, API marketing, dan sistem injeksi tsel.me.
* **Indosat/IOH Extended**: Domain iklan im3, analytics moengage, dan infrastruktur IOH terbaru.
* **Third-Party Trackers**: SDK pelacak yang digunakan oleh operator untuk profil pengguna.
* **Global Trackers**: Pelacak umum yang sering muncul pada lalu lintas data di Indonesia.

## ⚠️ Catatan Penting
* **Clear Cache**: Setelah memasang filter ini, sangat disarankan untuk melakukan *Clear Cache* pada aplikasi MyTelkomsel atau myIM3 agar iklan lama yang tersimpan hilang.
* **Whitelist**: Jika Anda mengalami kendala saat login atau melakukan pembayaran, tambahkan pengecualian (`@@`) pada domain terkait di daftar aturan pengguna Anda.

## 🔄 Pembaruan
Daftar ini diperbarui secara berkala. Dengan instruksi `Checkperiod: 1d` di dalam file, sistem Anda akan otomatis mengambil pembaruan setiap 24 jam.
