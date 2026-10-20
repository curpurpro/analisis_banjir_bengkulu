# analisis_banjir_bengkulu

# Analisis Potensi Banjir Provinsi Bengkulu

Studi kasus **eksploratif** untuk memahami potensi banjir di Provinsi Bengkulu menggunakan data geospasial, Python, dan Google Earth Engine. Proyek ini adalah kelanjutan dari studi kasus materi kuliah tentang penerapan komputasi dan analisis data. Belum ada model prediksi banjir yang terlatih maupun validasi kuantitatif.

## Tujuan

- Melihat pola curah hujan harian dan bulanan Bengkulu tahun 2024.
- Memahami variasi elevasi dan membuat klasifikasi elevasi eksploratif.
- Memeriksa raster bahaya banjir InaRISK BNPB sebagai calon data pembanding.

## Sumber data

| Data | Sumber |
| --- | --- |
| Curah hujan harian | CHIRPS Daily (`UCSB-CHG/CHIRPS/DAILY`) |
| Elevasi | SRTM (`USGS/SRTMGL1_003`) |
| Batas provinsi | FAO GAUL 2025 level 1 (`FAO/GAUL/2025/level1`) |
| Bahaya banjir | [InaRISK BNPB](https://inarisk.bnpb.go.id/portal/) |

## Struktur repositori

| File | Isi |
| --- | --- |
| `analisis_banjir_bengkulu.ipynb` | Notebook Google Colab (seluruh analisis) |
| `data_curah_hujan_bengkulu_2024.csv` | Curah hujan harian rata-rata wilayah, 2024 |
| `luas_kelas_elevasi_bengkulu.csv` | Luas tiap kelas elevasi |
| `grafik_hujan_harian_2024.png` | Grafik hujan harian |
| `grafik_hujan_bulanan_2024.png` | Grafik hujan bulanan |
| `luas_kelas_elevasi.png` | Grafik luas kelas elevasi |
| `peta_elevasi_bengkulu.png` | Tangkapan layar peta elevasi |
| `requirements.txt` | Daftar pustaka Python |

## Cara menjalankan

1. Buka `analisis_banjir_bengkulu.ipynb` di Google Colab.
2. Jalankan sel secara berurutan dan login ke akun Google Earth Engine saat diminta.
3. Pada bagian 8, unggah file ZIP raster InaRISK yang diunduh dari portal BNPB.

## Hasil

> Isi setelah notebook dijalankan.

- Curah hujan 2024: *(bulan terbasah dan terkering, total bulanan)*
- Elevasi Bengkulu: *(minimum, maksimum, rata-rata dalam meter)*
- Luas kelas elevasi: *(rendah, sedang, tinggi dalam km² dan persen)*
- Raster InaRISK: *(cakupan terhadap Bengkulu, persen piksel NoData)*

## Keterbatasan

- Batas kelas elevasi (50 m dan 200 m) adalah asumsi eksploratif, bukan standar resmi bahaya banjir.
- Nilai bulanan curah hujan adalah jumlah estimasi rata-rata harian wilayah, bukan volume air total.
- Raster InaRISK yang digunakan hanya mencakup sekitar 1°×1° dan sebagian besar pikselnya NoData. Piksel NoData tidak berarti bebas banjir, dan arti nilainya belum dikonfirmasi dengan legenda BNPB.
- Analisis belum menyimpulkan wilayah mana yang paling berpotensi banjir.

