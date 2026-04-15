# InteractiveRpgMap Plugin Guide

On this Repository page you’ll find the full reference and setup instructions for using the plugins.

---

## Plugin Load Order

It is **critical** that you keep the following load order in your Plugin Manager:

0. `Gamemory` *(optional)*  
1. `InteractiveRpgMap`  *(required)*
2. `InteractiveMapElements` *(optional)*  
3. `InteractiveMapNpc` *(optional)*  
4. `InteractiveMapManager` *(optional)*  
5. `InteractiveMapUserMarkers` *(optional)*  
6. `InteractiveMapRouter` *(optional)* 
7. `InteractiveMapNotes` *(optional)* 
8. `InteractiveRpgMapControls` *(required)*

👉 **Navigate here to access the documentation:**  
**[https://github.com/Lonsdale201/rpgmakermyplugins/wiki/Start-Here!](https://github.com/Lonsdale201/rpgmakermyplugins/wiki/Start-Here!)**

---

## What is InteractiveRpgMap?

`InteractiveRpgMap` is a **full‑screen interactive map system** for RPG Maker MV.  With it you can:

- Define a **custom “full‑window” map** for each area.
- **Place interactive elements** (via **InteractiveMapElements**) anywhere on the map.
- Optionally show **events (NPCs)** on the map—with runtime tracking (movement, facing, availability) only for events on the **current map**.
- Configure **global** or **per‑map** settings, including **conditional access** (require item, switch, skill, or actor).
- **Zoom** (3 levels) and **scroll** the map.
- Apply a **custom Window Skin** or **custom frame**.
- Enable **player tracking** (real‑time player position) globally or per map.
- Treat it as a **modal window** (not a minimap): once opened it pauses the lower layers until closed.
- Attach **custom interactions** to map elements (load another map, teleport, run a Common Event, etc.).
- Open a **portrait window** for an element or NPC to show extra data—even NPCs can open a portrait, though other NPC interactions are not yet configurable.

---

## Plugin Components

### Core Foundation

### 1. Core Plugin: **InteractiveRpgMap**
The backbone framework and renderer for the interactive map system. **Required** by all InteractiveMap addons.

### 2. Utility Layer: **InteractiveMapManager**
Core interaction helper (teleport/open-related/common-event/battle routing). Keep it loaded; usually no per-project tuning needed.

### 3. Input Layer: **InteractiveRpgMapControls**
Centralized keybind/control plugin (open map/notes, zoom, pan, marker modifier, delete, route toggle).

---

## Content & Interaction Addons

### 4. **InteractiveMapElements**
Defines clickable map elements (buildings, signs, POIs) and their configured interaction behavior.

### 5. **InteractiveMapNpc**
Projects map events/NPCs onto the interactive map (currently current-map runtime scope), with event-based visibility and portrait/click support.

### 6. **InteractiveMapRouter**
Draws a route line from player position to clicked POIs on configured region networks (with snap/exclude rules and goal marker).

### 7. **InteractiveMapUserMarkers**
Player-created custom markers/notes (Shift+click workflow), persistent per map, with optional consumable cost and delete/edit flow.

### 8. **InteractiveMapNotes**
Map codex-style menu (Info / Elements / Monsters tabs) with visibility rules, intro blocks, list/grid layouts, and pagination.

### 9. **InteractiveMapDebugger** *(dev tool)*
Development-only diagnostic overlay/logger for IRMap event flow and click/input tracing. Not needed in production builds.

---

## Separate System (Progress/Memory)

### **Gamemory** *(separate but integrated)*
Persistent game-memory/stat plugin (visited maps, enemy/troop/battle stats) used by some UI/visibility features (e.g., hide-until-visited / hide-until-defeated).

---


> **Tip:** Always check the Wiki for the up‑to‑date usage examples, parameter descriptions, and troubleshooting tips!
