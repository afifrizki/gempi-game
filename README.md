# GEMPI – Android project

The game (www/index.html + bundled three.js) wrapped with Capacitor. It runs fully offline.

## Option A: build on your computer
Needs Node 18+, JDK 17 and Android Studio (or the Android SDK).

    npm install
    npx cap add android
    npx cap sync android
    cd android && ./gradlew assembleDebug

The APK is at android/app/build/outputs/apk/debug/app-debug.apk

## Option B: build online (no Android tools needed)
1. Create a GitHub repository and upload everything in this folder.
2. Open the Actions tab and run "Build APK" (it also runs on every push).
3. Download the gempi-apk artifact from the finished run.

## Install
Copy app-debug.apk to your phone and open it (allow "install unknown apps" when asked).
The debug APK is fine for personal use. For Google Play you need a signed release build (a keystore and ./gradlew bundleRelease).
