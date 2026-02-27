# Solar past and forecast model for Home Assistant

This code can be used in Home Assistant. It provides a dashboard with tbe past 24h and expected future 24h solar energy production.

[![Home Assistant](https://img.shields.io/badge/Home%20Assistant-Integration-3DDC84?logo=home-assistant&logoColor=#03A9F4)](https://www.home-assistant.io/) 

## Alpha release
This is an alpha release. There is no guarantee that this code will be developed any further or that it will be maintained in the future. Use at your own discretion.

## Features
It takes into account:
- Your coordinates
- Number of PV panels
- Each set of panels is part of an array, with a maximum of 2 arrays.
- Each array can be specified with
  - azimuth
  - tilt
  - panel Wp
  - temperature coefficient (it takes into account the current local temperature)
  - degradation of the panels due to wear
 
It fetches the required data from https://open-meteo.com/ API.
For now it only uses the KNMI Harmonie Arome Netherlands model, which is suitable for most locations in north-west Europe. It has the advantage of reliable, high res Global Tilted Radiation.
With all the data available, it calculates the expected solar energy production for the past and next 24h for your location, specific PV setup and weather circumstances like temperature.

## What's New?
Release 0.1

### Getting Started
1. **Configure Home Assistant**
   - Use the provided YAML files in the `home assistant` folder as follows.
     - Configuration files are organized using the package-based structure:
       - `packages/advanced_battery_controller.yaml` contains all input entities (booleans, datetimes, numbers, selects) and template sensors for battery control.
     - The main `configuration.yaml` automatically loads all package files from the `packages/` directory

1. **Home Assistant DASHBOARD**
   - In Home Assistant import `dashboard.yaml` to create a dashboard.

## Contributing
Currrently not open for contributions. Any issues can be reported in this repository.
