# NUcleus

An Android companion app for FAST-NUCES students. It shows your FLEX data (attendance, marks, GPA) in clean native screens, and **NUdge** sends you alerts when something needs your attention.

> **Student project. Not affiliated with, endorsed by, or connected to FAST-NUCES.**

## What it does

- **FLEX Wrapper (Release 0):** log in to FLEX inside the app and see your attendance, absences left, marks and GPA in organised screens. Plain FLEX is always one tap away.
- **FlexDOWN (Release 1):** a community status monitor for FLEX. NUdge sends a notification when FLEX goes down and when it comes back.
- **Events (Release 2):** campus and society events, with reminders.
- **More FLEX and polish (Release 3):** GPA projection, what-if calculators, extra screens chosen from a student survey.

## Privacy

- Your password is typed into FLEX's own login page inside a WebView. The app never reads, stores or sends it.
- In Release 0, your academic data stays on your phone. Nothing is uploaded.
- Later releases will only collect anonymous, minimal telemetry, and the app will say so plainly.
- We never use anyone else's account for testing.

## Tech stack

| Part | Tech |
| --- | --- |
| Mobile app | Flutter (Dart), Android |
| API and probe worker | Node.js, Express |
| Database | MongoDB |
| Status web page | React |
| Alerts | Firebase Cloud Messaging |
| CI and releases | GitHub Actions, GitHub Releases |

## Repository layout

```
NUcleus/
├── app/      Flutter app (Release 0 lives here)
├── server/   Express API and FLEX probe worker (Release 1)
├── web/      React status page (Release 1)
└── docs/     Project outline and design notes
```

## Status

Release 0 is in progress. Step 1 is a spike to confirm we can read the logged-in FLEX pages reliably.

## Install

Android only. APKs will be published on the [Releases](../../releases) page. Download the latest `.apk` and allow installs from your browser or file manager when Android asks.

## Getting started (development)

Requirements: Flutter SDK, Android Studio or a device with USB debugging, and Node.js 20+ for the server.

```bash
git clone https://github.com/NUcleus-FAST/NUcleus.git
cd NUcleus/app
flutter pub get
flutter run
```

Server and web setup instructions will be added when Release 1 starts.

## Contributing

- Work on a branch and open a pull request. No direct pushes to `main`.
- Every PR is reviewed by the other developer before merging.
- Don't commit secrets: signing keys, `key.properties`, `google-services.json`, `.env` files.

## Team

- [Umer](https://github.com/umerhassanbajwa)
- [Azhan Arif](https://github.com/azzhanarif)

## License

To be decided.
