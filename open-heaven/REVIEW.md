# REVIEW — Open Heaven (storyline A)

Render: `renders/open-heaven.mp4`: H.264, 1920×1080, 30 fps, 20.0 s, delivery quality.

## Creative calls
- The film is one continuous take through four worlds. Each world is entered through an opening in the last: the door in the sky (Rev 4:1), the crystal firmament (Ezek 1:22), the wheels within wheels with eyes on their rims (Ezek 1:16–18), and the sea of glass before the throne (Rev 4:2–6).
- **The throne:** no figure sits on it. "Like a jasper and a sardine stone" is drawn as cut facets of white, jasper and sardius-red light. The emerald rainbow rises above the sea floor, and its reflection in the glass completes the circle "round about" the throne. Seven lamps are lit before it, and 24 crowned elders in white sit around it (Rev 4:4–5).
- **Words:** all scripture on screen is quoted verbatim from the KJV: Rev 4:1, 4:1, 4:6 and 4:8. I dropped a planned Ezekiel line so the wheels speak for themselves.
- **Font:** EB Garamond (bundled) replaces the Cormorant Garamond named in the storyline, so no font file was needed.
- **GSAP:** stored locally at `assets/vendor/gsap.min.js`, because this container's render browser can't reach the CDN.
- **Storylines not built:** B, "Wheels Within Wheels" (Ezekiel 1 as a 3D flight), and C, "The City Coming Down" (Rev 21 built from type). Both are in `STORYLINES.md`.

## What was checked
- **Measured:** `hyperframes check` passes with 0 errors. The file was verified with ffprobe for duration, size and frame rate.
- **Looked at:** frames at 0, 1.5, 3.2, 4.0, 4.4, 5.5, 7.3, 7.8, 9, 10, 10.6, 12.5, 14, 15.4, 16.2, 19.5 and 19.75 s, plus the rendered frames on either side of every handoff (4.6, 6.9, 8.05, 10.7–11.0 s). Every handoff is continuous.
- **Fixed after the first look:**
  - The rainbow circle and its reflection cut through "HOLY". It is now a bow above the sea floor with a reflection that fades out.
  - The seats read as a fence. They are now spread wider and deeper, with darker backs.
  - The sea read flat. It now has more tile contrast.
  - The light shaft on the hills read as a muddy road. It was removed.

## Warnings kept on purpose
- **`film_silent`:** there is no music source here (no HeyGen sign-in, no local music model), and worship use usually means the church's own song. Add a track as `<audio id="music" src="assets/music.mp3" data-start="0" data-volume="1">` in `index.html`, then re-render.
- **`canvas_content_at_edge`:** the canvas is the full-bleed background, so touching the edge is intended.
- **`composition_file_too_large`:** `heavens.html` holds the whole continuous take as one `render(t)`. Splitting it would break the single camera.

## Weakest shot
- The sea of glass from 11 to 14 s: the throne is small for about three seconds while the glass tiles carry the shot. With more time I would add real reflections of the sky into the tiles, or bring the throne closer sooner.
- The amber "fire infolding itself" arcs behind the wheels are close to decorative rings.
