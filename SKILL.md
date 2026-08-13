---
name: atr-options-carousel
description: "Use when creating ATR Instagram carousel or Story visuals."
version: 1.0.0
author: Hermes Agent
license: MIT
metadata:
  project: Active Trading Room / «Сэм про Опционы»
  command_hint: "/atr-carousel"
  sync_policy: "Mirror local updates to the public GitHub repository once configured."
---

# Active Trading Room / «Сэм про Опционы» visual production

## Use when

Use this skill when the user asks for an Instagram carousel, a slide series, a Story, or a Story series for Active Trading Room / «Сэм про Опционы», including requests based on a Telegram post URL or pasted post text.

Default output is final PNGs generated with Hermes `image_generate` using GPT Image 2. Do not use a code/PIL overlay workflow for these project visuals unless the user explicitly asks for a deterministic layout instead.

## Source and narrative

1. If a post URL is supplied, retrieve the original post before writing. Prefer direct extraction. If it fails or the source is rendered/blocked, use the browser or ask the user to paste the post text. Do not invent facts from a URL.
2. Separate source facts from editorial framing. Finance education must not promise returns, issue trade signals, or imply a personal recommendation.
3. Before generating images, produce a slide-by-slide narrative with a clear role for every slide: hook → familiar situation → mechanism → consequence → practical action → CTA.
4. The cover must create a real question, not a vague motivational slogan. Russian must be natural and fully grammatical.
5. Keep a single thought per slide. The user may request `medium` text density, but never turn the slide into a paragraph.

## Mandatory approval gate

Before producing a new series, present:
- final slide texts;
- visual scene for each slide;
- CTA and caption if requested;
- frame count and format.

Wait for the user to approve the narrative unless the user explicitly says to generate immediately.

## Project art direction

### Visual DNA

- Premium realistic editorial tabletop photography, viewed from directly above or a slight top-down angle.
- Matte near-black and dark navy desk surface; quiet deep-green zones of light; dense warm cream paper; restrained brass hardware; black fountain pen or notebook; soft directional studio light.
- The brand green is a deep, natural ATR green, never cyan, luminous, or neon.
- Cream and sand-gold support the palette. Red may appear only as a subdued scenario-line warning, not as a dominant brand color.
- Materials must read as physical: paper grain, clean torn or deckled edges, paper tickets, clips, binder rings, cards and notes. Avoid stock-photo clutter.
- Every slide is a single physical editorial scene. Do not use terminal UI, fake trading dashboards, generic holograms, neon charts, coins, rockets, cash, or fake market data.

### Option-trading visual vocabulary

Use only when it genuinely helps the slide:
- physical ticket marked `CALL` or `PUT`;
- clear payoff curve without fake numeric market data;
- simple option-chain grid with no invented prices or tiny unreadable text;
- card labels such as «СРОК», «СТРАЙК», «ПРЕМИЯ», «ВОЛАТИЛЬНОСТЬ», «СЦЕНАРИЙ», «РИСК»;
- risk plan, calendar, paper scenario paths, or a desk notebook.

`CALL` and `PUT` are accepted professional English terms. Do not transliterate them into «КОЛЛ» or «ПУТ» unless the user asks.

### Typography and hierarchy

- Use a tall, wide, modern grotesk with reliable Russian Cyrillic.
- Large headline: normally 2–4 lines. Make every line grammatical when read in sequence.
- Use cream text on dark backgrounds and black/graphite text on cream paper. Never put light text on a light paper surface.
- Mark only 1–2 semantic anchors in deep ATR green per slide. The rest of the headline stays cream or graphite. Green must guide the reading order, not become decoration.
- Underline, glow, uppercase noise, and more than two accent colors are forbidden.
- Keep lockup «ПРО ОПЦИОНЫ» small and unadorned. Do not put icons, vertical bars, logos, or extra symbols immediately before it.
- The exact Russian text supplied for a slide is mandatory. No extra English labels, gibberish, fabricated data, or ornamental pseudo-text.

## Instagram geometry and blind zones

### Feed carousel

- Preferred format: 4:5, 1080×1350 px. Use the closest provider aspect ratio, then prepare final files at the correct export size if needed.
- Keep every essential headline, subheadline, CTA and lockup within the central safe area: at least 8% inset from left/right, 7% from top, 8% from bottom.
- Do not put key words at the extreme left or right: Instagram profile-grid crops and device UI can reduce the visible side area.
- Keep the cover headline in the upper-middle zone, never tight to the top edge. Keep the CTA legible without needing the caption.
- Leave 6–8% separation between text blocks and scene objects. No letter may touch a paper edge or crop boundary.

### Story and Story series

- Format: 9:16, 1080×1920 px.
- Keep crucial text inside x=90–990 and y=250–1480 px. The top UI zone and bottom 440 px must not carry essential copy.
- If the user plans a native Link sticker, reserve a clean lower-third area roughly y=1420–1700 px with no headline, face, small labels, or important visual data.
- Put the main message in the central 55–65% of the canvas. One Story, one message.

## Generation discipline

1. Generate every final slide from a full consolidated prompt. Do not make a production series by repeatedly chaining image-to-image micro-edits.
2. A targeted edit is permitted only for one isolated correction. If any texture, glyph, object, framing, or compositional quality degrades, reject it and regenerate that slide from scratch.
3. Give every slide a different physical scene, while preserving shared palette, material palette, light direction and type system.
4. Use GPT Image 2 only for final project visuals unless the user explicitly chooses another approach.
5. Every prompt must contain: format; composition; safe margins; material and light; exact approved text; semantic words to accent in green; allowed option vocabulary; forbidden elements.

## QA before delivery

Inspect each PNG and reject it when any condition fails:

- Any Russian word is misspelled, clipped, substituted or unreadable.
- Required words are absent or extra words/pseudo-text appear.
- `CALL` / `PUT` was transliterated despite the supplied text.
- Light text appears on a light paper card or contrast is weak.
- The title, CTA, logo lockup or core object enters an Instagram blind zone.
- The scene has degraded paper texture, muddied typography, duplicated objects, warped hands, fake UI, fake numerical market data, watermarks, coins, cash, rockets or neon glow.
- A slide breaks the series art direction.

Generate one fresh retry with a consolidated prompt. If it still fails, report the precise slide and defect instead of shipping it.

## Final delivery

Deliver individual PNGs in order and an archive. State the actual dimensions and list any rejected/unfinished slides honestly.

## GitHub mirror policy

This local skill has a public GitHub mirror. Whenever this skill or one of its supporting files is changed locally, update the mirror in the same task: sync files, commit, push, then read back the public commit URL. If GitHub authentication or access blocks the push, report it directly and leave the local change intact for the next authenticated sync.
