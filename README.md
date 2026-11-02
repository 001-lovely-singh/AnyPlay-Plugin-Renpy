# 🎮 Any Play – Ren'Py Plugins

Two small companion apps for **[Any Play](https://001-lovely-singh.github.io/)** that let you play **Ren'Py 7 and Ren'Py 8 visual novels** on your Android phone – straight from a game folder or straight from a `.zip` file, with on-screen touch controls.

> These plugins are **not standalone apps**. You open a Ren'Py game inside Any Play, and Any Play hands it over to the matching plugin.

## 📥 Downloads

| Plugin | For games made with | Min. Android | Download |
|---|---|---|---|
| **Ren'Py 7 Plugin** | Ren'Py 7+ | 4.4 | [AnyPlay-Renpy7-Plugin.apk](https://github.com/001-lovely-singh/AnyPlay-Plugin-Renpy/releases/download/v1.0/AnyPlay-Renpy7-Plugin.apk) |
| **Ren'Py 8 Plugin** | Ren'Py 8+ | 5.0 | [AnyPlay-Renpy8-Plugin.apk](https://github.com/001-lovely-singh/AnyPlay-Plugin-Renpy/releases/download/v1.0/AnyPlay-Renpy8-Plugin.apk) |

Ren'Py 7 and Ren'Py 8 are different engine versions, so install the plugin that matches your game (or both, they can be installed side by side).

All releases: [Releases page](https://github.com/001-lovely-singh/AnyPlay-Plugin-Renpy/releases)

## 📦 Technologies

- `Ren'Py 7.7.1` (Ren'Py 7 plugin)
- `Ren'Py 8.5.3` (Ren'Py 8 plugin)
- `Java`
- `Kotlin`
- `Python 2.7 / 3` (the engine's own scripting)
- `SDL2`
- `Gradle`

## 🦄 Features

Here's what the plugins can do:

- **Play from a folder** : point Any Play at a Ren'Py PC game folder (the one that contains `game/`) and it runs in place, nothing is copied.
- **Play straight from a `.zip`** : no extracting first. The game is read directly from the zip file.
- **On-screen gamepad & keyboard** : a D-pad and buttons (ENTER, ESCAPE, Z, B) plus a full keyboard overlay, in the same look as Any Play.
- **Editable layout** : tap the pencil icon to move, resize, recolor, copy or delete buttons, and add your own. Your layout is saved per game on your device.
- **Memory-friendly** : the image cache is sized to your phone's RAM, so big games don't choke a phone with little memory.
- **No autosave stutter** : autosave is off by default, because saving the whole game state makes the game freeze for a moment.
- **No ads, no account, no tracking** : the plugins are just game players.

## 🕹️ The Icon Column

A small icon column sits in the top-right corner while you play:

- **Gamepad icon** – show / hide the touch controls
- **Pencil icon** – edit the button layout (move, resize, recolor, add, reset, undo)
- **Sparkle icon** – cheats. Ren'Py games don't need cheats, so it only shows a short note
- **Keyboard icon** – show / hide the on-screen keyboard

While you edit the layout, Back leaves the editor instead of closing the game.

## 🎯 How It Works

1. You open a Ren'Py game in Any Play.
2. Any Play starts the matching plugin and tells it where the game is (a folder or a zip file).
3. The plugin checks it has file access, then starts the Ren'Py engine and runs the game from there.
4. Your saves stay on your device (next to the game when it is a folder, like on a PC).

## 👨‍🍳 The Process

The plugins are built with Ren'Py's own Android build tool (`rapt`) and a tiny "stub" game. The stub game has no story of its own – it only tells the engine to run whatever game Any Play points to.

On top of that I added:

- Direct `.zip` support, so large games don't have to be extracted first
- A memory manager that adapts the image cache to the phone and only frees memory when Android says it is really low
- The same on-screen controls as the main Any Play app

While testing I found that a game ran noticeably slower on Ren'Py 7.8.7 on my phone than on 7.7.1, so the Ren'Py 7 plugin is built on **7.7.1**.

## 📚 What I Learned

- Reading engine logs to find where a game really spends its time
- How Android handles memory and why graphics memory doesn't show up in an app's normal memory numbers
- Mixing Java and Kotlin in one Gradle project
- How open-source licenses (MIT / LGPL) work when you ship a program built on an engine

## 🚀 Installing

1. Download the APK you need from the table above.
2. Open it. If Android asks, allow **"Install from unknown sources"** for your browser or file manager.
3. Install it.
4. Open a Ren'Py game from **Any Play** – it will start the plugin for you.
5. The first time, the plugin asks for **"All files access"**. It needs this to read the game you chose and to save your progress next to it. Allow it and come back.

> ⚠️ **Play Protect / "unknown app" warning:** Android shows this for any app installed outside the Play Store. It does not mean something is wrong.

## 🔒 Privacy

The plugins don't collect, store or send personal information, don't show ads, and have no account or analytics. They need file access only to read your game and save your progress. They may create small files on your device (for example a log, a crash report, and the save and cache files Ren'Py itself makes). Full details are in the Privacy Policy on the [Any Play website](https://001-lovely-singh.github.io/).

## 📄 Licenses

These plugins are built on **[Ren'Py](https://www.renpy.org/)** and contain free software licensed under a number of licenses, including the GNU Lesser General Public License. A complete list of the software is available at [renpy.org/doc/html/license.html](http://www.renpy.org/doc/html/license.html).

- License of the Ren'Py 7 plugin: [`RENPY-7-LICENSE.txt`](RENPY-7-LICENSE.txt)
- License of the Ren'Py 8 plugin: [`RENPY-8-LICENSE.txt`](RENPY-8-LICENSE.txt)
- Source code of Ren'Py: [github.com/renpy/renpy](https://github.com/renpy/renpy)
- Build tooling for the Android engine: [github.com/renpy/renpy-build](https://github.com/renpy/renpy-build)

The games you play with these plugins belong to their own creators and have their own licenses.

Any Play and these plugins are independent projects. They are **not affiliated with or endorsed by** the Ren'Py project.

## 💭 How It Can Be Improved

- A settings screen for autosave, hardware video and image cache size
- Typing text into Ren'Py input boxes from the on-screen keyboard

## 📬 Contact

[Join the Discord](https://discord.gg/Y9Yjsn5yDP)
