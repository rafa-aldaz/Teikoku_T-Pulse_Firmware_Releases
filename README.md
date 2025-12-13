# T-Pulse Firmware Releases

This repository contains public firmware releases for T-Pulse devices.

## Manifest

The `manifest.json` file contains metadata about available firmware versions. The iOS app uses this file to check for updates.

## Firmware Files

Firmware binaries are stored in the `firmware/` directory and are also attached to GitHub releases.

## How to Update Firmware

1. Use the T-Pulse iOS app
2. Connect to your device via Bluetooth
3. Navigate to the OTA Update section
4. Tap "Check for Updates"
5. Follow the on-screen instructions

## Repository Structure

```
├── manifest.json          # Firmware metadata (used by iOS app)
├── firmware/              # Firmware binary files
│   └── Teikoku_T-Pulse-*.bin
└── README.md             # This file
```

## For Developers

To publish a new firmware release:

1. Build the firmware: `idf.py build`
2. Run the publish script: `./scripts/publish_firmware_release.sh <version> [notes]`
3. Commit and push changes to this repository
4. Create a GitHub release with the firmware binary
