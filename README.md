# DungeonMod / The Hollow Below

Procedural dungeon-room generator with reusable, swappable texture materials.

## Current build
**Room Forge 2.3 — Lynocs integration**: all 21 supplied texture archives have been processed into a compact working material library containing **219 diffuse texture variations**. The browser demo uses Canvas 2D, with named material slots: `floor`, `wall`, `trim`, `wood`, `metal`.

The full working project and offline HTML are delivered as conversation artifacts. Download the editable project ZIP, extract it, and run `python build_standalone.py` to regenerate the standalone HTML.

## Source project structure
- `src/engine.js`: procedural layout, face generation and texture-mapped renderer
- `src/index.template.html`: room builder / material library UI
- `manifest.json`: curated presets and 21 collection presets
- `texture-library.json`: index of all 219 diffuse variations and source archive references
- `assets/full_library/`: 256-pixel JPEG working copies, one for each diffuse texture
- `build_standalone.py`: bundles source and textures into offline HTML

## Important distinctions
The Canvas renderer currently uses diffuse textures only. Additional normal, height and related material maps remain in the source archives for future WebGL rendering. No room artwork is baked into a background: each rendered face references one material slot.

## License and attribution
Texture source: [Lynocs Texture Pack](https://lynocs.itch.io/texture-pack), advertised CC0. Review source terms before repackaging the texture library on its own.

## Integration status
This repository was initially empty. The source project is supplied in the ZIP; GitHub files can be added from the archive. This README alone does not mean the entire asset library has been committed to GitHub.
