# MG Smart Glow — ESP8266 Firmware

Cloud-build repository for MG Smart Glow (NodeMCU ESP8266 / ESP-12E).

## Project layout

```
firmware/
  platformio.ini
  src/
    main.ino
.github/
  workflows/
    build-firmware.yml
```

## Add the firmware source

Upload the tested ArduinoDroid sketch to:

`firmware/src/main.ino`

Keep the filename exactly `main.ino`. The sketch includes its Wi-Fi configuration portal and OTA firmware upload route.

## Build firmware

1. Open the **Actions** tab.
2. Select **Build MG Smart Glow Firmware**.
3. Tap **Run workflow** (or push a change under `firmware/`).
4. Open the completed workflow run.
5. Download the artifact named **MG-Smart-Glow-ESP8266-firmware**.
6. Extract `firmware.bin` from the downloaded ZIP.

## OTA upload

Connect your phone to the ESP8266's network and open its local web interface. Use the firmware update section to select and upload `firmware.bin`. Keep the ESP powered reliably during the update. Do not expose the ESP web interface directly to the public internet.

Board: NodeMCU 1.0 (ESP-12E Module), PlatformIO environment: `nodemcuv2`.
