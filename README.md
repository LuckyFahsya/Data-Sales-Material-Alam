# 📈 Dashboard Sales Material Alam

Dashboard penjualan interaktif di Microsoft Excel (PivotTable, PivotChart, slicer, dan timeline) untuk memantau pembelian, penjualan, dan laba material alam.

> **Catatan:** ini adalah proyek latihan. Dataset dan desain dashboard mengikuti tutorial YouTube; saya membangunnya ulang sendiri untuk mempraktikkan PivotTable, PivotChart, dan slicer di Excel.

<img width="1361" height="663" alt="Dashboard_View" src="https://github.com/user-attachments/assets/626a9d3c-354b-4608-8f5e-17ab680a07cb" />


---

## 📊 Isi Dashboard

- **KPI card:** Total Pembelian, Total Penjualan, dan Total Laba
- **Volume per material:** Batu Kali, Kerikil, Pasir
- **Laba per sales:** anto, Rudi, Tono
- **Laba per material:** perbandingan pembelian, penjualan, dan laba
- **Tren laba per bulan:** periode Januari–Juli 2025
- **Filter interaktif:** slicer (Sumber Material, Material, Sales) dan timeline tanggal

## 🗂️ Dataset

Data transaksi penjualan material alam periode Januari–Juli 2025 dengan kolom: Tanggal, Sales, Sumber Material, Material, Volume, Harga Satuan Pembelian, Total Pembelian, Harga Satuan Penjualan, Total Penjualan, dan Laba. Sumber material: Gunung Merapi, Magelang, dan Temanggung.

## 🛠️ Yang Dipraktikkan

- Membuat PivotTable dari tabel sumber dan menautkannya ke PivotChart
- Menampilkan KPI card dengan `GETPIVOTDATA`
- Menghubungkan slicer dan timeline ke beberapa pivot sekaligus
- Menguji alur pembaruan data: menambahkan record uji di tabel sumber, memastikan KPI card dan chart ter-update setelah **Refresh All**, lalu menghapus record uji tersebut

## 📁 Isi Repository

```
└── Dashboard_Sales_Material_Alam.xlsx   # buka sheet "Dashboard"
```

📊 **[Buka dashboard (Excel)](Dashboard_Sales_Material_Alam.xlsx)** — coba klik slicer untuk melihat angka dan chart berubah.

---

**Dibuat oleh:** Lucky Chairul Fahsya
