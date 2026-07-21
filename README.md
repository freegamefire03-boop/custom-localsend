# Custom LocalSend

Fork of [LocalSend](https://github.com/localsend/localsend) with Android foreground service support — stays discoverable and can receive files even when the app is in the background or the screen is off.

## Status
Active development — foreground service implemented, building/testing.

## Features
- All original LocalSend features
- Android foreground service with persistent notification (prevents background kill)
- Installs as a separate app alongside the original LocalSend (`org.custom.localsend`)

## Tech Stack
- Flutter / Dart (UI)
- Rust (HTTP server via flutter_rust_bridge)
- Kotlin (Android platform layer — foreground service)

## Building
```bash
cd app
flutter pub get
flutter build apk --debug
```

APK output: `app/build/outputs/apk/debug/app-debug.apk`

## Changes from Upstream
- `applicationId` changed to `org.custom.localsend` (separate app)
- Android foreground service added (persistent notification while server runs)
- Notification permission requested on Android 13+
- App label: "Custom LocalSend"

## Known Issues / TODO
- [x] Fork/clone upstream source
- [x] Change app identity (separate from original)
- [x] Add Android foreground service (Kotlin)
- [x] Start/stop service with HTTP server lifecycle
- [ ] Build and test custom APK
- [ ] Auto-install via LocalSend CLI to phone
