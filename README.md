# piercing_silence
piercing_silence_v1
# Piercing Silence

**A browser-based platformer about sound, paranoia, and the search for quiet.**

Based on the short story by Raj Patel (@rp.heic).

---

Piercing Silence follows Ramesh Pratap — philosopher, insomniac, visiting scholar at UPenn — across six chapters of escalating tinnitus, methamphetamine use, institutional paranoia, and memory intrusion. Every mechanic has a cost. Every relief carries a consequence. The game ends the way the story does.

## Play

Open `index.html` in any modern browser. No build step, no dependencies, no server. Single-file HTML + Canvas + JavaScript.

Works on desktop (keyboard, gamepad) and mobile/tablet (touch controls appear automatically).

**Recommended:** Headphones. The tinnitus tone is part of the experience.

## Controls

| Input | Action |
|---|---|
| ← → / A D | Move |
| ↑ / W / Space | Jump |
| Shift (hold) | Focus — reduces paranoia, slows movement, suppresses shadows. Increases tinnitus. |
| ↓ / S (hold) | Listen — reveals hidden platforms via sonar pulses. Increases tinnitus. Cannot jump. |
| M | Toggle audio mute |
| V | Cycle volume |
| F | Toggle reduced flash mode |
| H | Toggle high contrast HUD |
| Esc | Settings overlay |

Gamepad (DualSense / standard mapping): left stick + d-pad for movement, Cross to jump, L1 to focus, R1 to listen, Triangle or Options to advance screens.

Touch: directional buttons bottom-left, jump/focus/listen bottom-right. Tap top-right corner for settings.

## Chapters

1. **THE CONSTANT HUM** — Late night, Baltimore Avenue. Ramesh's apartment above the Queen of Sheba. The rain helps.
2. **THE BANAL CABAL** — Morning, Locust Walk. Luke Ward and the department's gaze. Stay out of sight.
3. **FRACTURED PERCEPTION** — Evening, the office. The corruption diagrams look like conspiracy maps now. The meth reveals patterns. Or invents them.
4. **THE SHEET** — Dead of night, Kensington & Clearfield. Among the ghouls, one figure stands apart.
5. **ECHOES** — Dawn. Arunachal Pradesh, London, childhood. The past breaks through.
6. **PIERCING SILENCE** — The apartment. Final dawn. The noise must stop.

## Mechanics

**Tinnitus** rises constantly. It drains stability (health) above 0.8. Quiet zones reduce it temporarily — but linger too long and paranoia spikes instead. Listening raises it faster. Focus raises it slowly.

**Paranoia** distorts perception. Above 0.6, platforms begin to flicker — both visually and physically. Enemy gaze cones widen. At high levels, sonar pulses produce phantom echoes.

**Meth** offers temporary clarity: reduced tinnitus, increased speed. The cost is permanent. Each dose degrades jump height and raises the paranoia baseline. What you take in one chapter, you carry into the next.

**Hidden platforms** exist from chapter 2 onward. They're revealed by the Listen sonar mechanic. Sonar pulses illuminate them briefly; paranoia accelerates their fade. At high paranoia while listening, revealed platforms visually drift — the game lies to you about where they are.

**Fragments** are the collectibles. Each type shifts your state differently. Collect all fragments in a chapter, then reach the exit on the right wall.

**Chapter 6** removes jump, removes free movement, and locks tinnitus and paranoia at maximum. You can only move by holding Focus. Each fragment writes a line of the suicide note.

## Accessibility

The settings overlay (Esc or tap top-right) provides:

- **Audio mute** — the game is fully playable without sound
- **Volume cycling** — 30%, 60%, 70%, 90%
- **Reduced flash** — dampens screen shake, tinnitus flashes, distortion noise, and corruption glyphs
- **High contrast HUD** — brighter HUD text and bars against a darker background

The ending screen displays the 988 Suicide & Crisis Lifeline.

## Technical

Single HTML file, ~2400 lines. No frameworks, no bundler, no external assets.

- 800×500 canvas, CSS-scaled to viewport
- Pre-rendered offscreen canvases for tile textures, collectible sprites, and title logo
- Web Audio API: two oscillators (sine + triangle) for tinnitus and meth overlay tones
- 60fps game loop with delta-time-independent physics (fixed timestep via requestAnimationFrame)
- Touch, keyboard, and gamepad input handled simultaneously
- Particle cap (220), sonar pulse cap (10) for consistent performance
- All atmosphere art (buildings, street signs, interiors) drawn procedurally per level

## Content Warning

This game depicts tinnitus, methamphetamine addiction, institutional paranoia, memory of childhood abandonment, and suicide. It does not flinch. The final chapter is a suicide note written one fragment at a time.

If you or someone you know is struggling: **988 Suicide & Crisis Lifeline — call or text 988.**

## Credits

Story, design, and development: **Raj Patel**

Built with Claude (Anthropic).

## License

All rights reserved. This repository is provided for review and portfolio purposes. The source story, game design, narrative content, and code are the intellectual property of Raj Patel. Do not redistribute, modify, or use commercially without permission.
