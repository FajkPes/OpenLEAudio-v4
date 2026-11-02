# OpenLEAudio v4

A configurable Bluetooth LE Audio stack for Windows, created to make headset connections more transparent and controllable.

## Why OpenLEAudio?

I started OpenLEAudio to get more control over Bluetooth LE Audio on Windows and better visibility into connection problems. It uses a dedicated USB Bluetooth adapter through WinUSB while another adapter can continue using the standard Windows stack.

## Features

- Adjust codec, sample rate, frame duration, bitrate, PHY and latency-related settings.
- Monitor connection status, signal and packet loss; configure automatic reconnection.
- Use headset controls, battery reporting and optional microphone support where available.
- Restore the selected adapter to the Windows driver when finished.

## Requirements and setup

- Windows 10/11 x64 and a compatible, dedicated USB Bluetooth adapter.
- VB-CABLE and the Microsoft runtimes described by the installer.
- A compatible LE Audio headset. The reference setup was a JBL TUNE 780NC and ASUS USB-BT600; other devices are not guaranteed to work.

Download the ZIP from [Releases](https://github.com/FajkPes/OpenLEAudio-v4/releases/latest), extract it, and run `START OpenLEAudio 4.bat`. Follow the Setup page to prepare the driver and adapter, then connect the headset. The original step-by-step instructions are in [release/README.md](release/README.md).

The **Range / stability** profile uses automatic codec negotiation and a 1M audio PHY by default. Custom settings take effect according to the application’s labels; some require reconnecting. This project uses a dedicated adapter and is not a replacement for every Windows Bluetooth feature.

[Detailed documentation](README-DETAILS.md) · [All releases](https://github.com/FajkPes/OpenLEAudio-v4/releases)

## Connection and troubleshooting

The aim is both a working LE Audio connection and access to the parameters and diagnostics that explain what the stack is doing. You can use the default stability profile or select custom settings, monitor signal and packet loss, and retry a connection after the headset goes out of range. Some settings apply only after reconnection. The project has been tested with a particular headset and adapter; the same behavior is not guaranteed with every device.

## Credits

**Idea, concept and design:** FajkPes  
**Coding:** ChatGPT Codex, Claude and Google Antigravity
