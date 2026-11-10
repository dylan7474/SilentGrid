# SilentGrid

A turn-based WW2 submarine strategy game that runs in your browser. Command a U-boat on a hex grid under fog of war, call in air support, sink Allied convoys and survive the destroyer hunting you.

**Play:** https://dylan7474.github.io/SilentGrid

No install or build. It is a single `index.html` (Three.js, Tailwind and Phosphor icons load from CDNs). To run it locally, serve the folder, e.g. `python -m http.server`, and open `index.html`.

## Objective

Sink **3 merchant convoys** within **35 turns**. You lose if your hull reaches 0 or the turns run out.

## How to play

You get **10 Action Points (AP)** each turn. Spend them, then press **End Turn**; the enemy then moves.

| Action | Cost | What it does |
|---|---|---|
| **Move** | 1 AP surfaced, 2 AP submerged | Click an adjacent hex. |
| **Surface / Periscope / Deep Dive** | 1 / 2 / 2 AP | Change depth (see below). |
| **Active Ping** | 2 AP | Reveals contacts within 4 hexes, but alerts the destroyer to your position. |
| **Torpedo** | 3 AP (2 with Hydraulic Rammer) | Click a hex up to 3 away. 55 damage. You carry 4. |
| **Recon Sweep** | 3 AP | A Catalina reveals the clicked hex and its neighbours. |
| **Airstrike** | 4 AP (3 with Enigma Air Radio) | Bombs a hex you have visually confirmed (by recon). 70 damage. |
| **Salvage** | 2 AP | Surfaced, on a wreck: gain Scrap and Intel. |
| **Upgrades** | free | Spend Scrap and Intel on permanent upgrades. |

Click an action button first, then click the target hex. Actions that need a target stay selected until used.

### Depth

- **Surfaced** – fastest and recharges the battery, reloads one torpedo per turn, and is the only depth where you can salvage. The destroyer hunts you from anywhere, and depth charges do the most damage.
- **Periscope** – balanced stealth and vision. The battery drains 15% per turn (recharges with the Snorkel).
- **Deep Dive** – hardest to hit and reduces depth-charge damage, but the battery drains 25% per turn. At 0% the boat is forced to the surface.

### The destroyer

HMS Bulldog hunts you if you are surfaced, have pinged, or come within 2 hexes. Once adjacent it drops depth charges every turn: 45 hull damage if you are surfaced, 35 at periscope depth, 18 deep. Sink it with two torpedoes, or run.

### Salvage and upgrades

Sunk ships leave wrecks. Surface on one and salvage it for Scrap and Intel, then spend them in the Upgrades screen: Electric Snorkel, Hydraulic Rammer, Enigma Air Radio and Zaunkönig Homing Heads (listed, not yet implemented).

## Status

Early prototype. See [DESIGN.md](DESIGN.md) for the fuller vision: Allied and Axis factions, more asset types and a bigger tech loop.

## License

[MIT](LICENSE.md)
