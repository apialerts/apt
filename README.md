# API Alerts • apt repository

This repository hosts the apt package repository for the [API Alerts CLI](https://github.com/apialerts/apialerts-cli), served via GitHub Pages at [apt.apialerts.com](https://apt.apialerts.com).

- Website: [apialerts.com](https://apialerts.com)
- Docs: [apialerts.com/docs/tools/cli](https://apialerts.com/docs/tools/cli)

> Do not edit this repository manually. It is updated automatically on each CLI release.

## Installation

```bash
curl -fsSL https://apt.apialerts.com/key.gpg | sudo gpg --dearmor -o /usr/share/keyrings/apialerts.gpg
echo "deb [arch=amd64,arm64 signed-by=/usr/share/keyrings/apialerts.gpg] https://apt.apialerts.com stable main" | sudo tee /etc/apt/sources.list.d/apialerts.list
sudo apt update && sudo apt install apialerts
```

## Direct Install (without repository)

If you'd prefer not to add the repository, `.deb` packages are available on the [GitHub Releases](https://github.com/apialerts/cli/releases) page:

```bash
sudo dpkg -i apialerts_<version>_linux_amd64.deb
```

Note: packages installed this way won't receive updates via `apt upgrade`.

## Upgrading

```bash
sudo apt update && sudo apt upgrade apialerts
```

## Uninstalling

```bash
sudo apt remove apialerts
```
