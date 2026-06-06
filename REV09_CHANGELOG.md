# Rev09.00 (versionName 2.3-Rev09.00, versionCode 6)

## Tajweed (now actually works)
- Added a real tajweed engine (TJ.colour) — previously TJ was referenced but never defined, which crashed every render with "Content failed to load: TJ is not defined". That crash is now impossible.
- Heuristic rules applied to Arabic: ghunnah (noon/meem + shadda), qalqalah (sukoon on q/t/b/j/d), noon-sakinah & tanween -> idgham / ikhfa / iqlab, and explicit madd marks. Conservative by design (does not colour every natural madd) to avoid over-painting. It is a reading aid, not a certified mushaf.

## Readability
- Arabic weight 500 -> 700 (bold, no synthesis), transliteration -> 600, English opacity 0.88 -> 1.0 and weight 500. Text is no longer thin.

## Gestures
- Swipe now works in all directions: left/right and (when the card is not scrolling) up/down move to the next/previous item. Thresholds lowered for easier flicks.

## Display glitch
- The screen no longer drifts / shows a diagonal seam: the burn-in pixel-shift now runs ONLY in TV screensaver mode, never on phone/tablet.

## Settings
- "Save & Apply" button is now solid green with white text (was invisible white-on-white because it used an undefined accent variable).

## Verified
- node --check on app.js; headless jsdom boot renders all tabs with zero errors; TJ.colour produces correct coloured spans on Dua items and Ayat al-Kursi.
