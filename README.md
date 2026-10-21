# Sunken Garden: builds

Windows and Linux builds of **Sunken Garden**, a co-op pixel art survival game where you terraform a desert. This repository only holds the builds. There is no source code here.

## Install on Windows (once)

1. Download **[SunkenGardenLauncher.exe](https://github.com/truxiced/sunken-garden-builds/releases/latest/download/SunkenGardenLauncher.exe)**.
2. Run it. Windows may say *"Windows protected your PC"* because the game is not signed: click **More info**, then **Run anyway**.
3. The launcher installs itself and shows a path like
   `C:\Users\<you>\AppData\Local\SunkenGarden\SunkenGardenLauncher.exe`.
   Press **Copy path**. You can delete the file you downloaded.
4. In Steam: **Games > Add a Non-Steam Game to My Library… > Browse…**, paste the path into the file name box, press **Open**, then **Add Selected Programs**.
5. Optional: right-click the new entry in your library, choose **Properties**, and rename it to *Sunken Garden*.

## Install on Linux (Ubuntu, once)

1. Open a terminal and run:
   ```sh
   cd ~/Downloads
   curl -fLO https://github.com/truxiced/sunken-garden-builds/releases/latest/download/SunkenGardenLauncher.x86_64
   chmod +x SunkenGardenLauncher.x86_64
   ./SunkenGardenLauncher.x86_64
   ```
   Downloaded with a browser instead? The file is not executable yet, and double-clicking it in Files does nothing: run the `chmod` and `./` lines above.
2. The launcher installs itself to `~/.local/share/SunkenGarden` and adds **Sunken Garden** to the app menu. Press **Continue** to download the game. You can delete the file you downloaded.
3. In Steam: **Games > Add a Non-Steam Game to My Library…**, tick **Sunken Garden** in the list, then **Add Selected Programs**.
   Not in the list? Press **Browse…**, press **Ctrl+H** to show hidden folders, and pick `~/.local/share/SunkenGarden/SunkenGardenLauncher.x86_64`.

You can also start it from the app menu without Steam.

## Play

Start it from Steam. Each time, the launcher checks for a newer build, installs it, shows what changed, and starts the game when you press **Play**. If you are offline, it offers the build you already have.

To play together, everyone needs the same build. If joining fails with *"Version mismatch"*, whoever has the older build should quit and start the game from Steam again.

## Where things are

| | Windows | Linux |
|---|---|---|
| Launcher and game builds (the current and the previous one) | `%LOCALAPPDATA%\SunkenGarden` | `~/.local/share/SunkenGarden` |
| Your saves (updates never touch them) | `%APPDATA%\Godot\app_userdata\Sunken Garden` | `~/.local/share/godot/app_userdata/Sunken Garden` |
| Launcher log, for when something goes wrong | `%LOCALAPPDATA%\SunkenGarden\launcher.log` | `~/.local/share/SunkenGarden/launcher.log` |

To uninstall, delete the launcher folder and remove the game from Steam. On Linux also delete `~/.local/share/applications/sunken-garden.desktop`.

## Releases

Each release is one build, named after its build number (for example `build-11` is version `0.5.0+11`). It holds the game for Windows and Linux, both launchers, and `latest.json`, which the launcher reads. Builds are published automatically and only the newest 20 are kept.
