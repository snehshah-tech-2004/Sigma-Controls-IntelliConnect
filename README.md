# IntelliConnect: ESP32 Industrial Data Logger

Wi-Fi data logger firmware for industrial Modbus RTU devices (temperature scanners, PID controllers). It reads RS-485 slaves, logs to an SD card, and serves a live web dashboard with graphs and CSV export. Built for Sigma Controls.

> This repository publishes release binaries only. The firmware source is private.

## Features
- Reads Modbus RTU slaves over RS-485 with dynamic slave configuration
- Logs readings to SD card; configuration persists in `config.json` on the SD
- Wi-Fi web UI with live Chart.js graphs and CSV export
- Dual Wi-Fi mode (AP + STA) for easy setup and network access
- NTP time sync (IST, UTC+5:30)
- Buzzer alerts via ESP32 LEDC
- Over-the-air updates through GitHub Releases

## Screenshots
![Dashboard](docs/dashboard.png)

## Tech stack
ESP32, PlatformIO (Arduino framework), C++, Modbus RTU, RS-485, Chart.js, SD (SPI), NTP, OTA

## My role
Designed and developed the complete firmware and web UI during my software developer internship at Sigma Controls.

## Releases
See the Releases tab for firmware versions (v1.0, v1.1, v1.1.1).

## License
Proprietary. All rights reserved.
