# Iris example dimension

This is a deliberately small teaching pack built for the current Iris format. It contains one dimension, one region, two biomes, and one shared terrain generator. Oceans, caves, objects, decorators, structures, loot, and ores are omitted so the basic resource chain stays obvious.

```text
dimensions/example.json -> regions/main.json
regions/main.json -> biomes/plains.json, biomes/hills/rolling.json
both biomes -> generators/plain.json
```

The file path under each resource folder is its key. For example, `biomes/hills/rolling.json` is referenced as `hills/rolling`.

Start by changing one value at a time:

- Change a biome layer block to learn surface palettes.
- Change a biome generator's `min` and `max` offsets to alter its height above `fluidHeight`.
- Change the generator's `SIMPLEX` zoom to make terrain features broader or tighter.
- Duplicate a biome file, give it a new key, and add that key to `regions/main.json`.

Validate the pack before opening it in Studio:

- Bukkit: `/iris pack validate pack=example`
- Fabric, Forge, or NeoForge: `/iris pack validate example`
