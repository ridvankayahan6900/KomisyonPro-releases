# KomisyonPro Release Dağıtım

Bu özel repo KomisyonPro Android APK'larını host eder.

- `app_meta.json` → in-app updater bu dosyayı okuyup yeni sürüm var mı diye kontrol eder.
- Releases sekmesi → her sürüm için APK dosyası.

## Yeni sürüm yayınlama

```bash
cd /d/app/KomisyonPro
./gradlew.bat assembleDebug
gh release create v0.X.Y app/build/outputs/apk/debug/app-debug.apk \
  --title "vX.Y.Z" --notes "Sürüm notları..."
```

Sonra `app_meta.json`'u versiyon ile güncelle ve commit et.
