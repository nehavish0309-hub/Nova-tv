# Nova TV Android wrapper project

This project packages the existing Nova TV web preview in a basic Android WebView app. It is **source code, not a compiled APK**.

## Build an APK
1. Open this project in Android Studio (JDK 17; Android SDK 35).
2. Wait for Gradle sync.
3. Choose **Build → Build APK(s)**.
4. The debug APK will be at `app/build/outputs/apk/debug/app-debug.apk`.

Alternatively, push this project to a GitHub repository and run **Actions → Build Nova TV APK**. Download the `NovaTV-debug-apk` artifact from the completed workflow.

## Important limitations
- Requires internet access because the app loads the existing Nova TV preview website.
- This is a WebView wrapper, not a fully native launcher.
- Input-source switching is not implemented and a web page cannot switch physical TV HDMI inputs.
- Fire TV may not allow third-party apps to replace the system home launcher. Test on your exact device.
- The APK built by this workflow is an unsigned-for-release debug APK; do not distribute it as a production release without a proper signing setup.
