# pollenkoll-card
A Lovelace custom card for [custom component Pollenkoll](https://github.com/JohNan/home-assistant-pollenkoll/) in Home Assistant.

<b>You have to have `days_to_track` set to a minimum of `3`.</b>

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
      title: false
      city: Stockholm
      allergens:
        - Al
        - Alm
        - Ambrosia
        - Björk
        - Ek
        - Gråbo
        - Gräs
        - Hassel
        - Sälg / vide   # this one is important you write just like this.
```

## Options

| Name | Type | Default | Description
| ---- | ---- | ------- | -----------
| type | string | **Required** | `custom:pollenkoll-card`
| city | string | **Required** | Lower case city from which you have sensors
| allergens | list | **Required** | List of allergens for which you have sensors
| title | boolean | **Optional** | Set to `false` to remove the heading from the card
| minimal | boolean | **Optional** | Set to `true` to show only todays pollen levels in a smaller card
| compact | boolean | **Optional** | Set to `false` to have the three day forecast with bigger images.
| show_state | boolean | **Optional** | Set to `false` if you don't want to show the state text under the images.

The minimal card:

<img src="https://github.com/isabellaalstrom/pollenkoll-card/blob/master/pollenkoll-card-minimal-conf.png" alt="Pollenkoll Lovelace Card minimal configuration option" />


Like my work and want to say thanks? Do it here:

<a href="https://www.buymeacoffee.com/iq1f96D" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/purple_img.png" alt="Buy Me A Coffee" style="height: auto !important;width: auto !important;" ></a>
