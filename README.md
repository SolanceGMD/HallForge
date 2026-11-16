# HallForge

**Precision at every press.**

HallForge is a browser-based magnetic keyboard configuration centre with an interactive per-key editor, actuation and Rapid Trigger tuning, profiles, and a WebHID device discovery layer.

## Live deployment

The GitHub Actions workflow in `.github/workflows/deploy.yml` builds and deploys the static application to GitHub Pages whenever changes are pushed to `main`. The repository's Pages source must be set to **GitHub Actions** if it is not already enabled.

## Features

- Interactive keyboard layout with per-key actuation and Rapid Trigger settings
- Configurable actuation, press sensitivity, release sensitivity and Rapid Trigger toggle
- Apply settings to a row or the full keyboard
- Competitive, Everyday and Precision profiles; create custom profiles
- Local autosave plus JSON import/export
- WebHID device discovery and connection status
- Responsive Wooting-inspired dark interface

## Hardware support

WebHID device discovery is not the same as universal hardware control. Writing settings requires a tested, manufacturer- and firmware-specific protocol adapter. HallForge deliberately does not send guessed HID reports or claim settings have been applied to hardware. The current release provides a complete visual configurator and safe device detection; actual hardware configuration is enabled only when a validated adapter exists.

## Run locally

Serve this directory with any static HTTP server, for example:

```bash
python -m http.server 8080
```

Open `http://localhost:8080`. WebHID requires a secure context (HTTPS or localhost) and a compatible browser.

## Deployment

Push to `main`. The workflow installs no dependencies and publishes the static site to GitHub Pages.
