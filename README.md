# Hayati — initial Flutter MVP

This is an **early source-code prototype**, not the full 100-question specification and not a compiled APK. It implements basic daily task checklists, five-prayer checklists, a Quran daily checkbox and editable goal, three UI languages, light/dark mode, and local persistence using shared_preferences.

## Build prerequisites
Install Flutter SDK and Android SDK on your own machine, then from the project directory:

```bash
flutter create --platforms=android .
flutter pub get
flutter analyze
flutter test
flutter build apk --debug
```

The APK should then be at `build/app/outputs/flutter-apk/app-debug.apk` if compilation succeeds.

## Known limitations
- No APK was compiled or tested in the authoring environment (Flutter SDK unavailable).
- `shared_preferences` is only suitable for this small MVP; migrate to SQLite/Drift before expanding.
- Only current-day checklists are displayed; historical records are stored by date but historical UI and analytics are not yet implemented.
- No notifications, backup, full university/English/habit modules, widgets, or advanced privacy controls yet.
- The Quran goal text field is a prototype; its state and text-editing controller should be refactored before production.
- Date-based records use the device's local date.
