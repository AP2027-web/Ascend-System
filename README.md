# ASCEND: The System — V1.0 The Awakening

A single-player, mobile-first life RPG. No account, database subscription or external assets required. All progress lives in your browser (IndexedDB, with localStorage fallback if opening the database fails).

## Deploy to GitHub Pages
1. Extract the ZIP. Create a new public repository on GitHub, e.g. `ascend-system`.
2. Upload the files inside the extracted folder to the repository root (index.html must be at the root). Commit them to `main`.
3. Go to Settings → Pages → Build and deployment. Select Deploy from a branch, `main`, `/ (root)`, and Save.
4. When GitHub displays your Pages URL, open it on your phone. Android Chrome: menu → Add to Home screen / Install app. iPhone Safari: Share → Add to Home Screen.
5. Open the game, customise your player and start completing directives. Use Settings → Export player backup regularly.

## Local testing
From the extracted folder, run `python -m http.server 8000`, then open http://localhost:8000 on the same computer. To test from a phone on the same Wi-Fi, use the computer's LAN IP and port 8000; firewall rules may need adjustment. LAN HTTP does not generally support service workers, so use GitHub Pages HTTPS for phone installation and offline use.

A separate standalone HTML preview is provided outside the ZIP for quick desktop evaluation. It is not the installable edition; progress in the preview is separate from the hosted game. Export/import JSON to transfer.

## Gameplay
- Start with five editable habit directives. Create daily, weekly, one-off and counter quests, set days and rewards, or use suggestions.
- Complete tasks for XP, gold and energy. Daily habit completion provides a bonus. Attribute XP increases attributes automatically; allocate level-up points separately.
- Enter the Forgotten Crypt at level 1 after earning 3 energy. Four gates unlock at levels 1, 5, 12 and 22. Fight manually or auto-resolve an encounter. Branching gates offer rest and mystery options between fights.
- Buy and equip items. Unlock classes at level 5 when both required attributes reach 7. Equip up to two; named hybrids appear for supported combinations. The primary class determines the active combat skill in this version.
- Settings includes rest mode, optional penalties, difficulty, backups, daily recovery snapshot and storage persistence request. No real-life penalties or purchases.

## Saves and updates
Local saves are automatic and device/browser/origin specific. No GitHub API token is used. GitHub Pages hosts code only, not player progress. Do not commit exported personal saves to a public repository. Clearing site data can erase saves; export backups. On updates keep the same Pages URL and database name, increment the service worker cache version and implement migrations before changing the save schema. Multiple concurrent tabs are not supported; use one active session. GitHub cloud sync is deferred.

## Scope and limitations
V1 uses original SVG avatar and portal graphics; avatar customisation is colour-based. Story content is a four-chapter outline with gate clears, not a full branching narrative. Class unlocks are attribute-based; job-change trials, deeper class/hybrid skill trees, procedural maps, crafting, notifications, adaptive habit analysis, weekly completion bonuses, full achievement cosmetics and cloud sync are future expansions. Gate energy accumulates without a cap. The suggestions are template-based, not AI. Difficulty and reward values are initial balance assumptions. Habit completion cannot currently be undone or backdated. The game uses local calendar dates. Browser storage persistence is not guaranteed.
