<h1>TV remote for mobile dashboard</h1><br>

![IMG_20230921_215310](https://github.com/smeen89/Mobile-tv-remote/assets/106514124/ccbf6492-3e3e-481f-86c4-d90121ecff13)

<h2>1. Prerequisits</h2>
<b>Minimal:</b>
You will need the following HACS addons in order to setup the card.

https://github.com/custom-cards/button-card<br>
https://github.com/custom-cards/stack-in-card<br>
https://github.com/thomasloven/lovelace-card-mod<br>
https://github.com/thomasloven/lovelace-layout-card<br>
https://github.com/AnthonMS/my-cards/blob/main/docs/cards/slider-v2<br>

<b>Optional:</b>
https://github.com/thomasloven/hass-browser_mod<br>
https://github.com/thomasloven/lovelace-popup-card (deprecated). But needed in order to remove white border around card if using it as a pop up.<br>

<h2>2. Settings</h2>
If you intend to use the full set up and want to remove the white border around the pop up you should put the following in the CSS style option of the pop up card:

```
--mdc-theme-surface: transparent;
```
This is why the deprecated pop up card is needed. I haven't found another way to apply the CSS directly by using the intended way of opening a pop up using the code below from Browser Mod docs.

```
action: fire-dom-event
browser_mod:
  command: popup
  title: My title
  card:
    type: ...etc...
```

Furthermore the card is styled to fit my phones dimensions. Another user will likely have to make adjustments in order to fit their needs. It's probable that adjustments have to be made to the margin and width of the custom volume slider of the card.<br><br>
I've used scripts for my buttons to do specific things suited for my set up but other users could simply call a service or use it to toggle an entity. Have fun.

<a href="https://www.buymeacoffee.com/smeen89" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Beer" style="height: 41px !important;width: 174px !important;" ></a>
