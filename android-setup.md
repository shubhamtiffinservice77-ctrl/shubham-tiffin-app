# Android App Setup Guide

## Prerequisites
- Node.js installed
- Android Studio installed
- JDK 11+ installed

## Steps to build Android APK

### 1. Install Capacitor CLI and dependencies
```bash
npm install -g @capacitor/cli
npm install @capacitor/core @capacitor/android
```

### 2. Initialize Android platform
```bash
npx cap init "Shubham Tiffin" "com.shubhamtiffin.app" --web-dir .
npx cap add android
```

### 3. Copy web files
```bash
npx cap copy
```

### 4. Open in Android Studio
```bash
npx cap open android
```

### 5. Build APK
- In Android Studio: Build → Build Bundle(s) / APK(s) → Build APK(s)
- APK will be at: `android/app/build/outputs/apk/debug/app-debug.apk`
- Install on device: `adb install android/app/build/outputs/apk/debug/app-debug.apk`

### For signed APK (Production)
1. Create keystore: 
   ```bash
   keytool -genkey -v -keystore release.keystore -keyalg RSA -keysize 2048 -validity 10000 -alias upload
   ```
2. In Android Studio: Build → Generate Signed Bundle / APK
3. Select keystore file and sign

## Troubleshooting
- If permissions error: Check Android SDK path in Android Studio
- Update gradle: `./gradlew wrapper --gradle-version=<latest>`
- Clear cache: `rm -rf android/.gradle`
