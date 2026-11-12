# Setup
Go to this link on your old iPhone.

[https://cbechtell.github.io/free-iphone-clock/](https://cbechtell.github.io/free-iphone-clock/)

Done!

# Free iPhone Clock

A full-screen digital wall clock that runs in Safari. It's built for old iPhones, like the iPhone 5c on iOS 10, that can't run modern clock apps. It's one HTML file with no app, no ads, and no tracking, and it works on any phone, tablet, or computer.

## Features

- Big digits that scale to fill the screen in portrait or landscape
- 10 font styles, all built into iOS, so nothing has to download
- 7 colors
- 12-hour or 24-hour time
- Date shown under the time
- Blinking colon
- Dims automatically at night, 10 PM to 7 AM by default
- Remembers your settings
- Keeps time with no internet once it's loaded, because it reads the time from the device

## Using it

Tap anywhere on the clock to open the settings menu. Pick a font, a color, and 12 or 24 hour, then tap **Done** or tap outside the menu. The menu also closes by itself after 20 seconds.

## MORE Setup (for iphones)

1. Open the clock's address in **Safari**.
2. Tap the **Share** button, then **Add to Home Screen**. Launch the clock from that icon so it opens full screen without Safari's address bar.
3. Keep the screen on: **Settings → Display & Brightness → Auto-Lock → Never**.
4. Optional, to lock the phone to the clock: turn on **Guided Access** in **Settings → General → Accessibility → Guided Access**. Open the clock and triple-click the Home button to start it. Triple-click again and enter the passcode to exit.
5. Turn the screen brightness down. The clock looks better and the backlight lasts longer.

## Customizing

All settings are near the top of the `<script>` section in `index.html`.

**Night dimming hours** use 24-hour time:

```js
var NIGHT_START = 22, NIGHT_END = 7, NIGHT_OPACITY = 0.45;
```

Set `NIGHT_OPACITY` to `1` to turn dimming off. Lower numbers make the night display darker.

**Colors:** add or change entries in the `themes` list:

```js
{ name: "Purple", color: "#b388ff" },
```

**Fonts:** add or change entries in the `fonts` list. `family` is a normal CSS font stack and `weight` is the CSS font weight:

```js
{ name: "Georgia", family: 'Georgia, serif', weight: 400 },
```

For the clock to look right on the iPhone, use fonts that come built into iOS. Fonts that aren't on the device fall back to the next font in the list.

## Compatibility

The page is written in older-style JavaScript and CSS so it runs on Safari in iOS 10. On desktops and Android, the iOS fonts are replaced with similar fonts that are on that device.
