# Rev08.00 (versionName 2.2-Rev08.00, versionCode 5)

## Navigation
- Five master tabs, scrollable in portrait: Azkar, Dua, Kalima, Durood (4th), Istighfar.
- Durood and Istighfar are no longer buried inside Dua/Azkar; each is its own tab.
- Tab routing by precedence: kalima > durood (Salawat/Darood) > istighfar > dua/azkar.

## Content
- Deduplicated by normalized Arabic: 278 -> 240 items (38 exact duplicates removed); usage tags merged on the survivor; better authenticity/source/translation kept.
- Six Kalimas protected as canonical (never absorbed by dedupe).
- Distribution: Dua 122, Azkar 63, Istighfar 29, Durood 20, Kalima 6.

## Display
- Full item shown in one view: Arabic auto-fits, then transliteration/translation scale down too, so nothing is clipped. Scroll only as last resort for the longest passages.
- Portrait Arabic floor lowered (19px) to keep long duas on one screen.

## Salah
- Salah time strip hidden by default; toggle "Salah ribbon" in Settings turns it on.
- Location-based prayer alert + countdown still computed silently; alert fires at prayer time.

## Fixes
- arHtml() guarded against the missing tajweed engine (TJ): previously every render threw with tajweed on, blanking the card. Arabic now renders cleanly; tajweed colouring applies only if an engine is present.
- content_index rotation_modes id-lists rebuilt from deduped data (stale lists removed).

## Verified
- node --check on app.js; all JSON parse; headless jsdom boot clicks all five tabs and renders with zero runtime errors.
