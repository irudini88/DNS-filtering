# 🛡️ IRUDINI DNS Filter

**IRUDINI DNS Filter** adalah *blocklist* DNS kustom yang dirancang khusus untuk mengembalikan privasi pengguna internet di Indonesia dengan memblokir gangguan di level jaringan.

### Fokus Utama:
* 🔥 **ISP Ad Blocking**: Mematikan iklan injeksi dan promosi operator.
* 🧠 **Privacy First**: Menghentikan *tracking* & telemetri aplikasi.
* 🚫 **Clean UI**: Menghilangkan *banner* promo & *campaign* yang mengganggu.
* 🔒 **Hardened Network**: Meningkatkan keamanan privasi seluruh perangkat.

---

# 🚀 Fitur Utama

### 📡 Aggressive ISP Ad Blocking
Memblokir infrastruktur periklanan dari operator besar di Indonesia:
* **Telkomsel** (MyTelkomsel, by.U)
* **Indosat Ooredoo Hutchison** (IM3, IOH)
* **XL Axiata & AXIS**

> **Cakupan:** *Injected ads* dari ISP, *In-app ads*, serta *Banner & Pop-up* promosi.

### 🧠 Advanced Tracking Protection
Menutup celah pengumpulan data oleh:
* **SDK Tracking**: Adjust, Appier, CleverTap, MoEngage, dll.
* **Endpoint Analytics**: Jalur pengiriman data perilaku pengguna milik operator.
* **Behavioral Tracking**: Pemantauan aktivitas klik dan preferensi.

### 🌍 Global Tracking & Telemetry
Perlindungan tambahan terhadap pelacak global:
* Google Analytics & Ads.
* Facebook Tracking & Firebase Telemetry.
* *Monetization networks* & *Redirect networks*.

---

# 🏗️ Struktur Filter

Daftar ini disusun secara modular untuk memudahkan manajemen:
1.  **ISP Indonesia**: Domain spesifik Telkomsel, by.U, Indosat, dan XL/AXIS.
2.  **Tracking & Analytics**: Pemutusan jalur SDK pihak ketiga dan internal ISP.
3.  **Lokal Integrasi**: Menggabungkan kecerdasan filter dari komunitas ABPindo.
4.  **Extra Hardcore**: Pemblokiran *click tracker* dan domain monetisasi.

---

# 📦 Instalasi

## 🟢 AdGuard Home (Direkomendasikan)

1.  Buka Dashboard **AdGuard Home**.
2.  Navigasi ke menu: `Filters` → `DNS blocklists`.
3.  Klik tombol: `Add blocklist` → `Add a custom list`.
4.  Masukkan konfigurasi berikut:

    * **Name:** `IRUDINI DNS Filter`
    * **URL:** `https://raw.githubusercontent.com/irudini88/DNS-filtering/main/IRUDINI_v4.txt`

5.  Klik **Save** ✅.

---

## 📱 AdGuard Apps (Android/iOS)

1.  Buka **Settings** → **Content Blocking**.
2.  Pilih **Filters** → **Custom**.
3.  Tambahkan URL Raw di atas dan klik **Subscribe**.

---

# ⚠️ Catatan Penting

### 🔴 Mode Aggressive
Karena filter ini bekerja secara agresif, Anda mungkin akan menemui:
* Banner promo di aplikasi MyTelkomsel/myIM3 hilang (kotak kosong).
* Rekomendasi paket "khusus untukmu" mungkin tidak muncul.
* Beberapa fitur *reward* berbasis iklan tidak dapat diakses.

### 🟢 Cara Mengatasi Error (False Positive)
Jika ada fitur aplikasi yang tidak berfungsi, gunakan **Query Log** di AdGuard:
1.  Cari domain dengan status **Blocked** saat Anda membuka aplikasi.
2.  Jika domain tersebut penting (seperti jalur login), tambahkan aturan pengecualian:
    ```text
    @@||domain-penting.com^
    ```

---

# 🔒 Advanced Setup
Untuk hasil maksimal, jalankan AdGuard Home pada server **Debian** dan hubungkan melalui **Tailscale Exit Node**. Gunakan *firewall enforcement* agar semua trafik DNS dipaksa melewati AdGuard (Anti-Bypass).

> 🔥 **Misi:** *"Internet bersih tanpa intervensi ISP di Indonesia"*

---

# 🤝 Kontribusi & Dukungan
Ditemukan domain iklan baru atau *false positive*? Silakan ajukan melalui **Pull Request** atau **Issue**. 

Jika proyek ini membantu Anda, jangan lupa berikan ⭐ di repository ini!

**Author:** [IRUDINI Project](https://github.com/irudini88)
