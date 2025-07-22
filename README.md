# 📸 Photo Renamer Based on GIS — Automate Your Field Photos!

Punya ribuan foto lapangan tapi nama filenya masih kayak `IMG_20250626_101433.jpg`?  
Kalau udah punya shapefile & data GPS di EXIF, kenapa gak langsung rename otomatis aja?

Inilah script Python yang gua pake bareng tim buat rapihin semua foto survei lapangan berdasarkan lokasi jalan terdekat — pakai data dari shapefile!

---

## 🚀 Fitur Utama

✅ Baca koordinat GPS langsung dari EXIF foto  
✅ Proyeksikan titik ke UTM biar spatial join lebih presisi  
✅ Cari garis (LineString) terdekat dari shapefile (biasanya jaringan jalan)  
✅ Rename foto otomatis sesuai atribut `Alamat` dari shapefile  
✅ Tambah suffix angka kalau ada nama duplikat  

---

## 💡 Studi Kasus Nyata

Sebelumnya nama foto kayak gini:

Kampung Rawa_20250626_102139002.jpg


Setelah diproses:

Gg._Gabus_1.1_3.jpg


✨ Hasilnya: semua foto langsung terorganisir berdasarkan lokasi jalan terdekat.  
Siap dipakai buat pelaporan, dashboard WebGIS, atau dokumentasi lokasi.

---

## 🧰 Tools yang Dipakai

- Python 3.x  
- [GeoPandas](https://geopandas.org/)  
- [Shapely](https://shapely.readthedocs.io/)  
- [ExifRead](https://pypi.org/project/ExifRead/)  
- [QGIS](https://qgis.org/) (buat ngecek shapefile & koordinat lapangan)

---

## 📁 Struktur Folder

photo-renamer-gis/
├── photos/ # Foto hasil survei (format .jpg)
├── shapefile/ # Data shapefile (.shp, .dbf, .shx, dll)
├── scripts/
│ └── rename_photos.py # Script utama buat rename
├── requirements.txt # Daftar pustaka Python
└── README.md # Ini file-nya


---

## ⚙️ Cara Pakai

1. **Install dependensi:**

```bash
pip install -r requirements.txt

    Edit path di script rename_photos.py sesuai folder kamu:

shapefile_path = "shapefile/KampungRawaLine_CIP.shp"
folder_foto = "photos"

    Jalankan:

python scripts/rename_photos.py

    Hasilnya: Foto-foto langsung berubah nama sesuai lokasi Alamat dari shapefile!

🔍 Requirements

geopandas
shapely
exifread

Versi Python yang dipakai: 3.10+
Pastikan shapefile kamu punya geometri LineString dan kolom Alamat.
👨‍💻 Buat Siapa Ini?

    Surveyor lapangan

    Anak GIS yang sering kerja bareng tim pemetaan

    GIS Developer yang butuh data terstruktur buat WebGIS

    Freelancer GIS yang kerjaan-nya “rapihin data klien” 😅

💬 Kenapa Gue Bikin Ini?

Gue kerja di bidang GIS, dan udah beberapa kali hadapi ribuan foto hasil survei yang namanya gak jelas.
Daripada rename manual satu-satu, mending automasi aja pake script dan shapefile.
Cepet, akurat, dan bisa dipakai ulang buat proyek lain.
🙌 Kontribusi?

    Punya ide buat support Point shapefile?

    Mau tambahin GUI kecil?

    Punya cara parsing EXIF lebih efisien?

Pull Request & feedback sangat welcome!
📫 Kontak

    LinkedIn: Nama Kamu

    GitHub: @yourusername
