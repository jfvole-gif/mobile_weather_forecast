# Changelog

All notable changes to this project are documented here.
The format follows [Keep a Changelog](https://keepachangelog.com/) and the project uses [Semantic Versioning](https://semver.org/).

The **version** number is defined in `custom_components/mobile_weather_forecast/manifest.json`.
The **build** identifier (`YYYYMMDD-N`) is defined in `custom_components/mobile_weather_forecast/const.py`
and is shown, together with the version, on the device page in Home Assistant.

## [0.2.0] - 2026-11-21 (build 20261121-1)

### Added
- **Place sensor**: city name (with region, country and source as attributes). It comes from the tracked entity itself when it provides a locality (Companion app *geocoded location* sensor), otherwise from an optional lookup.
- **Optional place name lookup** through Nominatim / OpenStreetMap, off by default, available in the setup form and in the options. The position is rounded to about 1 km, results are cached, and requests are rate-limited.
- **Elevation** and **time zone** sensors (diagnostic) and matching attributes on the weather entity.
- English and French translations for the new sensors and options.

### Changed
- The `locality` attribute of the weather entity now comes from the place data (same value as before when the Companion sensor is tracked).
- README: installation sections lead with searching in the Marketplace or HACS, and keep adding the repository by hand as a fallback; new "Place name and privacy" section.

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
