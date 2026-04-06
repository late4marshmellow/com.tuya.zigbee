# 🏠 Universal Tuya Zigbee v5.12.3

> **287 drivers** · **11267+ fingerprints** · Updated 2026-04-06

Local-first Zigbee control for Tuya devices on Homey Pro — the most comprehensive Tuya app available.

## Install

**Stable:** [Homey App Store](https://homey.app/a/com.dlnraja.tuya.zigbee/) · **Test:** [Test Channel](https://homey.app/a/com.dlnraja.tuya.zigbee/test/) · **Source:** [GitHub](https://github.com/dlnraja/com.tuya.zigbee)

## What's New (v5.12.3)

Added support for Zbeacon smart plugs and TS110E dimmer switches, Enriched driver database with multiple new Tuya device variants, Fixed fingerprint casing regression to ensure reliable case-insensitive matching, Relaxed cluster matching logic to properly pair and communicate with Tuya-Bridge mode devices, Resolved driver fingerprint collisions that caused incorrect device assignments

## Supported Devices

| Category | Drivers | FPs |
|---|---|---|
| 🔌 Socket | 69 | 2506 |
| 💡 Light | 32 | 1258 |
| 📡 Sensor | 83 | 4689 |
| 🌡️ Thermostat | 21 | 912 |
| 🪟 Windowcoverings | 8 | 481 |
| 🔐 Lock | 5 | 69 |
| 🌀 Fan | 15 | 248 |
| 🔔 Doorbell | 2 | 24 |
| 🎮 Remote | 18 | 120 |
| 🔘 Button | 2 | 28 |
| 🔥 Heater | 4 | 36 |
| 🚗 Garagedoor | 3 | 36 |
| 📦 Other | 20 | 860 |

[Device Finder](https://dlnraja.github.io/com.tuya.zigbee/) — search by fingerprint

## Features

- **Tuya DP protocol** (0xEF00/TS0601) + **Standard ZCL** clusters
- Physical button detection · Virtual buttons · LED backlight control
- Energy monitoring (W/V/A) · Air quality sensors (CO₂/VOC/PM2.5/HCHO)
- Covers & curtains with tilt · TRVs · Dimmers · IR blasters
- Auto-configured settings · Diagnostic reports

## Changelog

<details><summary>Previous versions</summary>

**v5.12.2:** Added support for Zbeacon smart plugs and TS110E dimmer switches, Enriched driver database with multiple new Tuya device variants, Fixed fingerprint casing regression to ensure reliable case-insensitive matching, Relaxed cluster matching logic to properly pair and communicate with Tuya-Bridge mode devices, Resolved driver fingerprint collisions that caused incorrect device assignments

**v5.12.1:** Added support for Zbeacon plugs, TS110E dimmers, and multiple new device variants. Fixed Tuya-Bridge mode pairing, resolved driver fingerprint collisions, corrected hybrid flow card routing, and improved capability update stability.

**v5.12.0:** Major stabilization release: Integrated Parallel Bot Handler for faster maintenance, fixed eWeLink/SONOFF plug support (Issue #194), and resolved multi-gang capability mapping bugs.

**v5.11.208:** Added Zbeacon support and fixed fingerprint casing regression in Universal Tuya Zigbee app.

</details>

## Report a Bug

Open a [GitHub Issue](https://github.com/dlnraja/com.tuya.zigbee/issues/new) — please include your `_TZxxxx` fingerprint and `TSxxxx` model ID.

## ☕ Support the Project

This app is free and open-source. If it's useful to you, a small donation helps keep it going:

**PayPal:** [paypal.me/dlnraja](https://paypal.me/dlnraja) · **Revolut:** [revolut.me/dylanoul](https://revolut.me/dylanoul)

---
*Last updated 2026-04-06 — [Source on GitHub](https://github.com/dlnraja/com.tuya.zigbee)*
