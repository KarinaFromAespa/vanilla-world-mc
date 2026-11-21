# vanilla-world-mc

Vanilla Minecraft reference worlds, kept as ground truth for worldgen
verification in the Minecraft-in-Rust programme. Each world was created in
vanilla Minecraft (FreesmLauncher) and flown around to generate chunks, then
archived here before the launcher instances were deleted.

## Worlds

| Version | World (LevelName) | Seed | Chunks generated |
|---------|-------------------|------|------------------|
| 1.21.7  | Test World (`New World`) | 8257987075890829262 | 16 overworld region files |
| 26.2    | 26.2 World (`26_2 World`) | -1514548643533799951 | 36 region/entity files |
| 26.1.2  | 26.1.2 (`26_1_2`) | 4656297851632877335 | 36 region/entity files |

Details (from level.dat / world_gen_settings.dat, verified 2026-11-21):

- **1.21.7 / Test World** — DataVersion 4438, creative, difficulty easy,
  spawn (0, 119, 0), generate_features on, bonus chest off. Seed lives in
  level.dat's WorldGenSettings compound. Paired ground truth for the 1.21.7
  port's worldgen checks (tree census, terracing, cave pit, cave-air bands)
  at the same seed as the port's Test 1 world.
- **26.2 / 26.2 World** — DataVersion 4903, survival. Seed lives in
  `data/minecraft/world_gen_settings.dat` (26.x no longer keeps it in
  level.dat).
- **26.1.2 / 26.1.2** — DataVersion 4790, creative. Seed likewise in
  `data/minecraft/world_gen_settings.dat`.

## Use

Copy a version folder's world directory into a vanilla instance's `saves/`
folder and open it in that Minecraft version. The worlds are complete saves
(level.dat, regions, entities, player data).

## Provenance

Created by the owner on 2026-11-21 and archived to this private repo the
same day. The 1.21.7 world was verified against the port's Test 1 world at
the same seed before archiving.
