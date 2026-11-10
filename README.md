# Weather Window

A plugin for the [TRMNL](https://trmnl.com) e-ink display: the weather forecast as a film still.

One real photograph that fits the next few hours, and two subtitle lines. The first line says what matters
next ("Rain until 13:00, then sun."), the second is a small remark that fits it ("Put the kettle on.").
Top left: your place, the day, high and low. Top right: tomorrow. There is no clock on the picture, so it
is still true when you look at it an hour later.

## How it works

- TRMNL asks [Open-Meteo](https://open-meteo.com) for the forecast at the coordinates in the plugin's form.
- The script in `trmnl/src/shared.liquid` reads the forecast, picks one of 19 kinds of weather for the next
  three hours, and writes both lines and the corner notes.
- It then shows one of the pictures in `stills/`. Every photograph was rendered in advance for each panel:
  `x` and `x_portrait` (TRMNL X, 16 greys), `og` and `og_portrait` (TRMNL OG, black and white).

## Files

- `trmnl/src/`: the plugin as TRMNL imports it (settings and five Liquid files). Generated, do not edit by hand.
- `stills/`: the pictures, four per photograph.
- `CREDITS.md`: every photographer.

## Credits

Photographs: Unsplash, see [CREDITS.md](CREDITS.md). Forecast data: Open-Meteo. Typeface: Fraunces
(SIL Open Font License), served by Fontsource.

Made by thefinkus.
