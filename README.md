<div align="center">

# ✨ Hyperspace Lighting x Home Assistant ✨

[![HACS Custom](https://img.shields.io/badge/HACS-Custom-41BDF5.svg?style=flat-square&logo=homeassistant&logoColor=white)](https://github.com/hacs/integration)
[![License](https://img.shields.io/github/license/hyperb1iss/signalrgb-homeassistant?style=flat-square&logo=apache&logoColor=white)](https://opensource.org/licenses/Apache-2.0)

Adds support to your home assistant for [Hyperspace Lighting](https://hyperspacelight.com/) devices.

![alt text](images/hc.webp)

</div>

## 🔧 HACS Installation
> **Note**: This component isn't in the official HACS repository. You can add it as a custom repository:
>
> 1. Go to HACS
> 2. Click on the three dots in the top right corner
> 3. Select "Custom repositories"
> 4. Enter "ToddAlvord/hyperspace-homeassistant" for the repository
> 5. Select "Integration" for the category
> 6. Click "Add"

1. Ensure that [HACS](https://hacs.xyz/) is installed in your Home Assistant instance.
2. In the HACS panel, go to "Integrations".
3. Click the "+" button in the bottom right corner.
4. Search for "Hyperspace Lighting" and select it.
5. Click "Install" and wait for the installation to complete.
6. Restart Home Assistant.





## Attribution
Hyperspace Lighting devices use a forked version of WLED. The native Home Assistant WLED integration worked with hyperspace lighting devices up to version `2024.7.4`. This repo is a copy of that `2024.7.4` WLED integration with additional changes. You can visit the [Home Assistant Core github](https://github.com/home-assistant/core) page for more information.


## Differences from stock 2024.7.4 WLED integration
- `manifest.json` 
    - `domain` changed so both the native WLED integration and this integration can co-exist without this one overriding core version.
    - `name` changed to match this integration.
- `const.py` - Updated domain to match manifest.
- `config_flow.py` - Only allows WLED devices whose `brand` is `Hyperspace`. This prevents standard WLED devices from being picked up by this integration.
- `strings.json` - Added new `abort_async` message for when non hyperspace devices are detected.
- Created as a HACS custom integration for convenience.