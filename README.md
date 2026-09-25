# 📈 Dashboard Sales Material Alam

Dashboard interaktif untuk memantau kinerja penjualan material alam (pasir, kerikil, batu kali) — dibangun di Excel dengan PivotTable, PivotChart, dan slicer, mencakup pembersihan data dan koreksi bug sebelum insight final diambil.

![Preview Dashboard](assets/dashboard_preview.png)
> ⚠️ Gambar di atas hasil render otomatis dan belum sepenuhnya rapi (judul terpotong, 1 chart belum tampil, slicer tidak ikut ter-render). Ganti dengan screenshot langsung dari Excel sebelum publish — hasilnya akan jauh lebih rapi karena semua elemen (termasuk slicer) tampil normal di Excel.

---

## 🎯 Ringkasan

Dashboard ini melacak 3 KPI utama dari transaksi penjualan material alam periode Januari–Juli 2025:

| KPI | Nilai |
|---|---|
| Total Pembelian | Rp 2.061.800.000 |
| Total Penjualan | Rp 2.937.900.000 |
| Total Laba | Rp 876.100.000 |

Dilengkapi breakdown per **Sales**, per **Material**, dan **tren bulanan**, plus slicer untuk filter interaktif.

---

## 🧹 Proses Data Cleaning (bagian penting dari proyek ini)

Sebelum insight diambil, dilakukan verifikasi terhadap data mentah dan ditemukan dua masalah:

**1. Outlier / kesalahan input data**
Satu baris transaksi (31 Juli, Batu Kali) tercatat dengan Volume **5.000** unit — jauh di atas rata-rata transaksi lain (40-90 unit). Baris ini sendirian menyumbang ~32% dari total laba yang tercatat, dan setelah diverifikasi dianggap sebagai kesalahan input, sehingga dikeluarkan dari perhitungan.

**2. Pivot table belum di-refresh (data stale)**
Sebagai akibatnya, angka pada dashboard versi awal tidak sinkron dengan data transaksi yang ada — pivot table menampilkan angka dari kondisi data yang sudah usang. Setelah dikoreksi ulang berdasarkan data transaksi aktual (minus outlier), seluruh KPI, tabel, dan chart disesuaikan agar konsisten.

**3. Bug pada pie chart "Total Laba per Sales"**
Chart ini awalnya ikut memasukkan baris "Grand Total" pivot sebagai salah satu slice — yang secara matematis akan selalu bernilai 50%, terlepas dari distribusi data yang sebenarnya. Sudah diperbaiki agar hanya menampilkan proporsi per sales (anto, Rudi, Tono).

---

## 🔍 Insight Setelah Data Dikoreksi

- **anto** adalah kontributor laba terbesar (Rp 636.850.000 — 73%), jauh di atas Rudi (19%) dan Tono (9%).
- **Batu Kali** adalah material dengan laba tertinggi (Rp 272.550.000), diikuti Pasir dan Kerikil yang relatif berimbang.
- Laba bulanan berkisar Rp 103–149 juta per bulan, dengan Juni sebagai bulan terbaik (Rp 148.750.000).

---

## 🛠️ Tools & Teknik

- **Excel PivotTable & PivotChart** — agregasi dan visualisasi per Sales, Material, dan Bulan
- **Slicer** — filter interaktif
- **Data validation** — deteksi outlier dengan membandingkan volume transaksi terhadap rata-rata

---

## 📁 Isi Repository

```
├── Dashboard_Sales_Material_Alam.xlsx   # file utama, buka sheet "Dashboard"
└── assets/
    └── dashboard_preview.png
```

📊 **[Buka dashboard interaktif (Excel)](Dashboard_Sales_Material_Alam.xlsx)**

---

## 📌 Catatan

Dataset merupakan data latihan dari program pelatihan data analytics. Proses cleaning, koreksi bug pivot/chart, dan penyusunan dashboard dikerjakan sendiri sebagai latihan penerapan analisis data end-to-end di Excel — termasuk proses verifikasi data yang tidak selalu terlihat di permukaan (stale pivot cache, outlier tersembunyi, bug chart).

---

**Dibuat oleh:** Lucky Chairul Fahsya
