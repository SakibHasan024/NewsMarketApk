# NewsMarket

A beginner-friendly Flutter news reader that requests Bangladesh-focused
articles from the NewsData.io API.

## Run the app

1. Install Flutter and Android Studio with the Android SDK.
2. From this project folder, run `flutter pub get`.
3. Configure your NewsData.io API key as described below.
4. Connect an Android phone with USB debugging enabled or start an Android
   emulator, then run the `flutter run` command from the API-key section below.

## Configure your NewsData.io API key

Pass the key at build/run time; do not put it in source control:

```powershell
flutter run --dart-define=NEWSDATA_API_KEY=your_api_key
```

For a release APK, pass the same define to `flutter build apk --release`.
The app reads the key with `String.fromEnvironment`. A key included in a mobile
app can still be extracted from the built binary, so use a backend to protect
the key in a public production release.

## Check the project

- `flutter analyze` checks the Dart code.
- `flutter test` runs the model and home-screen tests.

The app shows an API-key setup error until a key is supplied. News articles
are loaded from NewsData.io; the project does not use a backend or a database.
