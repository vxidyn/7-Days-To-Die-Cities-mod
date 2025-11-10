
---

## Features

- Adds a new world generation preset: **Max City World (2K All City)**  
- Makes the entire 2K map city blocks — no wilderness or rural zones  
- Fills every possible tile with POIs (max density)  
- Keeps normal biome generation for variety  
- Works in both **RWG Preview** and normal world creation  
- XML-only modlet — no scripts or dependencies

---

## Installation

1. Go to your 7 Days to Die install directory. For Steam users, that’s usually:

C:\Program Files (x86)\Steam\steamapps\common\7 Days To Die\

2. If you don’t already have a **Mods** folder there, create one.
3. Drop the mod folder into it so the structure looks like this:

Mods/
└── MaxCityWorld/
├── ModInfo.xml
└── Config/
└── rwgmixer.xml

4. Start the game or the RWG Preview tool.
5. When you go to generate a new world, pick the preset:

Max City World (2K All City)

6. Choose your seed and generate. It’ll produce a small 2K map that’s nothing but city — every corner covered in POIs, streets, and urban sprawl.

---

## Details

**World Size:** 2048 (2K)  
**City Density:** 100%  
**Town Density:** 100%  
**Wilderness Density:** 0%  
**POI Density:** Maxed (1.0 per tile)  
**Biome Distribution:** Normal (uses vanilla biome layout)

It replaces all rural and wilderness tiles with city hubs and fills every open area with roads and POIs. The world basically becomes one large city grid broken up by biome transitions.

---

## Making Bigger Versions (4K, 8K, 10K)

If you want to make a larger version of this preset, it’s easy. You only need to change one line in the XML file.

1. Open:

Mods/MaxCityWorld/Config/rwgmixer.xml

2. Find this line inside the `<preset>` block:
```xml
<property name="world_size" value="2048"/>

    Change the number:

        4096 for 4K

        8192 for 8K

        10240 for 10K

You can also increase tile size to make sure the city scales correctly:

<property name="max_tiles" value="24"/>
<property name="min_tiles" value="16"/>

Save the file and regenerate the world in RWG Preview.

Note: Bigger worlds look awesome but use more RAM and CPU.
8K and 10K worlds can take several minutes to generate and need good specs (at least 16GB RAM and a modern CPU).
Compatibility

    Tested with 7 Days to Die Alpha 22.4 (b7)

    Works fine with vanilla and most biome/POI expansion mods

    May conflict with other mods that modify rwgmixer.xml

    Requires a new world to take effect (old worlds won’t change)

    Safe to remove any time — it won’t break existing saves

Advanced Tweaks

If you know XML, you can open rwgmixer.xml and play with a few values:

    City count: change min_count and max_count under citylarge or citysmall

    POI density: set <property name="poi_density" value="1.0"/> even higher if the mod you're stacking supports it

    Biome balance: edit biome weighting for more desert or snow

    Trader placement: control where traders appear within city tiles

Experiment — the mod’s clean structure makes it easy to modify.
Credits

    Author: vxidyn

    Base RWG system: The Fun Pimps

    Testing and config help: the 7DTD modding community on 7daystodiemods.com and Reddit

License

This modlet is released under the MIT License.
You can edit it, share it, or expand it freely — just keep credit to the original creator.
Notes

This mod was made for players who want the chaos and atmosphere of a world that never stops being city. There are no wide open fields, no safe zones, and no long drives through empty forests — just streets, rooftops, and constant danger.

If you make your own versions (like larger maps, new biome setups, or themed “industrial” variants), feel free to fork it or upload your changes — just keep the credit line intact.
