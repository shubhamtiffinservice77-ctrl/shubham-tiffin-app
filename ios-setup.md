# iOS App Setup Guide

## Prerequisites
- Mac with Xcode installed
- Node.js installed
- CocoaPods installed: `sudo gem install cocoapods`

## Steps to build iOS App

### 1. Install Capacitor CLI and dependencies
```bash
npm install -g @capacitor/cli
npm install @capacitor/core @capacitor/ios
```

### 2. Initialize iOS platform
```bash
npx cap init "Shubham Tiffin" "com.shubhamtiffin.app" --web-dir .
npx cap add ios
```

### 3. Copy web files
```bash
npx cap copy
```

### 4. Open in Xcode
```bash
npx cap open ios
```

### 5. Build and Run
- Select target device/simulator
- Press Play or: Product → Run
- App will launch on simulator/device

### For App Store Submission
1. Set Bundle ID in Xcode: com.shubhamtiffin.app
2. Add app icons (1024x1024)
3. Product → Archive
4. Upload to App Store Connect
5. Submit for review

## Troubleshooting
- Pod install error: `cd ios && pod install && cd ..`
- Clear build: `Product → Clean Build Folder`
- Update pods: `cd ios && pod update && cd ..`
