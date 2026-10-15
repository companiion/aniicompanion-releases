🇧🇷 [Leia em português](README.pt-BR.md)

# AniiCompanion

**A live map of the Lost Sanctum in Aniimo's Egg Heist, drawn on top of your game.**
It shows where you are, which nests may still have an egg, the chests, the way out, and wave alerts. Your team's map is merged with yours.

<p align="center">
  <img src="images/partida.jpg" alt="The AniiCompanion map in the corner of the screen during an Egg Heist match" width="620">
</p>

<p align="center">
  <a href="https://github.com/companiion/aniicompanion-releases/releases/latest"><b>Download for Windows (latest release)</b></a>
</p>

Free. For Windows. Updates itself with one click. A fan project, not affiliated with Pawprint Studio / FunPlus.

---

## What it does

- **You on the map, live.** It finds your position on the game's minimap and shows the whole sanctum. The map can turn with the camera or stay north-up.
- **Nests and eggs.** It shows where a nest may still be, the chance for each spot, which nests you already searched, and eggs dropped on the floor.
- **Rare chests and Prismana.** It shows which chests can still give a Prismana item, and updates as chests get opened.
- **Route and alerts.** A line guides you through the nests you have not checked yet. You get a countdown to the three monster waves and the horde, and a "time to go back" warning with the route to the nearest exit.
- **Upper floor.** When you climb the stairs, the upper walkways show up on the map.
- **Map in a small window.** Prefer a small map in a corner? Switch to a movable, resizable window.
- **Playing with friends.** Add friends and see where they are. Nests, eggs and chests they find appear on your map too.
- **Updates with one click.** The app tells you when a new version is out and installs it after checking the author's signature.

<p align="center">
  <img src="images/mapa-janela.jpg" alt="The map in its own window: nests, chests, route and counters" width="620">
</p>

## Requirements

- Windows 11, 64-bit (tested). Windows 10 should work, but it has not been tested yet.
- Aniimo running in **windowed** or **borderless fullscreen** mode. Exclusive fullscreen cannot be captured, so the map will not work there.

## Install

1. Go to the [latest release](https://github.com/companiion/aniicompanion-releases/releases/latest) and download the `.zip` file.
2. **Extract the whole folder.** Do not run it from inside the zip.
3. Open `AniiCompanion.exe`. (Windows may warn you the first time. See the next section.)
4. The first time, the app downloads the sanctum maps. It takes a few seconds.
5. Open Aniimo in windowed or borderless mode and start Egg Heist. The map appears on top of the game, only inside the sanctum.
6. The difficulty is detected on its own from the coin goal on the game's panel. You can also choose it in the app window (Normal, Hard, Nightmare or Chaos).

**Updating:** the app checks for new versions when it opens and every 6 hours. When there is one, you will see "New version · Update" at the top of its window. Click it and the app does the rest. Your settings, friends and downloaded maps are kept, and the previous version stays in a folder called `AniiCompanion.anterior` next to the app.

**Uninstalling:** delete the app folder. Your settings and logs are kept in `%LOCALAPPDATA%\AniimoCompanion`. Delete that folder too if you want to remove everything.


## Windows warned or blocked it?

The app is free and has **no paid code-signing certificate**. Windows warns about any program like that, even when nothing is wrong. The other Aniimo maps and tools for other games are in the same situation.

1. **"Windows protected your PC"**: click **More info**, then **Run anyway**. You normally only need to do this once. Updates made by the app itself should not ask again.
2. **Your antivirus removed the app**: open Windows Security, then Virus & threat protection, then **Protection history**. Find AniiCompanion, click **Actions**, then **Restore**. If it keeps happening, add the AniiCompanion **folder** to **Exclusions** (an exclusion applies to that folder only, so do not put other things inside it).
3. **Smart App Control (Windows 11)**: with it turned on, no unsigned program can open, and there is no button to allow just one. **The app does not work with Smart App Control on.** Turning it off is your decision. Once it is off, Windows will not let you turn it back on without reinstalling Windows.

## Verify your download

Each release page shows the SHA-256 of the zip. To check yours, open PowerShell in the folder with the file and run:

```powershell
Get-FileHash .\AniiCompanion-<version>.zip
```

Compare the result with the one on the release page. If they are different, do not use the file.

## Safety and fair play

What the app **does**: it looks only at the **image of the game window**, like a screenshot, to find you on the minimap.

What the app does **not** do: it does not read the game's memory, does not inject anything into the game, and does not use mods.

Aniimo has an anti-cheat system. We cannot speak for the game's developers, and we cannot promise you that no tool will ever be flagged. We built the app to touch nothing in the game, but **using it is your own choice and at your own risk**.

## Privacy: what goes over the internet

There is no account and no data collection. The app only talks to the internet for these things:

- **Updates:** it checks this GitHub repository for new versions, and checks the author's signature and the file's SHA-256 before installing anything.
- **Maps:** on first use it downloads the sanctum maps from [aniidex.com](https://aniidex.com) and the upper-floor maps from [HideoutGacha](https://www.hideoutgacha.com).
- **Online mode (only if you use it):** it talks only to friends you added, through public Nostr relays. The relays can see your IP address and the time, but not the content, which is encrypted. With a direct connection, your friend can see your home IP address.
- **"Save report" button:** it only creates a `.zip` file in your Downloads folder. Nothing is sent. If something goes wrong, you can send that file to whoever gave you the app. It has the app logs and a few screenshots of the game window, so other windows open at the time may appear in them.

## FAQ

**The map does not show up.**
Check that Aniimo is in windowed or borderless fullscreen mode. The map also appears only inside the sanctum, and it hides on its own when you open the bag, a chest or a menu, and comes back by itself.

**Which keys does it use?**
- `F1` shows or hides the map.
- `Ctrl+F1` unlocks the small map window so you can drag and resize it. Press it again to lock it, and clicks go through to the game.
- `Ctrl+Shift+F1` restarts the map if it looks wrong (zoomed in, cut off, stuck). Your match is not lost. The "Restart map" button in the app does the same.

While AniiCompanion is open, these keys belong to it and do not reach the game. If another program already uses F1 (for example, another Aniimo map), close it first.

**Is the app in English?**
The app interface is currently in Portuguese. English is planned.

**Something went wrong. What now?**
Click "Salvar relatório" ("Save report") in the app window and send the `.zip` from your Downloads folder to whoever gave you the app.

## Credits and disclaimer

AniiCompanion is a free fan project. Aniimo is a trademark of Pawprint Studio / FunPlus. This project has no connection with them.

This repository only holds the published versions of the app. Each version comes with `AniiCompanion-<version>.zip` (the app) and `manifest.json` plus `manifest.json.sig`, which the app uses to update itself.
