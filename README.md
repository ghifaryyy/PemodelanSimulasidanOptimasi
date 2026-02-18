# Agent-Based Simulation: Analisis Penggunaan Ruang Parkir Kampus

Proyek ini merupakan simulasi berbasis agen (Agent-Based Modeling) yang dikembangkan untuk menganalisis dinamika ketersediaan ruang parkir di lingkungan kampus Universitas Telkom. Simulasi ini memungkinkan analisis pengaruh jumlah kendaraan, durasi parkir, dan tata letak area terhadap efisiensi pencarian slot parkir secara realistis.
## 🛠️ Platform & Tools
* **Software:** NetLogo 6.x 
* **Metode:** Agent-Based Modeling (ABM) 
* **Visualisasi:** Real-time state visualization (Yellow: Entering, Orange: Searching, Green: Parked, Red: Leaving) 

## 🏗️ Desain Model
Model ini terdiri dari interaksi agen (kendaraan) dan lingkungan (patches) dengan karakteristik sebagai berikut:
* **Atribut Agen:** `parking-duration`, `search-time`, `target-patch`, dan `car-state`.
* **Atribut Lingkungan:** Slot parkir (Zona A/B/C), jalan, dan pintu masuk/keluar.
* **State Machine:** Alur perilaku agen mengikuti siklus `ENTERING` → `SEARCHING` → `PARKED` → `LEAVING`.

## ⚙️ Parameter Simulasi
Pengguna dapat mengatur variabel berikut melalui antarmuka NetLogo:
* **Arrival Rate:** Laju kedatangan kendaraan (1-50%).
* **Parking Duration:** Durasi parkir minimum dan maksimum (Ticks).
* **Extra Parking Area:** Toggle untuk mengaktifkan Zona C sebagai area tambahan (+40% kapasitas).

## 📊 Temuan Utama (Hasil Eksperimen)
Berdasarkan analisis data simulasi, diperoleh kesimpulan sebagai berikut:
1. **Dominansi Durasi:** Durasi parkir adalah faktor paling signifikan; kenaikan durasi 2x lipat menyebabkan okupansi naik 3x lipat dan waktu pencarian membengkak 102%.
2. **Saturasi Zona:** Peningkatan *arrival rate* dari 10% ke 50% menyebabkan Zona A mencapai saturasi (100%), yang mengakibatkan waktu pencarian meningkat.
3. **Paradoks Lokasi:** Penambahan Zona C terbukti **tidak efektif** (okupansi 0%) karena algoritma *nearest-first* memprioritaskan slot terdekat, membuktikan bahwa lokasi strategis lebih penting daripada kuantitas slot.

## 👥 Tim Penyusun
Mahasiswa S-1 Sains Data, Fakultas Informatika, Universitas Telkom:
* **Ghifary Wibisono** (103052400016)
* **Brama Hartoyo** (103052400030)
* **Prayata Yasinkha Adnien** (103052400060) 
* **Luthfia Maulidya Izzati** (103052400066) 

---
*Proyek ini disusun sebagai bagian dari tugas besar simulasi berbasis agen tahun 2025.*
