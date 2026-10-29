# Cinephile

Cinephile is an Android app for discovering films and TV shows, building a
watchlist, and picking up where you left off.

This repository is the public release channel for the Android APK. The
application source is maintained separately.

## Download

**[Download the latest APK](https://github.com/GregoryAM-SP/Cinephile/releases/latest)**

Each release includes a universal `app-release.apk`.

| | |
|---|---|
| Platform | Android 7.0 (API 24) and newer |
| Package | `com.gregoryam.cinephile` |
| Signing | Cinephile release key |
| Updates | In-app from 1.1.1 onward |

## Install

1. Download `app-release.apk` from the latest release.
2. Open the downloaded file.
3. If Android blocks the install, allow installs from the app you used to open
   it (**Settings → Apps → Special access → Install unknown apps**), then try
   again.
4. Tap **Install**.

You do not need to uninstall an existing Cinephile install to update it. Android
keeps app data when the new APK uses the same package and signing key and a
higher version code.

## Updates

Cinephile 1.1.1 and later check this repository for new releases on launch. You
can also open **Settings → Chat & updates → Check for updates**.

The app downloads the APK and opens Android's installer. Confirm the install to
finish; your library, profiles, and sign-in are preserved.

- The first move from 1.1.0 to 1.1.1 is a one-time manual install because 1.1.0
  predates the in-app updater.
- Android requires a confirmation for sideloaded APKs. There is no silent
  installation outside Google Play.

## Releases

Releases are tagged `v<version>` (for example `v1.1.1`) and include the signed,
universal `app-release.apk`.

For maintainers:

- Bump `version` in the source `pubspec.yaml` and push a matching `v*` tag.
- Build, sign, and publish from the source repository; never upload a
  debug-signed APK.
- Keep the application id (`com.gregoryam.cinephile`) and signing key unchanged.
  Android treats a different key as a different app and refuses an in-place
  update.
- The tag and the app's version must match. A plain `v1.1.0` tag cannot update
  clients already on `1.1.0+3`; use `v1.1.1` or a `+build` tag.
- Release notes appear in the app's update drawer, so keep them short and
  user-facing.

## Verify

The APK is signed with the Cinephile release certificate. To verify a download:

```sh
apksigner verify --print-certs app-release.apk
```

Expected SHA-256:

```
90df9da64a4e3fe5e89e42a756b028b9e12cc453be5b55da609f1661e84f4a1c
```

## Community

- [Discord](https://discord.gg/YuwJ7WZtTW)
- [All releases](https://github.com/GregoryAM-SP/Cinephile/releases)
