# Changelog

All notable changes to this project are logged here, newest first.

## 2026-07-21
- Added: Android foreground service (LocalSendForegroundService.kt) with persistent notification
- Added: Foreground service automatically starts/stops with the HTTP server
- Added: Notification permission request for Android 13+
- Changed: `applicationId` to `org.custom.localsend` (installs alongside original)
- Changed: App label to "Custom LocalSend"
- Added: New MethodChannel handlers for service control
- Added: Project scaffolded from upstream v1.17.0
