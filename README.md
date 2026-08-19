# Calamba Emergency Ready (CER)

Scaled-down fork of Parañaque Emergency Ready (PER), built for Calamba, Misamis Occidental.

## What changed from PER
- Removed: Incident Report, Windy weather map, Hospital Locator, Family Emergency Plan
- Contact grid: PNP, BFP, DRRMO, Barangay only (no 911/HEMS/EOC on the main grid — 911 kept as an About-page fallback link only)
- Camera: lite version — photo + manual location text + timestamp only (no GPS auto-lock, no name/contact stamp), shares via native share sheet (Messenger-compatible)
- Barangay dropdown: Calamba's 19 barangays
- Theme: blue (#0D47A1) + yellow (#FFD700), same rounded-box style as PER
- Kept as-is: Profile screen (with ICE card), 72-hour Go Bag checklist, Manage Contact Numbers, About

## STILL NEEDED before this is usable
1. **Barangay-level phone numbers** for all 19 barangays — the "Manage Contact Numbers" screen lets you (or residents' barangay officials) fill these in per-barangay after install; there's no single master list to hardcode. PNP, BFP, and MDRRMO numbers are now set (see below).
2. **Municipality of Calamba logo** — the splash screen currently shows a placeholder SVG circle labeled "CALAMBA MUNICIPALITY LOGO PLACEHOLDER". Swap `<img class="splash-logo">`'s `src` for the real logo (as a base64 data URI, same pattern as the placeholder).
3. **Rotunda / Jose Rizal Statue background image** — the splash screen background is currently a placeholder SVG. Swap `<img class="splash-city-bg">`'s `src` similarly.
4. **Small header icon** (top-left of Home screen) — also currently a placeholder.
5. **App icons** — `manifest.json` references `icons/icon-72.png` through `icon-512.png`, but no `icons/` folder exists in the source PER repo either — these must be supplied/generated separately (likely handled during Median wrapping, worth confirming).
6. **LGU seal permission** — worth a quick check with the municipality on using the official seal in a community app before shipping publicly.

## Distribution
Same as PER: push to GitHub Pages, wrap via Median.co.

## Contact numbers now set
- PNP: 0998-598-6928
- BFP: 0975-490-2003
- MDRRMO: 0963-559-8199
