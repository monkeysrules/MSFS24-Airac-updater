# MSFS 2024 AIRAC Manager — Python Native

**Drop your 1 large zipped AIRAC and 1-click install it to any aircraft in your Community folder.**

Native desktop app (no browser, no website) — handles Navigraph / NavDataPro / custom zips and copies to the **correct `Community` path for each plane**, with auto backup and version tracking.

> Short: Python app for MSFS 2024 that takes one large AIRAC zip and deploys it to 40+ aircraft — PMDG 737-700/800/900 + all 777s, Fenix, iFly MAX 8, FSLabs, Aerosoft A340/CRJ, TFDi MD-11, CSS 737s & more — in one click.

---

### Features
- **1 large zip → 1 click** — drop a single Navigraph full-cycle zip (1GB+ supported)
- **Correct per-aircraft `Community` paths** — PMDG in `Community\pmdg-aircraft-xxx\Config\NavData` as you noted, plus Fenix, iFly, FSLabs, etc.
- **Auto backup** — `*_backup_<cycle>_<timestamp>` next to each navdata folder
- **Version tracking** — shows `INSTALLED: AIRAC 2407` vs `TARGET: AIRAC 2602` per plane
- **40+ aircraft** — Fenix, PMDG, iFly, FSLabs, Aerosoft, TFDi, CSS, iniBuilds, Just Flight, FBW, stock MSFS 2024 fleet
- **Portable** — single `.py` or single `.exe`, send it to friends, they pick their own Community folder
- **Native Python** — tkinter/customtkinter, no browser

---

### Supported Aircraft & Correct Install Paths

| Aircraft | Community / System Path | Method |
|---|---|---|
| **Fenix A319 / A320 / A321** | `C:\ProgramData\Fenix\Navdata` (shared) | Copy 3 files — Fenix rebuilds on next flight |
| **iFly 737 MAX 8** | `Community\ifly-aircraft-737max8\Data\navdata\Permanent` | Delete old `Permanent`, copy new, run MSFSLayoutGenerator |
| **FSLabs A321 CEO / neo** | `C:\FlightSimLabs2024\fsl-common\FSLabs\NavData` (shared) | Via Navigraph Hub or Control Center |
| **PMDG 737-600 / 737-700 / 737-800 / 737-900 / BBJ** | `Community\pmdg-aircraft-73x\Config\NavData` | Copy 3 files → MSFSLayoutGenerator |
| **PMDG 777-200ER / 200LR / 300ER / 777F** | `Community\pmdg-aircraft-77x\Config\NavData` | Same 3-file copy + MSFSLayoutGenerator |
| **Aerosoft CRJ 900 / A340-300 / A330 CEO** | `Community\aerosoft-xxx\Data\NavData` | Copy NavData folder |
| **TFDi MD-11** | `LocalState\packages\tfdidesign-aircraft-md11\work\Nav-Primary` | Delete old, copy new |
| **CSS 737-300 / 400 / 500** | `Community\cs-aircraft-737-xxx\Data\NavData` | Copy NavData |
| **iniBuilds A350-900 / A300-600R** | `WASM\MSFS2024\inibuilds-aircraft-a350\work\NavigationData` | Replace 2 files + MSFSLayoutGenerator |
| **Just Flight BAe 146 / F28** | `LocalState\packages\justflight-aircraft-xxx\work\JustFlight\navdata` | Delete old, copy new |
| **MSFS 2024 BASE + Stock Fleet** | `Community\navigraph-navdata` + `Community\navigraph-navdata-base` | Via Navigraph Hub → Base |

> **Your default Community:** `C:\Users\n2020\AppData\Local\Packages\Microsoft.Limitless_8wekyb3d8bbwe\LocalCache\Packages\Community`

---

### Quick Start (Python — Native Window)

1. Download `MSFS24-AIRAC-Manager.py`
2. Run: `python MSFS24-AIRAC-Manager.py`
3. In the app: Browse → select your 1 large zipped AIRAC → Select cycle on left → tick planes → Install to Selected

---

### Build a Standalone `.exe` to Send to Friends

1. Put these 3 files in one folder:
   - `MSFS24-AIRAC-Manager.py`
   - `build_exe.bat`
   - `requirements.txt`

2. Double-click `build_exe.bat` — it runs:
