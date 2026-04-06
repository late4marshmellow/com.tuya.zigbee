## Pattern Detection Report

| Pattern | Reports | Priority | Top Fingerprints |
|---|---|---|---|
| False Battery Alert / Missing Battery | 34 | **high** | `vision` (25x), `TS0601` (16x), `sensor` (12x) |
| Pairing Failure | 9 | **high** | `TS0601` (5x), `vision` (5x), `test` (4x) |
| Device Not Responding | 6 | **high** | `test` (6x), `vision` (3x), `TS0601` (3x) |
| Device Shows Unknown | 5 | **high** | `test` (4x), `TS0601` (3x), `_TZE284_aa03yzhs` (2x) |
| Ring/Alarm Wrong | 5 | **high** | `vision` (5x), `TS011F` (3x), `router` (2x) |
| Double Division (wrong sensor values) | 2 | **medium** | `vision` (2x), `test` (2x), `TS0601` (2x) |
| Inverted Sensor State | 1 | **low** | `_TZE200_wfxuhoea` (1x), `deconz` (1x), `vision` (1x) |
| Wrong Voltage | 1 | **low** | `_TZ3000_xr3htd96` (1x), `vision` (1x), `TS0201` (1x) |
| No Temperature | 1 | **low** | `debug` (2x), `test` (2x), `_TZ3000_tsgqxdb4` (1x) |
| Wrong Energy | 1 | **low** | `router` (2x), `_TZE204_clrdrnya` (1x), `vision` (1x) |

### False Battery Alert / Missing Battery (34 reports)
**Fix:** Set `get mainsPowered() { return true; }` and remove measure_battery in onNodeInit
**Files:** `drivers/{driver}/device.js`
**Most affected:** `vision` (25x), `TS0601` (16x), `sensor` (12x), `router` (12x), `test` (10x), `TS0202` (5x), `button` (5x), `tuya` (4x), `switch` (4x), `example` (3x)

### Pairing Failure (9 reports)
**Fix:** Check driver.compose.json fingerprints, verify manufacturerName + productId
**Files:** `drivers/{driver}/driver.compose.json`
**Most affected:** `TS0601` (5x), `vision` (5x), `test` (4x), `example` (3x), `button` (3x), `generic` (3x), `sensor` (3x), `_TZ3000_o4mkahkc` (2x), `TS0202` (2x), `tube` (2x)

### Device Not Responding (6 reports)
**Fix:** Check Zigbee mesh, device routing, and cluster bindings
**Most affected:** `test` (6x), `vision` (3x), `TS0601` (3x), `sensor` (3x), `debug` (2x), `_TZ3210_w0qqde0g` (1x), `TS011F` (1x), `_TZ3000_zutizvyk` (1x), `TS0203` (1x), `_TZ3000_tsgqxdb4` (1x)

### Device Shows Unknown (5 reports)
**Fix:** Check settings keys: zb_model_id (not zb_modelId), zb_manufacturer_name (not zb_manufacturerName)
**Files:** `drivers/{driver}/device.js`
**Most affected:** `test` (4x), `TS0601` (3x), `_TZE284_aa03yzhs` (2x), `tuya` (2x), `generic` (2x), `sensor` (2x), `vision` (2x), `dlnraja` (1x), `example` (1x), `_TZE200_3p5ydos3` (1x)

### Ring/Alarm Wrong (5 reports)
**Fix:** Check alarm DP map
**Most affected:** `vision` (5x), `TS011F` (3x), `router` (2x), `_TZ3000_j1v25l17` (2x), `_TZE204_clrdrnya` (1x), `lumi` (1x), `TS0601` (1x), `sensor` (1x), `relay` (1x), `_TZ3000_gjnozsaz` (1x)

### Double Division (wrong sensor values) (2 reports)
**Fix:** Check TuyaEF00Manager.js:1912 — skip auto-convert when dpMappings has divisor !== 1
**Files:** `lib/tuya/TuyaEF00Manager.js`
**Most affected:** `vision` (2x), `test` (2x), `TS0601` (2x), `router` (2x), `_TZE204_qyr2m29i` (1x), `tuya` (1x), `_TZE204_clrdrnya` (1x), `lumi` (1x), `sensor` (1x), `relay` (1x)

### Inverted Sensor State (1 reports)
**Fix:** Add manufacturerName to invertedByDefault in HybridSensorBase.js + device.js
**Files:** `lib/devices/HybridSensorBase.js`, `drivers/{driver}/device.js`
**Most affected:** `_TZE200_wfxuhoea` (1x), `deconz` (1x), `vision` (1x), `tuya` (1x), `TS0601` (1x)

### Wrong Voltage (1 reports)
**Fix:** Check voltage divisor
**Most affected:** `_TZ3000_xr3htd96` (1x), `vision` (1x), `TS0201` (1x)

### No Temperature (1 reports)
**Fix:** Check DP18 divisor
**Most affected:** `debug` (2x), `test` (2x), `_TZ3000_tsgqxdb4` (1x), `sonoff` (1x), `TS0201` (1x), `TS0601` (1x), `sensor` (1x)

### Wrong Energy (1 reports)
**Fix:** Check energy divisor
**Most affected:** `router` (2x), `_TZE204_clrdrnya` (1x), `vision` (1x), `lumi` (1x), `TS0601` (1x), `sensor` (1x), `relay` (1x)

