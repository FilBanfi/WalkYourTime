# 🦌 WalkYourTime

**Walk to earn your screen time.**

WalkYourTime converts your daily steps into screen time minutes. Once your earned time runs out, the apps you choose get blocked — until you walk more. No account, no server, no tracking. Everything stays on your device.

---

## Download

![Version](https://img.shields.io/badge/version-1.0%20Antilope-blue)
![License](https://img.shields.io/badge/license-GPL%20v3-green)
![Min SDK](https://img.shields.io/badge/minSdk-26-orange)
![Platform](https://img.shields.io/badge/platform-Android-brightgreen)

[Google Play Store](https://play.google.com/store/apps/details?id=com.filbanfi.walkyourtime)
<br>
[GitHub](https://github.com/FilBanfi/WalkYourTime/releases/latest)

<!-- [Samsung Galaxy Store]() -->
<!-- [Amazon Appstore]() -->
<!-- [F-Droid]() -->
<!-- [APK (latest release)](https://github.com/FilBanfi/WalkYourTime/releases/latest) -->

---

## How it works

1. WalkYourTime counts your steps in the background via the built-in step counter sensor.
2. Steps are converted into screen time minutes based on a ratio you set (default: 100 steps = 1 minute).
3. When your earned time runs out, selected apps are blocked via Android Accessibility Service.
4. Walk more to unlock more time.

---

## Screenshots

| | | |
|:---:|:---:|:---:|
| <img src="https://play-lh.googleusercontent.com/7OLxNfRrg6gVY2lazGanjpr-wSfovKpV15tOMpeF_D6_5IkLRufHoDq2mS3aBf36apI2UyAtlcewychqj9OEbw=w2560-h1440-rw" width="220"/> | <img src="https://play-lh.googleusercontent.com/3nmQ_epsWvboLalarLGIrQmcm7HgiD3oTzWugfk3k95Mx-kEwhVhb8rc6X53S3HppD8wUSmMmY-h1u1lal_2B2Y=w2560-h1440-rw" width="220"/> | <img src="https://play-lh.googleusercontent.com/p-13sbNMs4enhHFtxVtG-iTPLW7jW_N1rS16Gim7t_2fEIZ4k9D9xMw6tJ58v3UVE6wMSuSuURCqu_JbDq3gKA=w2560-h1440-rw" width="220"/> |
| <img src="https://play-lh.googleusercontent.com/HDe8mgFcgvGV6LD_SaG1hL37SDB1NVNdMZoav4Y3Jvk6HJi3-89_3PDC8DZ1y8s08mzH5PlT-V89o2d3tc73SA=w2560-h1440-rw" width="220"/> | <img src="https://play-lh.googleusercontent.com/MDTWLtaDV9leEJs8Yhuh0QVYByRYRfKTln842BxFlPrnRZzRPrFlJdu6RFFSkdv_CRvEd10XJtBD0ISTdjqJwQ=w2560-h1440-rw" width="220"/> | <img src="https://play-lh.googleusercontent.com/aF1LavaWmcEFhYQ2d3jVoNk6qZ4dSezbVtqUQkkUAoppg1ZF_5oW5wjZCfYioQnSrt4nN5BikmAk4JJoZJOY=w2560-h1440-rw" width="220"/> |

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
