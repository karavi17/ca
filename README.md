# TECHI APK — Student App

This is an Android Studio/Gradle project for the TECHI StudyClass student app.

## What is included
- Existing StudyClass student HTML UI packaged as an Android WebView app.
- Room-code connection.
- Configurable WebSocket server address on the connect screen.
- Camera/microphone permission handling for future WebRTC casting.
- File chooser support for the existing HTML app.
- Local WebSocket (`ws://`) support for same-Wi-Fi PC testing.

## Build without Android Studio
1. Upload this folder to a GitHub repository.
2. Push the included `.github/workflows/build-apk.yml`.
3. GitHub Actions builds `app-debug.apk`.
4. Download the APK from the workflow artifact.

## Important
The current mobile HTML source contains the existing whiteboard/PDF/student drawing logic. The Python PC server and teacher app are separate. For live screen CAST/UNCAST, the WebRTC signaling logic must be connected on both teacher and student sides; this package prepares the Android WebView and permissions but does not pretend that the old WebSocket-only student code already contains full WebRTC playback.
