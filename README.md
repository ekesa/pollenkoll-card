# pollenkoll-card
A Lovelace custom card for [custom component Pollenkoll](https://github.com/JohNan/home-assistant-pollenkoll/) in Home Assistant.

<b>You have to have `days_to_track` set to `3`. Sälg and asp currently not working.</b>

<img src="https://github.com/isabellaalstrom/pollenkoll-card/blob/master/pollenkoll-card.png" alt="Pollenkoll Lovelace Card" />

## Installation

1. Copy `pollenkoll-card.js` to `<config directory>/www/pollenkoll-card.js`
2. Copy the folder `pollen_img` and place in `<config directory>/www/`
3. Add `pollenkoll-card` as a resource in `ui-lovelace.yaml` or in raw config editor if you don't use yaml mode.

```yaml
resources:
  - url: /local/pollenkoll-card.js
    type: js
```


## Example configuration
Pick the allergens you want to display.
```yaml
views:
  title: My view
  cards:
    - type: custom:pollenkoll-card
      city: stockholm
      allergens:
        - al
        - alm
        - björk
        - ek
        - gråbo
        - gräs
        - hassel
```

## Options

| Name | Type | Default | Description
| ---- | ---- | ------- | -----------
| type | string | **Required** | `custom:pollenkoll-card`
| city | string | **Required** | Lower case city from which you have sensors
| allergens | list | **Required** | List of allergens for which you have sensors


Like my work and want to say thanks? Do it here:

<a href="https://www.buymeacoffee.com/iq1f96D" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/purple_img.png" alt="Buy Me A Coffee" style="height: auto !important;width: auto !important;" ></a>
