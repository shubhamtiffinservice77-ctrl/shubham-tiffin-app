# Shubham Tiffin Service - Complete App Setup

यह repository दोनों versions में उपलब्ध है:

## Version 1: PWA (Progressive Web App)
### क्या है?
- Browser में install होने वाला app
- Android और iPhone दोनों में काम करता है
- Offline भी काम करता है

### कैसे चलाएं?
```bash
npm install
npm run start
```
फिर browser में खोलें: `http://localhost:3000`

**Phone में install करने के लिए:**
- Chrome/Firefox में साइट खोलें
- Menu → "Install app" या "Add to home screen"
- Done! अब home screen पर app आ जाएगा

---

## Version 2: Android Native App
### क्या है?
- Real Android app (APK file)
- Google Play Store पर upload कर सकते हो
- Native Android performance

### कैसे बनाएं?
देखें: [android-setup.md](android-setup.md)

**Quick Steps:**
```bash
npm install -g @capacitor/cli
npm install @capacitor/core @capacitor/android
npx cap init "Shubham Tiffin" "com.shubhamtiffin.app" --web-dir .
npx cap add android
npx cap copy
npx cap open android
```
फिर Android Studio में Build → Build APK(s)

---

## Version 3: iOS Native App
### क्या है?
- Real iOS app (.ipa file)
- Apple App Store पर upload कर सकते हो
- Native iOS performance

### कैसे बनाएं?
देखें: [ios-setup.md](ios-setup.md)

**Quick Steps:**
```bash
npm install -g @capacitor/cli
npm install @capacitor/core @capacitor/ios
npx cap init "Shubham Tiffin" "com.shubhamtiffin.app" --web-dir .
npx cap add ios
npx cap copy
npx cap open ios
```
फिर Xcode में Product → Run

---

## कौन सा choose करें?

| Feature | PWA | Android | iOS |
|---------|-----|---------|-----|
| Installation | Easy (Browser) | APK file | App Store |
| Play Store | ❌ | ✅ | ❌ |
| App Store | ❌ | ❌ | ✅ |
| Offline | ✅ | ✅ | ✅ |
| Native Feel | ✅ | ✅✅ | ✅✅ |
| Setup Time | 5 min | 30 min | 1 hour (Mac needed) |
| Cost | Free | Free | $99/year |

**Recommendation:** PWA से शुरू करो, फिर Android/iOS बनाओ!

---

## Files Description
- `index.html` - Main app UI
- `manifest.json` - App metadata
- `service-worker.js` - Offline support
- `capacitor.config.json` - Capacitor configuration
- `package.json` - Project dependencies
