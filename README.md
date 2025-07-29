# InteractiveRpgMap Plugin Guide

On this Wiki page you’ll find the full reference and setup instructions for using the plugins.

---

## Plugin Load Order

It is **critical** that you keep the following load order in your Plugin Manager:

1. **InteractiveRpgMap**  
2. **InteractiveMapElements**  
3. **InteractiveMapNpc**  
4. **InteractiveMapManager**  
5. **InteractiveRpgMapControls**  

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

### 1. Core Plugin: **InteractiveRpgMap**  
The backbone framework. **Required** by every addon—none will function without it. Here you configure your maps and core settings.

### 2. InteractiveMapElements  
Add and configure **interactive map elements** (buildings, signs, triggers, etc.). Define each element’s interaction here.

### 3. InteractiveMapNpc  
Display **events (NPCs)** on the map. Only events from the **current map** appear (later we’ll support cross‑map data). They behave at runtime (move, face, show only if the player can access that event).

### 4. InteractiveRpgMapControls  
Customize the **map controls** (keys, zoom, open/close behavior).

### 5. InteractiveMapManager  
Utility plugin—**must** be loaded but requires **no configuration**.

---

> **Tip:** Always check the Wiki for the up‑to‑date usage examples, parameter descriptions, and troubleshooting tips!
