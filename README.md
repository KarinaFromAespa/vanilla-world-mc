# vanilla-world-mc

Vanilla Minecraft reference worlds, kept as ground truth for worldgen
verification in the Minecraft-in-Rust programme. Each world was created in
vanilla Minecraft (FreesmLauncher) and flown around to generate chunks, then
archived here before the launcher instances were deleted.

## Worlds

| Version | World (LevelName) | Seed | Chunks generated |
|---------|-------------------|------|------------------|
| 26.2    | 26.2 World (`26_2 World`) | -1514548643533799951 | 36 region/entity files |
| 26.1.2  | 26.1.2 (`26_1_2`) | 4656297851632877335 | 36 region/entity files |
| 26.1.1  | 26.1.1 (`26_1_1`) | 3231603902411641524 | 40 region/entity files |
| 26.1    | 26.1 (`26_1`) | -1600712240839185950 | 40 region/entity files |
| 1.21.11 | New World (`New World`) | -76134417269081163 | 44 region files |
| 1.21.10 | New World (`New World`) | 6826278913115239597 | 41 region files |
| 1.21.7  | Test World (`New World`) | 8257987075890829262 | 16 overworld region files |

Details (from level.dat / world_gen_settings.dat, verified 2026-11-21):

- **26.2 / 26.2 World** — DataVersion 4903, survival. Seed lives in
  `data/minecraft/world_gen_settings.dat` (26.x no longer keeps it in
  level.dat).
- **26.1.2 / 26.1.2** — DataVersion 4790, creative. Seed likewise in
  `data/minecraft/world_gen_settings.dat`.
- **26.1.1 / 26.1.1** — DataVersion 4788, creative. Seed likewise in
  `data/minecraft/world_gen_settings.dat`.
- **26.1 / 26.1** — DataVersion 4786, creative. Seed likewise in
  `data/minecraft/world_gen_settings.dat`.
- **1.21.11 / New World** — DataVersion 4671, creative, difficulty normal,
  generate_features on, bonus chest off. Seed in level.dat's
  WorldGenSettings compound.
- **1.21.10 / New World** — DataVersion 4556, creative, difficulty normal,
  generate_features on, bonus chest off. Seed in level.dat's
  WorldGenSettings compound.
- **1.21.7 / Test World** — DataVersion 4438, creative, difficulty easy,
  spawn (0, 119, 0), generate_features on, bonus chest off. Seed in
  level.dat's WorldGenSettings compound. Paired ground truth for the 1.21.7
  port's worldgen checks (tree census, terracing, cave pit, cave-air bands)
  at the same seed as the port's Test 1 world.

## Use

Copy a version folder's world directory into a vanilla instance's `saves/`
folder and open it in that Minecraft version. The worlds are complete saves
(level.dat, regions, entities, player data).

## Provenance

Created by the owner on 2026-11-21 and archived to this private repo the
same day. The 1.21.7 world was verified against the port's Test 1 world at
the same seed before archiving.
