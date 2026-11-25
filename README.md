# ASCEND V1.1 — Beyond the Gate

## Update existing installation
1. Open your current installed game and export a JSON backup in Settings.
2. Extract this ZIP. Upload its contents (not the enclosing folder) to the root of the **same** GitHub repository, replacing matching files. Commit all changes together.
3. After GitHub Pages deploys, close and reopen the installed app online. Refresh the game if the old version persists. Settings should show V1.1. Do not clear site data or change the site URL.
4. Your existing IndexedDB database and fallback storage keys are unchanged. New fields are initialised automatically. If needed, import your V1 backup. Saves remain device-specific.

## New content
Void Sanctum, Abyssal Throne, Tower of Trials, secondary class attacks, boss heavy attacks, whole-gate auto-battle, variable loot, five new items, enhancements and salvage, three familiars, three universal talents, three loadouts, achievements and titles, story decisions, bestiary, recent quest history, habit backdating and mastery suggestions.

## Tests
Run `node test.cjs` and `node test-expansion.cjs`. Tests cover game logic and page-render functions with a minimal DOM stub, not actual mobile browser installation or IndexedDB persistence. GitHub cloud sync, full branching dungeon maps, advanced class trials, and notification delivery are not implemented. No external service required.

## V1.2 — Paths of Ascension
Back up before updating. Replace files in the same repository; storage keys remain unchanged. Class and rank trials, six class trees, hybrid bonuses, route choices and animated SVG avatars are included. Existing rank and unlocked classes are retained. Class eligibility includes lifetime quest XP in both required attributes; historical values are estimated from existing completion records. Artwork uses CSS idle animations, not frame-by-frame combat sprites. No cloud sync or push notifications yet. Test with `node test.cjs`, `node test-expansion.cjs`, and `node test-ascension.cjs`.
