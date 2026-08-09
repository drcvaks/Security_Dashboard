# Home Security Dashboard Changelog

## v1.3 (First Git Version)
Date: 2026-08-06

### Added
- Git version control
- Professional security status bar
- Digital clock
- Ring alarm status
- Camera activity status:
  - Monitoring
  - Door • Side • Shed LIVE
  - Front LIVE
  - All Cameras LIVE

### Improved
- Dashboard now resembles a commercial security console.
- Replaced "Rear" terminology with descriptive activity messages.

## v1.4.0 — Camera Console Foundation
- Added second Camera Console view
- Added Back Steps and Deck exterior snapshots
- Added Living Room, Kitchen, and Basement standby cards
- Added Mushroom-based console styling
- Standardized interior card layout and heights

## v1.4.1 — Living Room Live View
- Added tap-to-live behavior for Living Room
- Added conditional standby/live card switching
- Added tap-to-stop behavior
- Confirmed direct helper control works without an intermediary script

## v1.4.2 — All Interior Cameras Live
- Added tap-to-live behavior for Living Room
- Added tap-to-live behavior for Kitchen
- Added tap-to-live behavior for Basement
- Added tap-to-stop behavior for each interior camera
- Standardized interior camera interaction using `input_select.interior_live_camera`

## v1.4.3 — Interior Camera Auto Timeout
- Added 10-minute automatic timeout for interior live cameras
- Preserved tap-to-stop behavior
- Restarted timeout when switching between interior cameras
- Centralized interior camera timing in `script.interior_camera_live`

## v1.4.4 — Doorbell Takeover

### Added
- Added automatic Doorbell Takeover triggered by `binary_sensor.front_ding`
- Added `input_boolean.doorbell_takeover` helper to control takeover state
- Doorbell press displays the Front Door live camera for 30 seconds
- Doorbell Takeover works from both the Security Console and Camera Console
- Normal dashboard automatically returns after the takeover ends
- Repeated doorbell presses restart the 30-second takeover timer

### Improved
- Reworked Camera Console interior camera layout
- Grouped each interior camera's standby and live states into a single card stack
- Removed large gaps between Living Room, Kitchen, and Basement cards
- Removed duplicate Living Room card introduced during layout restructuring
- Preserved 10-minute interior camera timeout and tap-to-stop behavior

### Entities / Helpers
- `binary_sensor.front_ding`
- `input_boolean.doorbell_takeover`
- `camera.door_live_view`

### Automation
- `Doorbell → Full Screen`

## v1.4.4 - modification

### Display Optimization
- Optimized Security Console for the ASUS 1080p touchscreen
- Changed primary camera cards from 16:9 to 16:8
- Ensured the complete 2×2 camera grid and camera labels remain visible
- Maintained Chrome at 100% zoom for normal text readability
