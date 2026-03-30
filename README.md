# 🦌 WalkYourTime

**Walk to earn your screen time.**

WalkYourTime converts your daily steps into screen time minutes. Once your earned time runs out, the apps you choose get blocked — until you walk more. No account, no server, no tracking. Everything stays on your device.

---

## Download

[Google Play Store](https://play.google.com/store/apps/details?id=com.filbanfi.walkyourtime)

<!-- [Samsung Galaxy Store]() -->
<!-- [Amazon Appstore]() -->
<!-- [F-Droid]() -->
<!-- [APK (latest release)](https://github.com/FilBanfi/WalkYourTime/releases/latest) -->

![Version](https://img.shields.io/badge/version-1.0%20Antilope-blue)
![License](https://img.shields.io/badge/license-GPL%20v3-green)
![Min SDK](https://img.shields.io/badge/minSdk-26-orange)
![Platform](https://img.shields.io/badge/platform-Android-brightgreen)

---

## How it works

1. WalkYourTime counts your steps in the background via the built-in step counter sensor.
2. Steps are converted into screen time minutes based on a ratio you set (default: 100 steps = 1 minute).
3. When your earned time runs out, selected apps are blocked via Android Accessibility Service.
4. Walk more to unlock more time.

---

## Screenshots

<!-- Add screenshots once available -->
<!-- ![Home](screenshots/home.png) -->
<!-- ![Blocked](screenshots/blocked.png) -->
<!-- ![Onboarding](screenshots/onboarding.png) -->

---

## Features

- Step-to-screen-time conversion with customizable ratio
- App blocking via Accessibility Service
- Monet dynamic theming — 8 color seeds × light/dark (Material You, API 31+)
- 30+ language localizations
- Fully offline and privacy-first — no account, no network calls
- Foreground step counter service with battery optimization exemption

---

## Roadmap

| Status | Feature |
|---|---|
| ✅ 1.0 | Core step counting and app blocking |
| ✅ 1.0 | Monet theming, 30+ localizations |
| ✅ 1.0 | Onboarding flow |
| 🔜 1.1 | Onboarding screens refinement |
| 🔜 1.1 | Dynamic system app exclusion list for blocking |
| 🔜 1.1 | Credits screen |
| 🔜 Future | Health Connect integration |
| 🔜 Future | Garmin Connect integration |
| 🔜 Future | Huawei Health integration |
| 🔜 Future | Room database (replacing SharedPreferences) |
| 🔜 Future | Home screen widget |

---

## Building from source

1. Download the source ZIP from the [latest release](https://github.com/FilBanfi/WalkYourTime/releases/latest)
2. Extract the archive
3. Open the project in Android Studio (Ladybug or later recommended)
4. Let Gradle sync complete
5. Build → **Generate Signed Bundle/APK** for a release build, or just **Run** for a debug build

No additional setup required — there are no API keys, no external services, no secrets.

---

## Project structure

```
WalkYourTime/
├── app/
│   └── src/main/
│       ├── AndroidManifest.xml
│       ├── ic_launcher-playstore.png
│       ├── java/com/filbanfi/walkyourtime/
│       │   ├── App.kt
│       │   ├── BlockedActivity.kt
│       │   ├── MainActivity.kt
│       │   ├── NotificationActionReceiver.kt
│       │   ├── OnboardingActivity.kt
│       │   ├── PrefsKeys.kt
│       │   ├── ScreenTimeAccessibilityService.kt
│       │   ├── SettingsActivity.kt
│       │   ├── StepCounterService.kt
│       │   └── ui/
│       │       ├── blocked/
│       │       │   └── BlockedScreen.kt
│       │       ├── main/
│       │       │   └── WalkYourTimeScreen.kt
│       │       ├── onboarding/
│       │       │   ├── OnboardingRouter.kt
│       │       │   └── OnboardingScreens.kt
│       │       ├── settings/
│       │       │   └── SettingsScreen.kt
│       │       └── theme/
│       │           ├── Theme.kt
│       │           └── Type.kt
│       └── res/
│           ├── drawable/
│           │   ├── blocked_hero.xml
│           │   ├── main_hero.xml
│           │   ├── onboarding_accessibility_hero.xml
│           │   ├── onboarding_battery_hero.xml
│           │   ├── onboarding_notification_hero.xml
│           │   ├── onboarding_privacy_hero.xml
│           │   ├── onboarding_ready_hero.xml
│           │   ├── onboarding_steps_hero.xml
│           │   ├── onboarding_welcome_hero.xml
│           │   └── ic_launcher_foreground.xml
│           ├── font/
│           │   └── google_sans_flex.ttf
│           ├── mipmap-*/           # Launcher icons (all densities)
│           ├── values/
│           │   ├── ic_launcher_background.xml
│           │   ├── strings.xml
│           │   └── themes.xml
│           ├── values-*/           # 30+ locale string files
│           └── xml/
│               └── accessibility_service_config.xml
├── PRIVACY.md
├── LICENSE
└── README.md
```

---

## Contributing

Contributions are welcome. Before opening a pull request, please open an issue first to discuss what you want to change — especially for features, as the roadmap is actively managed.

Bug fixes and localization improvements are always appreciated.

By contributing you agree that your code will be distributed under the [GPL v3 license](LICENSE).

---

## Privacy

WalkYourTime collects no data. Full privacy policy: [PRIVACY.md](PRIVACY.md)

---

## License

[GNU General Public License v3.0](LICENSE) — © 2026 FilBanfi
