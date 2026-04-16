# ResourceWorld

A high-performance resource world plugin designed for modern Minecraft servers.
Supports automatic world resets, safe teleportation, and flexible biome searching with both GUI and command-based systems.

---

## ✨ Features

* 🌍 **Automatic Resource Worlds**

    * Separate overworld and nether resource worlds
    * Fully resets with a new seed each cycle

* 🔄 **Flexible Reset Scheduling**

    * Daily, weekly, or interval-based resets
    * Per-world time and timezone support

* 🧭 **Dual Biome System**

    * **LIST mode** – GUI-based biome selector with cached scanning
    * **LIVE mode** – on-demand biome search via commands (no cache, minimal lag)

* ⚡ **Performance Optimized**

    * Designed to work with **Chunky** for pregeneration
    * Prevents heavy lag spikes during biome searching and resets

* 🐾 **Pet Support**

    * Tamed pets automatically follow players when leaving resource worlds
    * Prevents pets from being left behind or lost

* 🛡️ **Safe Teleportation**

    * Surface-only teleporting
    * Avoids unsafe blocks and terrain
    * Nether roof protection

* 🎮 **Clean GUI**

    * Simple, configurable interface
    * Optional biome selector menu

* 🧪 **Debug System**

    * Toggleable debug logging
    * Separate categories for commands, teleports, resets, and biomes

---

## ⚠️ Requirements

* **Chunky is strongly recommended (and expected for best performance)**
  Without Chunky, biome searching and world generation may cause noticeable lag spikes.

Download Chunky here: https://modrinth.com/plugin/chunky

---

## ⚙️ Commands

| Command             | Description                        |
| ------------------- | ---------------------------------- |
| `/rw`               | Opens the main GUI                 |
| `/rw tp`            | Random teleport in overworld       |
| `/rw nether`        | Random teleport in nether          |
| `/rw <biome>`       | Teleport to a biome                |
| `/rwbiome <biome>`  | Teleport to a biome                |
| `/rwbiome list`     | View biome list (LIST mode only)   |
| `/rwbiome page <#>` | Change biome page (LIST mode only) |

---

## 🧠 Biome Modes

### LIST Mode

* Uses cached biome scanning
* Enables GUI selector
* Supports `/rwbiome list`

```yml
biome-search:
  mode: "LIST"
```

### LIVE Mode

* No cache, no GUI
* Biomes are searched in real time
* Best performance

```yml
biome-search:
  mode: "LIVE"
```

---

## ⚙️ Configuration Highlights

```yml
features:
  main-gui-enabled: true
  biome-gui-enabled: true
  typed-biome-commands-enabled: true

debug:
  enabled: false
  commands: false
  teleports: false
  resets: false
  biomes: false
```

---

## 🔧 Installation

1. Install **Chunky** (required for best performance)
2. Download ResourceWorld `.jar`
3. Place it in your server's `/plugins` folder
4. Start the server
5. Edit `config.yml` as needed
6. Restart the server

---

## ⚠️ Notes

* Do not use `/reload` — always restart your server
* Make sure only one ResourceWorld jar exists in `/plugins`
* Chunky pregeneration is highly recommended before players join

---

## 📦 Version

**v1.1.0**

* Added dual biome modes (LIST & LIVE)
* Added debug system
* Improved GUI behavior
* Reduced lag during biome searching
* Added pet transfer support
* General bug fixes and stability improvements

---

## 💡 Support

If you run into issues:

* Check that Chunky is installed and running
* Double check your config
* Ensure no duplicate plugin jars exist
* Review console errors carefully

---

## 🐝 Buzzle’s Hive

Built as part of the Buzzle’s Hive ecosystem.
Focused on performance, simplicity, and clean server experiences.
