# ResourceWorld

Automatic resource world resets with safe teleports and configurable scheduling for Paper 1.21.x servers.

---

## Commands

### Players

* `/rw`  
  Opens the ResourceWorld main menu.

* `/rw biome`  
  Displays the available biome list.

* `/rwbiome <biome>`  
  Teleports the player to a specific biome inside the resource world.

---

### Admin / Console

* `/rwreset`  
  Forces a reset of the configured resource world.

---

## Reset Modes

ResourceWorld supports three reset types:

### INTERVAL
Resets every X hours or days.

### DAILY_AT
Resets once per day at a specific time.

### WEEKLY_AT
Resets once per week on a specific day and time.

Example:

```yaml
resets:
  overworld:
    mode: "DAILY_AT"
    timezone: "America/New_York"
    time: "04:00"

/*
 * Buzzle’s Hive Plugin
 * Copyright (c) 2026
 * All Rights Reserved.
 *
 * Unauthorized copying or distribution of this file is strictly prohibited.
 */
