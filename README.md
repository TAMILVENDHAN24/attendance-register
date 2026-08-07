# Attendance Register apps

The existing `index.html` remains the single source for the website, Android app, and Windows app.

## Windows desktop app

Run `npm install`, then use `npm run desktop:start` to test it or `npm run desktop:build` to create the portable Windows package.

The generated application can be launched from `dist/win-unpacked/Attendance Register.exe`.

## Android APK

Install JDK 17 and Android Studio with the Android SDK. Then run:

```powershell
npm install
npm run android:add # first time only
npm run android:build
```

The debug APK is created at `android/app/build/outputs/apk/debug/app-debug.apk`.

After changing `index.html`, run `npm run android:sync` before rebuilding the APK.

## Firebase sync

The app needs a browser or device connection to Firebase. Do not block `firestore.googleapis.com` with an ad blocker or privacy extension; otherwise changes can be saved only on the device and will not sync.
