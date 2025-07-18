# shp_bbox_selat-bali
# Shapefile Bounding Box Selat Bali

`shp_bbox_selat_bali` merupakan *shapefile* yang berisi batas kotak pembatas (*bounding box*) wilayah Selat Bali. Shapefile ini digunakan untuk mendefinisikan area geografis yang mencakup wilayah perairan antara Pulau Bali dan Pulau Jawa bagian timur. Data ini biasanya dimanfaatkan sebagai referensi spasial untuk:

* Pemotongan (*clipping*) data vektor atau raster
* Analisis oseanografi
* Perencanaan konservasi laut
* Kajian wilayah pesisir dan laut di sekitar Selat Bali

## 📌 Informasi Umum

| Atribut | Keterangan |
|---------|------------|
| **Format** | Shapefile (`.shp`) |
| **Sistem Koordinat** | WGS 84 (EPSG:4326) |
| **Tipe Geometris** | Polygon (representasi kotak pembatas) |
| **Cakupan Wilayah** | Selat Bali dan sekitarnya, termasuk sebagian wilayah pesisir Bali timur dan Jawa timur bagian selatan |

## 🧾 Atribut Utama

| Nama Atribut | Deskripsi |
|--------------|-----------|
| `id` | ID unik area bounding box |
| `nama` | Nama wilayah (contoh: `"Selat Bali"`) |
| `xmin` | Koordinat batas minimum longitude (opsional) |
| `xmax` | Koordinat batas maksimum longitude (opsional) |
| `ymin` | Koordinat batas minimum latitude (opsional) |
| `ymax` | Koordinat batas maksimum latitude (opsional) |

## 📍 Kegunaan

* Menentukan batas analisis spasial di kawasan Selat Bali
* Menjadi dasar pemotongan (*masking*) data spasial lainnya
* Digunakan dalam aplikasi GIS untuk pemodelan, monitoring, atau analisis spasial di wilayah perairan Selat Bali

## 🗂️ File Structure

```
shp_bbox_selat_bali/
├── shp_bbox_selat_bali.shp        # File shapefile utama
├── shp_bbox_selat_bali.shx        # Index file
├── shp_bbox_selat_bali.dbf        # Database file (atribut)
├── shp_bbox_selat_bali.prj        # Projection file
└── README.md                      # Dokumentasi
```

## 🚀 Cara Penggunaan

### Python (dengan GeoPandas)
```python
import geopandas as gpd

# Membaca shapefile
bbox_selat_bali = gpd.read_file('shp_bbox_selat_bali.shp')

# Melihat informasi dasar
print(bbox_selat_bali.info())
print(bbox_selat_bali.head())

# Visualisasi sederhana
bbox_selat_bali.plot()
```

### R (dengan sf)
```r
library(sf)

# Membaca shapefile
bbox_selat_bali <- st_read("shp_bbox_selat_bali.shp")

# Melihat struktur data
str(bbox_selat_bali)
head(bbox_selat_bali)

# Visualisasi
plot(bbox_selat_bali)
```

### QGIS
1. Buka QGIS
2. Drag and drop file `shp_bbox_selat_bali.shp` ke dalam map canvas
3. File akan secara otomatis dimuat dengan sistem koordinat WGS 84

## 📄 Lisensi



## 🤝 Kontribusi

Silakan buat issue atau pull request jika Anda ingin berkontribusi pada pengembangan dataset ini.

## 📧 Kontak

[Ilham Habibullah]

---

*Dataset ini dibuat untuk keperluan penelitian dan analisis spasial di wilayah Selat Bali*
