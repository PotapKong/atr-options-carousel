---
name: atr-options-carousel
description: "Use when creating ATR carousels, Stories, or branded Telegram covers, including company earnings/report visuals."
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

Use this skill when the user asks for an Instagram carousel, a slide series, a Story, a Story series, or a branded wide Telegram cover for Active Trading Room / «Сэм про Опционы». This includes company earnings/report visuals and requests based on a Telegram post URL or pasted post text.

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

- **The last 30 live covers in @activetradingroom are the primary visual truth.** This is not a beige lifestyle-editorial identity and not a generic office desk.
- **Green is the primary ATR colour, not a decorative accent.** Build the visible field from rich emerald, deep forest green and green-tinted midtones; graphite/charcoal may support contrast, paper edges and typography, but must never dominate the frame. The Story must read as green in a phone feed, not as a black creative with a green line.
- Use the project emerald `#25C26B` as a substantial structural colour: a panel, depth field, illuminated card edge, typographic plane or working surface. Preserve premium contrast with cream/white text and dark graphite details. Avoid black voids and crushed shadows; expose material and headline at ordinary phone brightness.
- Typography: bold condensed uppercase Cyrillic, large white headline, usually 2–5 short grammatical lines. Highlight one semantic anchor in bright green. The small `ПРО ОПЦИОНЫ` lockup is quiet, typically near a lower or side edge.
- Choose the cover mode from the current feed: (a) dark educational key art with a clear green option concept, (b) real portrait of the speaker for an announcement, or (c) content-collage / research-card cover. Do not invent an unrelated fashion/lifestyle scene.
- Interface-like frames, terminals and market-grid textures are allowed only as sparse visual atmosphere with no fabricated prices, ticker tables, tiny unreadable pseudo-text or fake factual data. They must not replace the headline or the core concept.
- **For participant reviews, use Native Proof, not a glossy poster.** Prefer a real supplied Telegram-message crop. If the original screen is unavailable, use only an explicitly editorial, minimal message excerpt with the verified quote, clear source label and no fabricated avatar, username, timestamp, reactions or chat metadata. The Story must say «Что пишут участники» before it asks the viewer to interpret a quote.
- Do not use 3D metal type, generic option tickets, glowing empty CTA boxes or decorative neon arrows as the hero treatment for educational/review Stories. Let the source artifact, one short headline and the platform-native Link sticker carry the frame.
- Physical materials are optional, not default. Use cards, paper, labels or a desk only when the post's idea genuinely needs them; never add a notebook, pen, watch or clip as generic decoration.
- ATR is a serious premium channel about exchange options and trading. Every central object must directly read as an option contract, expiry, option-chain structure, strike, premium, volatility, liquidity, risk or trading workflow.
- No coins, rockets, cash, generic holograms, cyan/neon glow, beige architectural interiors or stock-photo business poses.

### Wide earnings cover template

Use this as the default repeatable format when the post is about a named public company’s quarterly report or earnings call. The approved visual reference is `assets/earnings-cover-approved-zoom.png`; preserve its architecture, not the Zoom-specific wording.

- **Format:** wide Telegram cover, 16:9. Use the closest native landscape generation and verify the exported dimensions before delivery.
- **Composition:** approximately 44% left for company identity and headline, 56% right for one physical earnings object. Keep generous safe margins and a calm empty gap between the two zones.
- **Left zone:** place the current official company logo large at the top or upper-left on a clean dark field. Preserve the official wordmark, colors, proportions, clear space, and current brand rules. Below it, place a bold condensed Russian headline in 2–4 lines. Keep most words white and highlight one semantic line or anchor in ATR green `#25C26B`.
- **Right hero:** a premium physical earnings journal, quarterly-report binder, or results dossier, angled slightly toward the viewer. Its front sheet carries the same official company logo at the top, a restrained divider, and the single word `EARNINGS` below. The object may use black leather, a cool metallic sheet, glass frame, fasteners, and a quiet green underlight, matching the approved example.
- **Project lockup:** top-right, small and quiet: `Сэм Шарипов` in white above `ПРО ОПЦИОНЫ` in green. It must never compete with the company logo or headline.
- **Background:** almost-black graphite with sparse technical grid/topographic texture and faint concentric green rings. Keep it editorial and cinematic, never a fake terminal.
- **Report tension:** show the editorial tension through the physical journal, lighting, page depth, or a second page moving into shadow. Do not invent a numerical chart to explain the thesis.
- **Template discipline:** company logo, headline, light tension, and small report details may change; the left identity/headline zone, right `logo + EARNINGS` journal, top-right project lockup, graphite field, and green accent stay stable across the series.
- **Allowed visible text by default:** official company logo/wordmark, exact approved Russian headline, `EARNINGS`, `Сэм Шарипов`, and `ПРО ОПЦИОНЫ`. Add a ticker, quarter, date, price, or metric only when the user explicitly supplies and approves it.
- **Forbidden:** fake prices, percentages, candles, unsupported charts, terminal UI, extra tickers, pseudo-text, duplicate/mutated logos, random English labels, rockets, coins, cash, cyan neon, and generic trader desks.
- **Generation:** source the current official company logo first, use it and the approved earnings reference in GPT Image 2, then generate one complete PNG. Do not recreate the final cover through code overlays.
- **QA:** inspect every Cyrillic glyph, `EARNINGS`, both logo appearances, brand colors/proportions, project lockup, safe margins, mobile readability, extra text, and visual artifacts. Regenerate any failed asset before delivery.

For the reusable consolidated prompt, use `references/earnings-cover-template.md`.

### Option-trading visual vocabulary

Use only when it genuinely helps the slide:
- physical ticket marked `CALL` or `PUT`;
- clear payoff curve without fake numeric market data;
- simple option-chain grid with no invented prices or tiny unreadable text;
- card labels such as «СРОК», «СТРАЙК», «ПРЕМИЯ», «ВОЛАТИЛЬНОСТЬ», «СЦЕНАРИЙ», «РИСК»;
- risk plan, calendar, paper scenario paths, or a desk notebook.

**Metric-scope gate for quizzes.** Match the visual evidence to the exact unit in the question. A chart of total annual options-market volume cannot illustrate a quiz about a large print in one option contract. For a question about one contract, use a real source crop when available or an explicitly labelled educational option-chain row that highlights `ОБЪЁМ` while avoiding invented market values. The viewer must understand within two seconds that the observed fact belongs to one option, not the whole market.

`CALL` and `PUT` are accepted professional English terms. Do not transliterate them into «КОЛЛ» or «ПУТ» unless the user asks.

### Typography and hierarchy

- Use a tall, wide, modern grotesk with reliable Russian Cyrillic.
- **Default for every standalone cover, including a Telegram poll cover: include a large readable headline that names the topic or asks the poll question.** A text-free cover is allowed only when the user explicitly requests no text or supplies an existing text overlay workflow. A merely decorative object on a dark background is a failed cover, even when it is technically on-brand.
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
