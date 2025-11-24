# Little Lemon App

Deskripsi
---------
Little Lemon adalah contoh aplikasi iOS (SwiftUI) yang menampilkan desain dan gaya UI untuk studi atau demo. Proyek ini berisi komponen SwiftUI, Core Data (PersistenceController), dan style (Styles.swift).

Prasyarat
---------
- macOS dengan Xcode (disarankan versi terbaru)
- Command Line Tools (xcode-select --install)
- Simulator iOS (mis. iPhone 16 Pro Max)

Menjalankan aplikasi (via Xcode)
--------------------------------
1. Buka Xcode:
   ```
   open LittleLemonApp.xcodeproj
   ```
   Jika proyek menggunakan workspace, buka `*.xcworkspace`.
2. Pilih target scheme `LittleLemonApp` dan pilih simulator (mis. iPhone 16 Pro Max).
3. Tekan tombol Run (ikon ▶️) atau ⌘R.

Menjalankan aplikasi (via Terminal)
----------------------------------
Contoh build & pasang ke simulator (sesuaikan scheme/workspace bila perlu):

```bash
cd /Users/alvinahmad/Downloads/little-lemon-app-main/LittleLemonApp

# boot simulator jika perlu
xcrun simctl boot "iPhone 16 Pro Max"

# build (ganti -project dengan -workspace jika perlu)
xcodebuild -project LittleLemonApp.xcodeproj -scheme LittleLemonApp \
  -destination 'platform=iOS Simulator,name=iPhone 16 Pro Max' \
  -derivedDataPath build clean build

# instal dan jalankan
xcrun simctl install booted build/Build/Products/Debug-iphonesimulator/LittleLemonApp.app
# ganti bundle id jika perlu (lihat Info.plist -> Bundle Identifier)
xcrun simctl launch booted com.your.bundle.id
```

Catatan
-------
- Jika Anda menjalankan file Swift tunggal (mis. Styles.swift) dari VS Code, itu tidak akan menjalankan aplikasi lengkap. Gunakan Xcode untuk membuild dan menjalankan app di simulator.
- Pastikan Bundle Identifier sesuai saat menggunakan simctl launch.

Struktur direktori (ringkasan)
------------------------------
- LittleLemonApp/        — sumber utama Xcode project
- LittleLemonApp.xcodeproj
- LittleLemonApp/Styles.swift
- ... lainnya
