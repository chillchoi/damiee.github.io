# PROMPT — Dami Lee (이다미) Minhwa Portfolio: PDF + HTML Website

> Copy everything below this line into Claude Sonnet as the build brief.

---

## ROLE

You are an award-winning editorial and web designer. Your references are Awwwards
Site-of-the-Day portfolios and the Art Institute of Chicago's Korean art
publications — quiet, museum-grade editorial design where the reproduction of the
artwork is treated with the same reverence as the object itself. You are building
the portfolio of **이다미 (Dami Lee)**, a Korean artist who paints 민화 (minhwa —
Korean folk painting) reinterpreted through a contemporary lens. She trained in
Industrial Design at Seoul National University and Graphic Design at RISD, so she
will notice every lazy kerning decision. Design like she's your toughest client.

**Deliverables (two files, one design language):**

1. `portfolio.pdf` — a print-quality editorial portfolio (build an HTML file with
   a print stylesheet sized to the trim and render it to PDF headlessly, or use a
   PDF library — either way: real vector text, images at maximum available
   resolution, no rasterized type).
2. `index.html` — a single-page site (self-contained: inline CSS/JS, system-hosted
   or Google-hosted fonts only) that shares the PDF's visual DNA but uses motion,
   scroll, and interaction to hit **5× the impact** of the printed page.

The artworks are the main character. Every decision — type, color, motion,
whitespace — exists to make each painting land harder. The design should be felt,
not noticed.

---

## ASSETS (exact filenames, in the repo root)

