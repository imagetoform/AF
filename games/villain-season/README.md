# Villain Season

An original side-scrolling platformer about a masked MC fighting the music industry. One HTML file, no build step, no dependencies. Open `index.html` in a browser.

## Controls
| Action | Keys | Touch |
|---|---|---|
| Move | ← → / A D | ◀ ▶ |
| Jump | Space / ↑ / W | JUMP |
| Spit (shoot words) | Z / J / X | SPIT |
| Pause / Mute | P / M | — |

## The core idea: words are weapons, rhythm is power
The game runs a boom-bap drum machine, synthesized live in Web Audio. If you spit off the beat, you throw a small word (`bars`, `flow`). If you spit on the beat (watch the ring in the top-centre HUD), you throw a craft term (`CAESURA`, `ASSONANCE`) for double damage. Four on-beat shots in a row turn the flow gold: `ENJAMBMENT!` hits for triple damage and pierces through enemies. Your words also cancel enemy contracts in mid-air ("REJECTED").

## Levels and bosses
1. **Rooftops** → **The Hype Machine**, a walking speaker stack (jump its shockwaves, duck the high blasts)
2. **Underground** → **The Ghostwriter**, who teleports and fires homing quills, and can only be hit while solid
3. **The Tower** → **Mr. Major, C.E.O.**, at a flying desk. He throws contracts, rains cash, and sends interns. Hit him from the platforms or when he swoops down.

## Enemies and pickups
- Wack MCs (patrol), Hype Men (jump at you), Label Execs (throw contracts), Bootleg CDs (fly)
- Vinyl = points · Boombox = +1 health · Golden Mic = 12 s of triple-spread bars · Spray can = tag the wall, checkpoint

## Testing hook
`index.html?level=2` jumps straight to a level.
