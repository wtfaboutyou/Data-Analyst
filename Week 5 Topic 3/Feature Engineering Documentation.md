# Feature Engineering Documentation

## Dataset
Dataset yang digunakan adalah `Clean Dataset v2.csv`, yaitu dataset mobil yang telah melalui proses cleaning.

## Feature Engineering

### 1. AVG_MPG
- **Kolom baru:** `AVG_MPG`
- **Kolom yang digunakan:** `CITY_MPG`, `HIGHWAY_MPG`
- **Rumus:** `(CITY_MPG + HIGHWAY_MPG) / 2`
- **Tujuan:** Menghasilkan nilai rata-rata konsumsi bahan bakar mobil berdasarkan penggunaan di dalam kota dan di jalan raya.
- **Contoh:** Jika `CITY_MPG = 21` dan `HIGHWAY_MPG = 27`, maka `AVG_MPG = 24`.

### 2. POWER_TO_WEIGHT
- **Kolom baru:** `POWER_TO_WEIGHT`
- **Kolom yang digunakan:** `HORSEPOWER`, `CURB_WEIGHT`
- **Rumus:** `HORSEPOWER / CURB_WEIGHT`
- **Tujuan:** Mengukur perbandingan tenaga mesin terhadap berat kendaraan. Nilai yang lebih tinggi menunjukkan tenaga mesin yang lebih besar relatif terhadap bobot kendaraan.
- **Contoh:** Jika `HORSEPOWER = 111` dan `CURB_WEIGHT = 2548`, maka `POWER_TO_WEIGHT ≈ 0.04356`.

## Hasil
Dataset final memiliki dua kolom tambahan:
- `AVG_MPG`
- `POWER_TO_WEIGHT`

Dataset kemudian disimpan sebagai `Final_Clean_Dataset.csv`.
