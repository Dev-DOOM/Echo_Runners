ECHO RUNNERS

"Race against your past. Beat your own route. Discover a better way to run."

Echo Runners is a 45-second top-down arcade courier game built in vanilla HTML5, CSS, and JavaScript (Canvas 2D). You pilot a courier bot to collect energy cells and bank them at an extraction beacon before time runs out. After every completed run, your recorded trajectory spawns as an active Echo Rival on the next run—physically competing against you for the exact same pool of collectibles.

Playable Links

Latest Playable Build (V1.0): https://dev-doom.github.io/Echo_Runners/

Source Code Repository: https://github.com/Dev-DOOM/Echo_Runners

Iterative Version Builds (/versions)
V0.1 Base structure: https://dev-doom.github.io/Echo_Runners/versions/echo_runners_v01.html

V0.2 Fixed (Stable Competitive Echo): https://dev-doom.github.io/Echo_Runners/versions/echo_runners_v02.html

V0.3 (Risk & Reward Arena): https://dev-doom.github.io/Echo_Runners/versions/echo_runners_v03.html

V0.4 Fixed (Multi-District & Daily Seed): https://dev-doom.github.io/Echo_Runners/versions/echo_runners_v04.html

V0.5 (Metagame & Gadget Workshop): https://dev-doom.github.io/Echo_Runners/versions/echo_runners_v05.html

V1.0 Fixed (Complete Release): https://dev-doom.github.io/Echo_Runners/versions/echo_runners_v10_fixed.html

Controls & Core Rules

Move: WASD or Arrow Keys (Mouse / Touch drag also supported)

Activate Gadget: SPACE or E (or click the HUD gadget button)

Run Timer: 45.0 seconds per run

Scoring:

Banked Cell (Delivered at green DROP beacon): +100 pts per unit

Carried Cell (Unbanked at timeout): +15 pts per unit

High-Value Orange Core (3x): Worth +3 cargo units (300 pts banked)

Development Version History

The prototype was built incrementally, validating stability and core loop feel at every milestone before adding new systems:

V0.1 — Core Loop Prototype

Built the foundational 45-second collection-and-delivery loop on HTML5 Canvas.

Implemented normalized 8-directional movement, distance-based collectible pickups, extraction beacon banking, local high-score persistence, and a visual-only ghost replay of the previous run.

V0.2 Fixed — Stable Competitive Echo (echo_runners_v02_fixed.html)

Upgraded the Echo from a passive visual ghost into a physical competitor that steals energy cells and banks points independently.

Resolved early frame-freeze issues by rebuilding Echo playback with O(log n) bitwise binary search interpolation across 70ms timestamp samples, enforcing a single requestAnimationFrame loop, and validating localStorage route JSON.

V0.3 — Risk & Reward Gameplay (echo_runners_v03.html)

Introduced solid rectangular wall obstacles to create distinct safe perimeter paths versus inner shortcuts.

Added the red EMP Slow Zone (45% movement penalty), high-value 3x Energy Cores placed in high-risk zones, and shared Speed Boost Pads (1.45x speed for 2.5s on a 6s cooldown) that both the player and Echo can trigger.

V0.4 Fixed — Replayability & Challenge Layer (echo_runners_v04_fixed.html)

Added 3 Selectable District Arenas (Sector Alpha, Twin Gates, and Core Reactor), each with isolated Echo and personal-best persistence.

Implemented the Echo Rival Target Toggle (Previous Run Echo vs. Personal Best Echo), a deterministic Daily Fixed-Seed Mode (mulberry32 PRNG), 3 trackable Courier Contracts, and a 5-run session history log.

V0.5 — Progression & Metagame (echo_runners_v05.html)

Added a Courier Credits (CC) economy earned from run scores, Echo victories, and contract completions.

Built the Courier Workshop featuring 3 balanced active gadgets on a 14-second cooldown (Phase Dash, Pulse Magnet, and EMP Shield) alongside 3 unlockable cosmetic chassis and trail themes (Cyber Cyan, Solar Crimson, and Neon Emerald).

V1.0 Fixed — Complete Playable Release (index.html / echo_runners_v10_fixed.html)

Added a zero-asset Web Audio API Synthesizer for procedural pickup, banking, boost, gadget, and countdown sound effects (with HUD mute toggle).

Polished game feel with floating score popups, particle bursts, beacon delivery shockwaves, subtle screen shake, contextual first-run onboarding prompts, and a live HUD lead indicator.
