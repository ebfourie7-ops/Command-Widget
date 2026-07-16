# Command Widget

Command Widget is a KDE Plasma 6 system-telemetry widget with a user-level installer. It provides local telemetry for the widget and for applications such as Command Centre.

## What It Shows

- Power mode
- CPU usage, frequency, and temperature
- RAM and GPU usage
- Storage usage and read/write speeds
- Fan, network, VPN, and battery status

## Install

Clone the repository and run the installer:

```bash
git clone https://github.com/ebfourie7-ops/Command-Widget.git
cd Command-Widget
./install.sh
```

The installer copies the widget and telemetry programs into the current user's profile and enables:

- `telemetry-daemon.service`
- `telemetry-http-daemon.service`

The local telemetry endpoint is `http://127.0.0.1:9090/telemetry`.

No root access is required. After installation, add **Telemetry Widget** from Plasma's **Add Widgets** panel.

## Uninstall

```bash
./uninstall.sh
```

The uninstaller stops and disables the user services and removes the installed widget and helper programs.

## Requirements

- KDE Plasma 6
- Python 3
- systemd user services
- Standard Linux telemetry interfaces under `/proc` and `/sys`

## License

MIT
