# 🌍 WebGIS Kerusakan Bangunan Pascagempa Flores M7,7
### Manggarai Timur – Analisis Terintegrasi RVS + Google Earth Engine

> **Demo langsung:** [Buka di GitHub Pages](https://username.github.io/webgis-gempa-flores)

---

## 🛰 Fitur Google Earth Engine (Baru)

| Analisis | Sensor | Produk |
|---|---|---|
| **Kehilangan Koherensi SAR** | Sentinel-1 C-band IW | ΔCoh pra–pasca gempa |
| **Damage Proxy Map (DPM)** | Sentinel-1 GRD | Peta kerusakan otomatis |
| **Perubahan NDVI** | Landsat-8/9 OLI | ΔNDVI vegetasi/tanah |
| **Deformasi Tanah InSAR** | Sentinel-1 SLC | Penurunan permukaan (cm) |
| **Shakemap Intensitas** | Simulasi BMKG/USGS | Zona MMI |

## 📦 Fitur Aplikasi

- 🗺 **Peta interaktif Leaflet** – titik bangunan RVS + overlay raster GEE
- 🔴 **Damage Proxy Map** – skor 0–1 dari SAR change detection
- 📡 **Koherensi Sentinel-1** – peta kehilangan koherensi VV polarisasi
- 🌿 **NDVI Landsat-8/9** – perbandingan vegetasi/tanah pra & pasca gempa
- 📐 **Deformasi InSAR** – visualisasi penurunan permukaan (DInSAR)
- 📊 **Moran's I** – autokorelasi spasial kerusakan
- ✅ **Confusion Matrix** – validasi SAR vs survei lapangan (RVS)
- 📥 **Ekspor CSV / GeoJSON** – unduh data terfilter
- 📂 **Muat CSV sendiri** – ganti data simulasi dengan data asli

## 🚀 Deploy ke GitHub Pages

### Cara 1: Upload Manual
1. Buat repository baru di GitHub (misal: `webgis-gempa-flores`)
2. Upload file `index.html` dan `README.md`
3. Masuk ke **Settings → Pages**
4. Source: **Deploy from a branch** → branch `main` → folder `/ (root)`
5. Klik **Save** → web langsung online dalam ~1 menit

### Cara 2: Git CLI
```bash
git init
git add .
git commit -m "feat: WebGIS Gempa Flores + GEE analysis"
git remote add origin https://github.com/USERNAME/webgis-gempa-flores.git
git push -u origin main
# Aktifkan GitHub Pages di Settings → Pages
```

## 🔑 Integrasi GEE Nyata

Untuk menggunakan data GEE yang sesungguhnya:

1. **Daftar akun GEE** (gratis): https://earthengine.google.com
2. Buka https://code.earthengine.google.com
3. Salin kode dari tab **"💻 Kode GEE"** di aplikasi
4. Ganti `roi` dengan batas wilayah studi kamu
5. Ekspor hasil ke Google Drive → unduh GeoTIFF
6. Konversi ke GeoJSON dengan QGIS atau `gdal_polygonize`
7. Muat ke aplikasi via tombol **"Muat CSV sendiri"**

## 📡 Pasangan Citra Sentinel-1

| Pra-gempa | Pasca-gempa | Baseline | Mode |
|---|---|---|---|
| 27 Jul 2026 | 20 Agt 2026 | 24 hari | IW/VV+VH |
| 03 Agt 2026 | 27 Agt 2026 | 24 hari | IW/VV+VH |

## 📚 Referensi

- Yun et al. (2015). Rapid Damage Mapping. *Science Advances*
- ESA Copernicus Sentinel-1 SAR C-band handbook
- USGS Landsat-8/9 Collection 2 Level-2 Science Product
- Leaflet.js v1.9.4 · © OpenStreetMap contributors

---

**Dibuat dengan:** HTML + JS + Leaflet · Google Earth Engine · Sentinel-1 · Landsat-8/9
