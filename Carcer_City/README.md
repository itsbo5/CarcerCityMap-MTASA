# Carcer City - MTA:SA Multiplayer Map

A complete conversion of Carcer City into a playable MTA:SA multiplayer map using the eagleLoader streaming system.

## Map Overview

| Detail | Value |
|--------|-------|
| **Map Name** | Carcer City |
| **Zones** | 17 (Clarksland, Lacpoint, CC Interior, Subway, etc.) |
| **Custom Buildings** | ~3,710 |
| **Custom Textures** | 83 TXDs (~655 MB) |
| **Total Resource Size** | ~887 MB |


## Requirements

- **MTA:SA Server** 1.6+
- **eagleLoader** 

## Installation

1. Copy the `Carcer_City` folder into your `mods/deathmatch/resources/` directory
2. Copy the `eagleLoader` folder into the same directory (if not already present)
3. Edit your `mtaserver.conf` or add to ACL:
   ```xml
   <resource src="eagleLoader" startup="1" />
   <resource src="Carcer_City" startup="1" />
   ```
```
start eagleLoader
start Carcer_City
```

## eagleLoader Configuration

In `eagleLoader/config.lua`, ensure these settings for best results:



## Zone List

| Zone | Description |
|------|-------------|
| `clark_gen` | Clarksland general objects & terrain |
| `clark` | Clarksland main buildings |
| `clark_levels` | Clarksland multi-level structures |
| `clark_props` | Clarksland decorative props |
| `clark_props2` | Clarksland additional props |
| `lacE` | Lacpoint East - main city area |
| `lacElevels` | Lacpoint East level structures |
| `lacW` | Lacpoint West - industrial area |
| `lacWlevels` | Lacpoint West level structures |
| `lac_props` | Lacpoint decorative props |
| `lac_props2` | Lacpoint additional props |
| `cc_subway` | Carcer City subway system |
| `cc_interiors` | Interior environments |
| `clk_interior` | Clarksland interiors |
| `dynamic` | Dynamic objects |
| `dynamic2` | Additional dynamic objects |
| `vegepart` | Vegetation & nature |


### Files Structure
```
Carcer_City/
  meta.xml                    -- Resource definition
  eagleZones.txt              -- Zone list for eagleLoader
  water.dat                   -- Water definitions
  interiors.map               -- Interior entry/exit markers
  imgs/
    dff.img                   -- 3D models (191.7 MB)
    col.img                   -- Collision data (38.4 MB)
    txd.img                   -- Textures (654.7 MB)
  zones/
    <zone>/
      <zone>.map              -- Object placements
      <zone>.definition       -- Model definitions (DFF/COL/TXD refs)
```

### Source Files
- **Original Mod**: GTA Carcer City Demo (by the community)
- **Converter**: eagleRemapper by Blue Eagle
- **Loader**: eagleLoader by Blue Eagle


## Credits

- **Blue Eagle** - eagleRemapper & eagleLoader tools
- **GTA Carcer City Demo** - Original mod assets
- **Conversion** - Map converted using eagleRemapper pipeline

