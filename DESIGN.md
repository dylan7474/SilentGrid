html/javascript game losely based on computer battleships but with submarines, boats, planes, etc. the game is played from the submarines, calling in air strikes for sonar or visually detected subsmarins and boats, turn based with mutliple assets with actions with a bit of a civilisation style. The players are ww2 based with axis and allies. Upgrades are available by salvaging opponents wrekages. This is a starter for the game outline so feel free to expand this prompt into a more deatiled outline and feature set and maybe produce some sample grapghics based on a few potential styles. Don't write any code yet. 

Game Design Document: Gritty Top-Down Edition
1. The Core Gameplay Loop
The player starts with a small "Wolfpack" (1–2 submarines) on a dark, hexagonal grid shrouded in Fog of War. You must complete Objectives (e.g., intercepting a convoy, sabotaging a harbor) while surviving enemy hunters, primarily Destroyer Escorts, which use passive sonar to hunt your active visual and auditory footprint.

                  ┌──────────────────────┐
                  │   Fog of War Grid    │
                  └──────────┬───────────┘
                             ▼
         Is the player Detected? ───[YES]───► High Danger (Evasive AP Actions)
                             │
                            [NO]
                             ▼
     [PASSIVE SONAR] (Detection) / [ACTIVE SCAN] (Reveal)
                             │
                             ▼
                  Identify Target & Attack
                             │
                             ▼
              [SALVAGE WRECK] ──► mid-battle upgrades
2. Expanded Mechanics: Active Depth & Stealth States
To lean into the submarine-specific gameplay, each your own sub units can toggle between 3 specific depths—each offering unique tactical tradeoffs:

Surfaced (Highest AP, Most Vulnerable): Fully visible. Highly vulnerable to airstrikes, torpedoes, and deck gun fire. Recharges batteries and regenerates air. Allow the sub to travel much faster (lower AP per movement hex) and salvage wreckages directly.

Periscope Depth (Moderate Stealth, Combat Ready): Barely visible. Allows you to visually spot enemy vessels without active sonar, making you much harder to detect. Crucial for firing unguided torpedoes and launching reconnaissance assets. Very slow, and you must manage your "Surveillance" and battery.

Deep Submerged (Max Stealth, Blind): Fully invisible except to nearby active sonar/depth charges. Relies entirely on passive "sound" tracking (cannot visually see targets). Rapidly drains the air/battery meter. Useful for slipping past hunters or escaping a deadly engagement.

3. Asset Breakdown & Support Systems
Rather than being just a sub game, players coordinate an entire multi-asset fleet over a wider theater:

Allied Faction (USN & RN)
Submarine: Standard "USS Gato" or "Gudgeon" class with average stats, good radar, and rapid reloading.

PBY Catalina (Recon Aircraft): Casts a wide recon sweep on the grid, peeling back Fog of War for 1 turn. Can occasionally drop a single "Sonar Buoy" to monitor a sector over multiple turns.

Airstrike (B-24 Liberator): Heavy bombing run on a known, visually-spotted target. Deferrable, taking 1 full turn to arrive.

Sub-Chaser (Surfaced Support): Small Allied patrol boats that assist in scanning and tracking Axis movements on the edge of your network.

Axis Faction (Kriegsmarine)
Submarine: Type VII or Type IX U-Boat with superior stealth, advanced torpedo configurations, and high damage output.

Bv 138 (Recon Flight): Patrols high-altitude. Exceptional scanning and visual spotting range, but expensive to call in.

Stuka / Condor (Strike): Faster, high-precision air sweeps. Devastating to exposed, isolated enemy merchant ships.

S-Boot (E-Boat): Quick patrol boats used for rapid harassment and distraction, enabling Wolfpack attacks.

4. Salvage, Upgrades & The Tech Loop (Mid-Battle Evolution)
Destroyed ships and submarines create Salvage Tiles on the map, represented as oil slicks, debris, and floating hulls. Send a surfaced sub to a debris field and spend AP to "Salvage" the area. This gathers resources:

Material Scrap: Used for hulls, plating, and structural repairs.

Captured Intel: High-value intelligence spent to upgrade your detection, submersibles, and technology.

Upgrade Types (Submarines Only)
Acoustic Coating (Stealth): Reduced chance of passive sonar detection.

Enhanced Batteries: Stay submerged deep for 1.5x longer without needing to surface for air.

Torpedo Upgrades: Increase range, add magnetic sensors (ignores armour), or fire homing "Acoustic" torpedoes.

Anti-Air / Deck Guns: Surfaced sub defense against scouting aircraft and light vessels.

Detailed Gameplay Interface Illustration
To demonstrate how the tactical "battleships with subs and planes" perspective should look on screen, I've designed a gameplay visual depicting Option 4: a gritty, storm-tossed top-down scenario. It captures the complex turn-based UI, showing hexagonal grid patterns, sonar tracking sweeps, target locks on enemy destroyers, and air support.gritty top-down WW2 naval strategy game view of an Allied submarine sub in stormy sea, strategy UI overlaid with grid and targeting graphics, calling in an airstrike, cinematics, realistic ocean texture, hand-drawn look but high fidelity with weather effects, scanlines, and digital tracking hud showing UI for subs, boats, planes, salvage, upgrading status, AP meters, active turn, status metrics, UI panels, immersive dark tone. At twilight, heavily textured ocean surface under dramatic cinematic stormy lighting. A submarine cuts through crashing foam. Multiple asset selections and target tracks. Combat UI around, including 'SURFACE', 'DIVES', 'PING', 'BOMBER AIRSTRIKE', 'UPGRADE LAB', 'SALVAGE TILE SIGHTING'. A radar sweep and flight trajectory of a calling recon plane visible on visual HUD overlay. Action Points (AP) and battery stats on top. Low key color palette of dark blue, grey, with glowing amber/green. High detailed interface. Fine rain and water particles visual overlay. Fine visual lines. No code overlays. Beautiful turn-based view of a wolfpack tactical operation. High fidelity. I can generate some mock gameplay visuals based on this. Let's start with a view showing an engagement where a sub spots an enemy and is calling in support, all inside the UI system of a browser game. Let's show this interface
