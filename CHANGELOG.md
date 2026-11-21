# Changelog

All notable changes to this project are documented here.
The format follows [Keep a Changelog](https://keepachangelog.com/) and the project uses [Semantic Versioning](https://semver.org/).

The **version** number is defined in `custom_components/mobile_weather_forecast/manifest.json`.
The **build** identifier (`YYYYMMDD-N`) is defined in `custom_components/mobile_weather_forecast/const.py`
and is shown, together with the version, on the device page in Home Assistant.

## [Unreleased]

### Changed
- README: the installation sections now lead with searching in the Marketplace or HACS, and keep adding the repository by hand (custom repository / add from link) as a fallback.

## [0.1.0] - 2026-11-19 (build 20261119-1)

First public pre-release.

### Added
- `weather` entity following the position of a smartphone or tablet (`person`, `device_tracker` or geocoded location sensor), with current conditions and daily/hourly forecasts, based on Open-Meteo.
- Sensors: condition (translated), temperature, feels like, humidity, precipitation, wind, wind gusts, pressure.
- Refresh on a regular interval (default 15 min) and immediately when the tracked entity moves more than 5 km.
- Fallback on the home position when the tracked entity has no coordinates.
- Setup through the UI, options flow for the update interval, one entry per tracked device.
- English and French translations.
- Brand icon and logo.
