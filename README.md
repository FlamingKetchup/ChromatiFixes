# ChromatiFixes

Various fixes for issues found in some of Reika's mods

Most credit goes to [gamrguy](https://github.com/gamrguy) a.k.a. "RobotLucca" a.k.a. "thegamemaster1234" for creating the original ASM-based ChromatiFixes

Fixes:
- CaveControl
  - Prevents `CaveLoader#getEffectiveBiome` from ever returning a null biome, fixing crashes usually caused by pylon chunk loading (thegamemaster1234)
- ChromatiCraft
  - With `disableArtefactShader` enabled, disables the Artefact shader (unilock)
  - Prevents crashes in `ChromaClientEventController#updateGlowCliffRendering` (thegamemaster1234)
  - Adds support for Xaero's maps where appropriate (unilock)
  - Caches the world directory path used during dungeon generation to make it much faster (FlamingKetchup)
  - Ignores the order progress was made in `ProgressionManager#isProgressionEqual` (unilock)
  - Prevents random ConcurrentModificationExceptions during pylon overlay rendering (thegamemaster1234)
  - Prevents the Lumen Beacon from interfering with itself (thegamemaster1234)
  - Enable Lumen Alveary Humidity and Temperature controls when the Princess is unable to work (as these are designed to allow the Princess to work in the first place) (thegamemaster1234)
  - Prevents crashes caused by Adjacency Cores on neighbor state updates (thegamemaster1234, unilock)
  - Reenables and moves the Item Fabricator transferRect (the thing you click on to open recipes that use the Item Fabricator in NEI) to be over the progress bar (FlamingKetchup)
  - Fix bug preventing recent GTNEI versions from loading ChC reciper handlers (https://github.com/GTNewHorizons/NotEnoughItems/issues/595) (FlamingKetchup)
- DragonAPI
  - With `disableClientSpecificConfigs` enabled, all "client-specific" configs use the same keys across all systems, allowing them to be packaged with modpacks and such (unilock)
- Satisforestry
  - Allow Pressurizer multiblock to receive RotaryCraft power via Power Hub (thegamemaster1234)
- DragonRealmCore
  - With `disableNetherShader` enabled, disables the Nether "heat" shader (unilock)
  - With `disableTerritoryStrongholdSystem` enabled, disables the TerritoryStrongholdSystem (unilock)
  - Prevents NullPointerExceptions caused by Hex Generators (thegamemaster1234)
  - With `energizationManagerFix` enabled, prevents crashes in `EnergizationManager#getEnergizationLevel` (however, the chosen fix prevents playing with the "Atmospheric Permeability Mediation" mechanic) (thegamemaster1234)
