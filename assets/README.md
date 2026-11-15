# Pixel art slots

Drop PNG files in this folder with the exact names below. Any file that is missing falls back to the drawn vector art, so you can add them one at a time. Nothing else needs to change; the list of slots lives in the `ART` manifest in `index.html`.

**Sizes.** The game shows art at 2x the "pixel size" below (1 art pixel = 2 SVG units), and the scenes snap to whole-number zoom where they fit, so pixels stay square. Make files at exactly the pixel size listed. All files are PNG; "alpha" means a transparent background.

## Scenes

| File | Pixel size | Alpha | What it is |
|---|---|---|---|
| `cell_bg.png` | 160x115 | no | The cell: brick wall, dark arch, stone floor. No bars, no Illithid. Leave the floor ellipse (ward ring) area empty; the glowing ward is drawn over it. |
| `illithid.png` | 80x100 | yes | The Illithid standing, shackled arms down, centred. Its pink eyes and tentacles are baked in, so the vector eye glow and sway are replaced. Chains stay vector. |
| `cell_bars.png` | 160x115 | yes | Foreground iron bars and top beam only. |
| `garret_bg.png` | 160x100 | no | The garret: rafters, floor, window with moonlit skyline, table, map, candle stub (no flame, the flame is animated), staff leaning on the right wall. No wizard, no shutters, no trapdoor. |
| `garret_shutters.png` | 33x37 | yes | Closed shutters over the window, drawn at the window position (shown only when you lie low). |
| `wiz_idle.png` | 60x62 | yes | Wizard standing, hands low. Used when idle, borrowing, or worn. |
| `wiz_reach.png` | 60x62 | yes | Same wizard, right arm reaching out (dominating). Same canvas and feet position as `wiz_idle`. |
| `wiz_head.png` | 60x62 | yes | Same wizard, hands to his head (bracing or feeding). |
| `wiz_sit.png` | 50x52 | yes | Wizard seated, meditating. |
| `wiz_crouch.png` | 42x36 | yes | Wizard crouched in the dark (lying low). |

## Map of Caldreth

| File | Pixel size | Alpha | What it is |
|---|---|---|---|
| `map_bg.png` | 320x260 | no | Walled oval city seen from above: houses, river crossing west to east with three bridges, wall with towers, the Spire's courtyard at the top. No buildings for the institutions; they are drawn on top. |
| `icon_coin.png` | 32x32 | yes | Gilded Consortium: counting house or merchant hall. |
| `icon_watch.png` | 32x32 | yes | Ashen Watch: barracks with crenellations and a red shield. |
| `icon_temple.png` | 32x32 | yes | Temple of the Still Flame: domed temple with a flame. |
| `icon_court.png` | 32x32 | yes | Lantern Court: noble hall with lanterns. |
| `icon_under.png` | 32x32 | yes | Undercroft: arched cellar mouth with a key sigil. |
| `icon_coll.png` | 32x32 | yes | Collegium of the Ninth Seal: academy with a tall central tower. |
| `icon_spire.png` | 36x40 | yes | The Spire: the High Magister's tower, red light at the top. Anchored at the base. |
| `icon_garret.png` | 16x16 | yes | Your garret: tiny gabled house, blue lit window. |
| `tok_locked.png` | 14x14 | yes | Thrall marker, not yet available: dim, grey. |
| `tok_open.png` | 14x14 | yes | Thrall marker, available to take: pale outline. |
| `tok_held.png` | 14x14 | yes | Thrall marker, your thrall: violet glow. Rank is shown by marker size, so draw it centred and filling the canvas. |
| `inquisitor.png` | 16x16 | yes | Inquisitor Maldane Roake: red-black hooded figure with a pale eye. |

Icons sit with their feet at the bottom edge of the canvas, so draw buildings to the bottom row.

## Shared style prompt (paste at the start of every generation)

> Pixel art, dark gothic fantasy, limited palette of 16 colours: near-black violet shadows (#0c0a11, #18141f, #2d2637), muted stone greys (#6a5f78, #a79bb8), accents of arcane violet (#c04de0), cold blue (#5aa0ff), candle amber (#ffb347) and blood red (#e05a4d). Crisp 1-pixel outlines in a darker shade of each fill, no anti-aliasing, no gradients or dithering except sparse, flat shading with one light source from the upper left, no text, no drop shadow, transparent background where marked.

Then add the specific subject, for example: *"Subject: a tall Illithid in tattered robes, shackled at the wrists, glowing pink eyes, four tentacles, front view, 80x100 pixels."*

Tips for consistency: generate every file from one seed or reference image, keep the wizard in all five poses to the same palette and proportions, and run everything through one palette (for example Lospec or an indexed-colour export) after generation. If a generator will not hit exact sizes, make it larger at an exact multiple (for example 4x) and downscale with nearest-neighbour.
