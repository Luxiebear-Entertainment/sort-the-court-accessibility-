# Sort the Court! - Accessibility Mod

An accessibility mod for the indie kingdom-management game *Sort the Court!*. This mod provides full screen reader support via NVDA, custom hotkeys for stat tracking, and independent audio controls designed specifically for blind and visually impaired players.

## Features
* **Native NVDA Integration:** Hooks directly into NVDA for fast, zero-latency feedback without relying on Windows UI automation.
* **Smart UI Reading:** Automatically reads floating text, character dialogue, and menu buttons, bypassing Unity's native focus issues.
* **Stat Batching:** Intelligently queues resource changes (Gold, Population, Happiness) to read smoothly after a character finishes speaking.
* **Custom Volume Control:** Splits the game's audio into independent Music and SFX/Voice channels, allowing you to turn down loud music while keeping your screen reader and game effects audible.
* **Text Sanitization:** Automatically strips out Unity Rich Text tags (like `<color=red>`) so your screen reader reads the story, not the code.

## Installation

1. **Install BepInEx:** Download and install [BepInEx](https://github.com/BepInEx/BepInEx) for your game. Extract the contents of the BepInEx zip file directly into your *Sort the Court!* installation folder (where the `.exe` is located).
2. **Run the Game Once:** Launch the game once so BepInEx can generate its configuration folders, then close it.
3. **Install the Mod:** Extract `SortTheCourtAccessibility.dll` and `nvdaControllerClient32.dll` into the `BepInEx\plugins` folder.
4. **Play:** Launch the game. NVDA should announce "Accessibility mod loaded successfully" when you reach the main menu.

## Mod Shortcuts & Hotkeys

### Stat Tracking
Check your kingdom's resources at any time during the day.
* **`Ctrl + H`**: Announce current Happiness.
* **`Ctrl + P`**: Announce current Population.
* **`Ctrl + M`**: Announce current Gold (Wealth).

### Volume Controls
Adjust volume in 10% increments. Menu navigation is safely locked while holding modifier keys.
* **`Ctrl + Up Arrow / Down Arrow`**: Increase / Decrease Background Music volume.
* **`Shift + Up Arrow / Down Arrow`**: Increase / Decrease Sound Effects and Character Voice volume.

### Quality of Life
* **`R`**: Repeat the last important dialogue, prompt, or event text on the screen.
* **`Spacebar`**: Progress through end-of-day summary screens and special event cards.

## Troubleshooting
* **Mod is completely silent:** Ensure `nvdaControllerClient32.dll` is placed in the exact same folder as the mod `.dll`, and that NVDA is currently running before you boot the game.
* **"Extra! Extra!" overlaps with the Main Menu:** Ensure you are using the latest version of the mod, which forces menus to confidently interrupt previous speech.
