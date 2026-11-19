# Dhaka Downpour: Mind the Manhole (Android project)

A tiny WebView app that bundles the game (`app/src/main/assets/index.html`), so it runs fully offline.

## Easiest: build the APK in the cloud (no Android Studio)
1. Create a free GitHub account and a new empty repository.
2. Upload everything in this folder, including the hidden `.github` folder. If the uploader skips it, choose
   "Add file > Create new file", name it `.github/workflows/build-apk.yml`, and paste in `build-apk-workflow.yml`.
3. Open the repository's Actions tab, pick "Build APK", and press "Run workflow" (it also runs on every upload).
4. When the run turns green, open it and download `DhakaDownpour-apk` under Artifacts. Unzip it to get `app-debug.apk`.
5. Copy the APK to your phone and open it. Allow "Install unknown apps" for your file manager or browser when asked.

## Or: Android Studio
Open this folder, wait for Gradle sync, then Build > Build APK(s).
The file appears at `app/build/outputs/apk/debug/app-debug.apk`.

## Or: command line
With JDK 17, the Android SDK (platform 34) and Gradle 8.9 installed: `gradle assembleDebug`.

The APK is signed with Android's debug key, which is fine for installing on your own phone.
Publishing to Google Play needs a release key and a bundle (`gradle bundleRelease`).