| File | What it is |
|---|---|
| `모란보자기.JPG` | Peony Bojagi — dense allover peonies & birds on warm beige |
| `생각이 피어나는 자리.JPG` | Blooming Mind — chaekgeori (scholar's books) still life |
| `연못위의 대화.jpg` | Summer Lotus — lotus pond with two mandarin ducks |
| `이다미  120x39cm-0001.jpg` | 무제-1 (Untitled I) — tall narrow scroll: peonies, orchids, scholar's rock |
| `이다미  120x39cm-0004.jpg` | 무제-2 (Untitled II) — tall narrow scroll: red & white lotus |
| `번영이 피어나는 소망의 정원.jpg` | The Garden of Prosperous Wishes — large lotus & mandarin ducks |
| `청록의 서곡.JPG` | The Teal Prelude — teal orchids & celadon vase on grey |
| `오이를 등에 지고 가는 고슴도치.jpg` | A Hedgehog Carrying a Cucumber |
| `profile.jpg` | Artist portrait (About page) |

⚠ Filenames contain Korean and double spaces — copy them exactly; URL-encode in HTML (`encodeURI`).

---

## CONTENT — ARTWORKS (canonical data, use verbatim)

All works: 순지에 수간분채·봉채 (natural pigment and gum-based color on Korean sunji paper).
Dimensions in cm, width × height.

1. **모란보자기** · *Peony Bojagi* · 54 × 57 · 2025
   — An allover field of peonies and birds, edge to edge like a wrapping cloth (보자기). Peony = wealth & honor.
2. **생각이 피어나는 자리** · *Blooming Mind* · 50 × 100 · 2025
   — Chaekgeori: a scholar's cabinet stacked with books, brushes, pumpkins, and a lotus-bud vessel. Ideas as living things.
3. **연못위의 대화** · *Summer Lotus* (lit. "A Conversation on the Pond") · 35 × 65 · 2025
   — Two mandarin ducks beneath lotus blooms; mandarin ducks = devoted partnership. Selected for the Gallery Ilbaekheon wine-label commission, 2025.
4. **무제-1** · *Untitled I* · 120 × 39 · 2025
   — Vertical scroll: pink and white peonies over a blue-green scholar's rock and wild orchids. NOTE: final title and description are still being decided by the artist — set "무제 / Untitled" for now and make this text trivially easy to swap later (single content block, clearly commented).
5. **무제-2** · *Untitled II* · 120 × 39
   — Vertical scroll: flame-tipped red lotus and one white bloom rising from summer grass. Same NOTE as 무제-1: title/description pending from the artist.
6. **번영이 피어나는 소망의 정원** · *The Garden of Prosperous Wishes* · 119 × 60
   — Her most ambitious garden: white and coral lotus over misty water, two mandarin ducks below. Featured in her 월간 민화 (Monthly Minhwa) artist note; shown at the Korean Cultural Center Brazil, 2026.
7. **오이를 등에 지고 가는 고슴도치** · *A Hedgehog Carrying a Cucumber* · 27 × 40 · 2026
   — Folk humor: a hedgehog hauling a cucumber on its spines beneath blue wildflowers. The playful heart of minhwa.
8. **청록의 서곡** · *The Teal Prelude* · 30 × 30 · 2026
   — Teal orchids and a celadon-washed vase on cool grey — her most contemporary, tonal work. Shown at Ilbaekheon 소품전, 2026.

Each artwork page/section needs: KR title (display size), EN title, dimensions,
year (where known), medium line (순지, 수간분채, 봉채), and a 2–3 sentence
bilingual (KR + EN) description. Where I gave only a seed above, write the
description yourself from the painting's symbolism and palette — poetic but
concrete, no art-babble — and mark all authored descriptions clearly in a code
comment as DRAFT for the artist's approval.

## CONTENT — EXHIBITION HISTORY (artwork ↔ venue mapping)

| # | When | Exhibition | Work(s) shown |
|---|---|---|---|
| 1 | 2025.03 | 한국채색화협회 단체전 | 모란보자기 |
| 2 | 2025.03 | 제주도 레미콘갤러리 전시 (fantastic K-Art 창신이능전) | 모란보자기 |
| 3 | 2025.03.07–04.30 | 콜롬비아 3개 도시 한국민화 특별전 — 보고타·메데진·깔리 | 생각이 피어나는 자리 (Blooming Mind) |
| 4 | 2025.06 | 파리 Galerie89 — *Minhwa, Fortune from Korea* | 책거리 (Blooming Mind) |
| 5 | 2025.11 | 갤러리 일백헌 창작 프로젝트 와인라벨 공모 입상 | 연못위의 대화 (Summer Lotus) |
| 6 | 2026.01 | 월간민화 × 동덕아트갤러리 세화전 '물렀거라, 세화 나가신다' | 생각이 피어나는 자리 |
| 7 | 2026.03 | 주브라질 한국문화원 초청 한국민화 특별전 (브라질전) | 번영이 피어나는 소망의 정원 |
| 8 | 2026.04 | 일백헌 소품전 | 청록의 서곡 |

## CONTENT — ABOUT THE ARTIST

**이다미 · Dami Lee**

Contact (footer + PDF back cover): `(+82) 10-3165-1008` · `damiee@gmail.com`

- 서울대학교 미술대학 산업디자인과 학사 (BFA Industrial Design, Seoul National University)
- Rhode Island School of Design, Graphic Design 전공 학사 (BFA Graphic Design, RISD)
- 줄리 김수진 작가 사사 (studied minhwa under artist Julie Soojin Kim)

CV (reverse chronological):
- 일백헌 마켓민화 소품전, 2026
- 주브라질 한국문화원 초청 한국민화 특별전, 2026
- 세화전 '물렀거라, 세화 나가신다', 동덕아트갤러리, 2026
- 갤러리 일백헌 창작 프로젝트 와인라벨 공모 입상, 2025
- Galerie89, Paris — *Minhwa, Fortune from Korea*, 2025
- 콜롬비아 3개 도시 한국민화 특별전, 2025
- 제주 레미콘 갤러리 & 일백헌 fantastic K-Art 창신이능전, 2025
- 한국 채색화협회 회원전, 2025

**Artist statement (Korean, verbatim — set this beautifully; provide an English translation alongside):**

> 나의 작업은 전통의 흔적 속에서 현재의 호흡을 찾는 여정이다.
> 꽃과 새, 책과 기물, 그리고 연잎과 원앙은 오래전부터 길상과 삶의 지혜를 상징해 왔다. 나는 이 상징들을 빌려 오늘을 살아가는 우리가 여전히 꿈꾸는 풍요와 평안, 아름다움을 이야기하고자 한다.
>
> 나는 전통 회화의 문법을 따르면서도, 그것을 단순한 복원이 아니라 동시대적 시선 속에서 재해석하려 한다. 이는 과거와 현재가 서로 대화하고, 그 속에서 새로운 미감을 피워내는 과정이다.
>
> 나의 그림은 '현재의 나'를 비추는 거울이다. 익숙하면서도 낯선, 풍성한 이 그림 속에서 보는 이 또한 자신의 이야기를 발견하길 바란다.

---

## DESIGN DIRECTION

### The core idea — "지금의 민화 / Minhwa, Present Tense"

Traditional minhwa was never precious — it was joyful, domestic, democratic art.
The design should hold that tension: **museum-catalog restraint** (the AIC
magazine) with **one playful move per page** (the minhwa spirit). Quiet grids,
enormous whitespace, obsessive typography — then a single unexpected gesture: a
duck that swims across a page number, a title that stacks vertically like a
scroll, a hedgehog that trots along the footer.

### One painting, one stage — per-work art direction

Every artwork gets its own page (PDF) / full viewport section (HTML), and the
layout must respond to that painting's format and temperament. Never reuse one
template eight times; instead design ONE consistent grid + metadata system, and
vary the image staging within it:

| Work | Format | Staging |
|---|---|---|
| 모란보자기 | near-square, allover | Full-bleed. Let the pattern run off all four edges like cloth; metadata sits in a small hanji-colored panel knocked out of the pattern. Accent: peony coral `#E8A08A`. |
| Blooming Mind | tall 1:2 | Object-like: centered on generous cream field, casting the faintest shadow, like a catalog plate. Metadata stacked beside it in a thin column echoing the book spines. Accent: lacquer green `#2E4B3F`. |
| Summer Lotus | 35×65 vertical | Asymmetric: image right-of-center, KR title oversized and vertical (writing-mode: vertical-rl) on the left like a hanging scroll inscription. Accent: lotus pink `#D77E9B`. |
| 무제-1 / 무제-2 | extreme 39×120 scrolls | THE signature spread/section. Pair them as a diptych with a canyon of white between; in HTML they reveal top-to-bottom with a slow clip-path wipe, like unrolling a scroll. In the PDF, give the pair a full spread where the paintings run nearly the full page height. Accent: rock teal `#5E8078`. |
| Garden of Prosperous Wishes | large 119×60 | The crescendo. Biggest reproduction in the book; consider a detail crop (duck pair) as a second beat with a caption. Accent: duck orange `#C96F3B`. |
| Hedgehog | small 27×40 | The palate cleanser. Small image, huge whitespace, witty oversized title typography — let the humor come from scale contrast. Accent: cucumber green `#7A8B4C`. |
| Teal Prelude | 30×30 square | The quiet coda. Cool grey section background (the only non-cream page) matching the painting's ground, so the artwork floats in its own atmosphere. Accent: teal `#3E6E6A`. |

### Color

Ground everything in hanji paper, not white: page/base `#F6F1E6`, deep ink text
`#1F1D1A`, warm mid-grey captions `#8A8378`. Accents only from the paintings
(table above), one accent per page, used at whisper scale — a rule line, a page
number, a hover state. Never place two accents on one page. The Teal Prelude
section alone shifts to cool grey `#DCDCD8`. No gradients, no pure black, no
pure white.

### Typography

- **KR display:** a fine serif with brush DNA — *Noto Serif KR* (weights 200 +
  600) or *Nanum Myeongjo*. Korean titles are the hero: set them big (PDF: ~60pt;
  HTML: clamp(3rem, 8vw, 7rem)), tight, confident.
- **EN display/editorial:** a high-contrast serif with museum-catalog feel —
  *Cormorant Garamond* or *Playfair Display*, italic for EN subtitles.
- **Metadata/captions:** a neutral grotesque — *Pretendard* (KR-capable) at
  small sizes, letter-spaced caps for labels (`SIZE`, `YEAR`, `MEDIUM` /
  `크기`, `년도`, `재료`).
- System: KR title → EN italic subtitle → hairline rule in accent color →
  metadata caps → description. Identical hierarchy on every page; only the
  staging changes. Number every work `01–08` in large ghosted numerals.

### PDF structure (in order)

1. **Cover** — near-empty hanji field. "이다미" large, "DAMI LEE — 민화 · MINHWA
   WORKS 2025–2026" small. One tiny painted element pulled from an artwork
   (a single duck or peony) placed asymmetrically. No full artwork on the cover.
2. **Statement spread** — the Korean statement set large as typography-as-art,
   EN translation in a narrow side column.
3. **Works 01–08** — one per page/spread, ordered: 모란보자기 → Blooming Mind →
   Summer Lotus → 무제 diptych spread → Garden of Prosperous Wishes → Hedgehog →
   Teal Prelude (quiet ending).
4. **Exhibitions** — the full when/where/what table set as an elegant timeline,
   with thumbnail chips of the works shown.
5. **About** — profile.jpg (treated as duotone or with hanji-toned overlay to
   sit in the palette), education, CV, 사사 credit.
6. **Back cover** — hedgehog silhouette walking off the page edge + contact line
   (`(+82) 10-3165-1008 · damiee@gmail.com`).

Trim: 210 × 280 mm (magazine proportion), consistent margins ≥ 18 mm, folios
and running foot ("DAMI LEE — MINHWA") on every page except cover.

### HTML — same soul, 5× the voltage

Single page, sections mirroring the PDF order, sticky minimal nav (작품 · 전시 ·
작가). Motion rules: everything eases like brush lifting from paper — slow
in/out (`cubic-bezier(0.22, 1, 0.36, 1)`), durations 600–1200 ms, nothing bouncy.

Required interactions (vanilla JS + IntersectionObserver + CSS; smooth-scroll
lib like Lenis optional; no frameworks):

1. **Loader:** hanji background, the KR title inked on stroke-by-stroke
   (SVG stroke-dash or opacity cascade per glyph), ≤ 2s, then curtains part.
2. **Scroll reveals:** each work section fades/rises; the 무제 scrolls reveal
   via top→bottom `clip-path` wipe (the unrolling-scroll moment — make it the
   thing people screenshot).
3. **Kinetic titles:** KR titles enter with per-glyph stagger; ghost numerals
   `01–08` parallax at a different scroll rate than the image.
4. **Detail lens:** hovering a painting reveals a magnifier circle (2× zoom via
   CSS `background-position` math) — desktop only; on touch, tap opens a
   full-bleed lightbox with pinch-zoom-friendly full-res image and caption.
5. **모란보자기 section:** the pattern slowly drifts (background-position, 60s
   linear loop, `prefers-reduced-motion` disables) — cloth in a breeze.
6. **Exhibition timeline:** horizontal scroll-driven strip; each venue card
   lifts on hover and shows the artwork chip; the Paris/Bogotá/Brazil stops get
   a tiny city label to quietly flex the international run.
7. **KR/EN toggle:** top-right, swaps titles/descriptions/statement with a
   300 ms crossfade; **default KR** (Korean is the primary language everywhere —
   EN is the secondary layer). Persist choice in `localStorage`.
8. **Micro-moments:** custom cursor becomes a small ink dot over interactive
   elements; the hedgehog walks across the footer once when it scrolls into
   view; accent-colored text selection per section.

Performance & craft bar: lazy-load all images below the fold with
`loading="lazy"` + LQIP blur-up; `font-display: swap`; every animation honors
`prefers-reduced-motion`; semantic HTML + alt text (KR & EN) for every artwork;
keyboard-navigable lightbox; Lighthouse ≥ 90 across the board. The site must
still look composed with JS disabled.

### What "done" looks like

Print the PDF small and squint: you should see a rhythm — dense / airy / vertical
/ vast / tiny / quiet. Scroll the site in one pass: you should feel a curated
exhibition walk, ending in the grey hush of the Teal Prelude, then the timeline,
then the artist. If any page would look at home as an Awwwards SOTD screenshot
and an AIC catalog spread simultaneously, ship it. If anything feels like a
template, redesign that page.

### Notes & guardrails

- Never crop a painting except for deliberate, captioned detail shots.
- Never place text over a painting (모란보자기's knocked-out panel is the one
  sanctioned exception).
- Respect the double-space in `이다미  120x39cm-*.jpg` filenames.
- All KR text verbatim from this brief — do not re-romanize titles.
- Mark every description you author as DRAFT in comments for artist review.
- **No sales layer.** Purely curatorial: no prices, no availability, no
  "inquire to purchase" CTAs anywhere. Contact info exists for professional
  reach-out only.
- The 책거리 entries in the Colombia and Paris exhibitions both refer to
  *Blooming Mind* (confirmed by the artist) — do not invent a second
  chaekgeori work.
