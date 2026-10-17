# Titan Gold Tracker — Both Factions (WotLK)

A small compatibility fix for Titan Panel's Gold Tracker on **WoW WotLK 3.3.5**, based on Titan Panel **4.3.8.30300**.

The tooltip and server gold total include **Alliance and Horde characters on the same realm**. Existing saved balances and hidden-character settings remain compatible; no database reset is needed.

## Installation

Requires an existing Titan Panel installation. This repository contains only the Gold Tracker module.

1. Exit WoW completely.
2. Back up `Interface\AddOns\TitanGoldTracker` and optionally `WTF\Account\<account>\SavedVariables\TitanGoldTracker.lua`.
3. Download this repository using **Code → Download ZIP**, then copy the included `TitanGoldTracker` folder into `Interface\AddOns`, replacing the existing module.
4. Start WoW and log into each character at least once with Gold Tracker enabled.
5. Right-click Gold Tracker and choose **Display server gold** to show the combined total on the bar.

Offline balances reflect the last login. Characters on different realms or WoW accounts are not combined. Hidden characters remain excluded.

## Scope

The supplied fix changes `TitanGoldTracker.lua` and `TitanGoldTracker.toc`; other Titan Panel modules do not need replacing. Saved keys retain the existing `character_realm::faction` format, while display filtering includes both factions on the current realm.

## Validation

The supplied archive reports Lua 5.1 checks using simulated WoW APIs for combined totals/tooltips, realm isolation, hidden characters, sorting, the player-only toggle, money updates, and persistence across faction logins. Those checks were not rerun as part of this repository import. **Not tested inside the WoW client.**

To roll back, exit WoW and restore your backed-up Gold Tracker folder.

## Credits

Original Gold Tracker: **Poena @ Area 52** and the **Titan Development Team**. Original source credits and localization files are preserved. This is an unofficial fix, not a full Titan Panel distribution.

No license file was included in the supplied archive; this repository does not assign a new license to the upstream code.
