# Sunken Garden: builds

Windows builds of **Sunken Garden**, a co-op pixel art survival game where you terraform a desert. This repository only holds the builds. There is no source code here.

## Install (once)

1. Download **[SunkenGardenLauncher.exe](https://github.com/truxiced/sunken-garden-builds/releases/latest/download/SunkenGardenLauncher.exe)**.
2. Run it. Windows may say *"Windows protected your PC"* because the game is not signed: click **More info**, then **Run anyway**.
3. The launcher installs itself and shows a path like
   `C:\Users\<you>\AppData\Local\SunkenGarden\SunkenGardenLauncher.exe`.
   Press **Copy path**. You can delete the file you downloaded.
4. In Steam: **Games > Add a Non-Steam Game to My Library… > Browse…**, paste the path into the file name box, press **Open**, then **Add Selected Programs**.
5. Optional: right-click the new entry in your library, choose **Properties**, and rename it to *Sunken Garden*.

## Play

Start it from Steam. Each time, the launcher checks for a newer build, installs it, and starts the game. If you are offline, it starts the build you already have.

To play together, everyone needs the same build. If joining fails with *"Version mismatch"*, whoever has the older build should quit and start the game from Steam again.

## Where things are

- Game builds: `%LOCALAPPDATA%\SunkenGarden` (the current and the previous build).
- Your saves are kept separately in `%APPDATA%\Godot\app_userdata\Sunken Garden`. Updates never touch them.
- To uninstall, delete `%LOCALAPPDATA%\SunkenGarden` and remove the game from Steam.

## Releases

Each release is one build, named after its build number (for example `build-11` is version `0.5.0+11`). Builds are published automatically and only the newest 20 are kept.
