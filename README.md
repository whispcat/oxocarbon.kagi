# Kagi Oxocarbon

A dark [oxocarbon](https://github.com/nyoom-engineering/oxocarbon) theme for Kagi Search, set in IBM Plex with square, Carbon-style corners.

## Install

Open Kagi's [Appearance settings](https://kagi.com/settings/appearance), click Change under Custom CSS, paste in `oxocarbon.css` and save. Make sure the `Enable Custom CSS` toggle is on.

The theme replaces both Kagi's light and dark themes. It doesn't reach the settings pages, because Kagi doesn't apply custom CSS there.

To turn it off for a single page, add `?no_css` (or `&no_css`) to the URL.

## Changing the accent

The accent is pink. To change it, point `--oxo-accent` near the top of the file at another palette color, such as `var(--oxo-blue)`, and adjust `--oxo-accent-soft`, the lighter shade used for hovers and text selection.

## How it works

Kagi's themes are CSS variables set by a class on `<html>` (`.theme_light`, `.theme_moon_dark` and others). The stylesheet redefines those variables on `html:root`, which outranks the theme classes, and then styles individual components directly.
