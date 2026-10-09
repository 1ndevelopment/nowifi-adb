# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.8] - 2026-10-08

### Fixed

- Wireless debugging toggle no longer flips back off on ROMs whose
  `verifyWifiNetwork` overload differs (e.g. Samsung Android 16 builds): every
  overload is now hooked by name instead of one exact signature, with an
  `adb_wifi_enabled=0` guard as a fallback.

### Changed

- Install docs now target KernelSU + Zygisk Next (Magisk still supported; the
  module is root-agnostic).

## [1.1.7] - 2026-09-28

### Fixed

- Fixed IP toggle now pins `127.0.0.1` in No-WiFi mode (no hotspot) instead of
  showing the general remote IP (`10.x.x.x` / carrier-NAT). Hotspot mode still
  pins `192.168.49.1`.

## [1.2.0] - 2026-07-10

### Added

- Android 16 QPR1 support.

### Fixed

- Hardened all hooks against methods removed or renamed on newer ROMs.

## [1.1.0] - 2026-04-17

### Added

- Added "Fixed IP/port" toggle on the Wireless Debugging screen to listen on `192.168.49.1:5555`.

### Fixed

- Various UI sync and lifecycle issues on Settings screens.

## [1.0.2] - 2026-04-12

### Added

- Added support for Android 16.

## [1.0.1] - 2026-04-10

### Fixed

- Fixed wrong IP shown on Wireless Debugging screen when hotspot is active.
- Fixed button label not updating on hotspot/Wi-Fi state changes.

## [1.0.0] - 2026-04-09

Initial release.

[1.2.0]: https://github.com/droserasprout/io.drsr.hotspotadb/compare/1.1.0...1.2.0
[1.1.0]: https://github.com/droserasprout/io.drsr.hotspotadb/compare/1.0.2...1.1.0
[1.0.2]: https://github.com/droserasprout/io.drsr.hotspotadb/compare/1.0.1...1.0.2
[1.0.1]: https://github.com/droserasprout/io.drsr.hotspotadb/compare/1.0.0...1.0.1
[1.0.0]: https://github.com/droserasprout/io.drsr.hotspotadb/releases/tag/1.0.0
