# 이다미 (Dami Lee) Minhwa Portfolio — Single Source of Truth

**Read this file completely before touching anything in this repo.**
It records every client request, restriction, and technical decision made so
far. It supersedes any earlier brief where they conflict.

Last updated: 2026-07-27

---

## 1. What this project is

A portfolio for **이다미 / Dami Lee**, a Korean artist painting 민화 (minhwa,
Korean folk painting) in a contemporary register. She holds a BFA in Industrial
Design (Seoul National University) and a BFA in Graphic Design (RISD), so the
design bar is very high and she notices everything.

Two deliverables, one visual system:

| File | What it is |
|---|---|
| `index.html` | The live single-page website. Self-contained: inline CSS + vanilla JS. |
| `portfolio.pdf` | 12-page screen-viewing portfolio, rendered from `print.html`. |
| `print.html` | Print/PDF source. Not itself published. |

### Repo layout — IMPORTANT

The live site is **`~/Documents/GitHub/damiee.github.io`** (remote:
`chillchoi/damiee.github.io`). Work there.

`~/Documents/GitHub/damiee-art.github.io` is a near-empty leftover; the project
files were moved out of it. A nested `damiee.github.io/damiee-art.github.io/`
folder holds a backup including the 324 MB source PDF — it is **gitignored**
because GitHub rejects files over 100 MB.

Also gitignored: the raw artwork photographs (originals up to 27 MB each) and
`__audit_*.html` / `_qa_tmp.html` QA scratch renders. The site serves only the
optimized derivatives in `assets/`.

### Build command (the only supported way to render the PDF)

```
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless \
  --disable-gpu --no-sandbox \
  --print-to-pdf="<REPO>/portfolio.pdf" \
  --print-to-pdf-no-header --no-pdf-header-footer \
  "file://<REPO>/print.html"
```

Verify afterwards with PyMuPDF: 12 pages, every page 210×280 mm, and the
embedded fonts must be `NotoSerifKR` / `NotoSansKR` / `CormorantGaramond`
subsets. **If you see `AppleMyungjo`, the embedded font block is broken.**

---

## 2. THE CLIENT'S ABSOLUTE RULES

Each of these came from the client directly, usually as a complaint. Treat them
as non-negotiable. Violating one is a defect, not a judgement call.

1. **No word is ever split across two lines**, Korean or English. Korean wraps
   on word boundaries (`word-break: keep-all`). This includes values like
   `50 × 100cm` and `순지에 수간분채·봉채` — never break inside them.
2. **Letters from different lines must never collide or touch.** Display type
   needs real leading; a tight `line-height` makes descenders hit the next
   line's ascenders.
3. **No decorative line patterns.** No fleck squiggles, no motif watermarks in
   the old generic corner style, no wavy "deckle" dividers, and no visible
   texture tile seams or grid lines. The client called these *"way too low
   quality"* and said *"I'd rather not have them."*
4. **No em dashes (—) or en dashes (–) anywhere.** Use `·` or a plain hyphen.
5. **No grey boxes or hard grey rectangles around artworks.**
6. **Every PDF page is the same size and orientation: 210×280 mm portrait.**
   No landscape spreads, no mixing.
7. **Nothing may cover, overlap, or sit on top of any painting** — no text, no
   numerals, no panels, no UI. Every painting is shown **whole, uncropped, and
   as large as the page/viewport allows**. The artwork is the main character.
   The only sanctioned crops are the small collage tiles on the cover, and even
   those now show complete works.
8. **No black seal / stamp boxes.** Page numbers are plain, never boxed chips.
9. **The artist's profile photo is always full colour** — never greyscale,
   duotone, sepia, or colour-washed.
10. **If a work has no English title in the source document, show the Korean
    title even in EN mode.** Works with **no** EN title: `모란보자기`,
    `오이를 등에 지고 가는 고슴도치`, `무제-1`, `무제-2`. The strings
    "Peony Bojagi", "A Hedgehog Carrying a Cucumber", "Untitled I", and
    "Untitled II" were **invented by an earlier pass and are banned**.
    Only these four works have real EN titles: *Blooming Mind*, *Summer Lotus*,
    *The Garden of Prosperous Wishes*, *The Teal Prelude*.
11. **Never write a sentence that is not in the artist's source document.**
    An earlier pass fabricated artwork descriptions, including the claim that
    번영이 피어나는 소망의 정원 was *"featured in a Monthly Minhwa artist note"*
    and was the artist's *"most ambitious"* work. The client's reaction:
    **"THIS NEVER HAPPENED."** All description paragraphs have been deleted.
    Do not reintroduce any. Only title, dimensions, year, medium, and
    exhibition facts from the source are allowed.
12. **No text touches or nearly touches a page edge.** Live text needs
    comfortable clearance from the trim on every side.
13. **Multi-column image collages must end level at the bottom, flush like the
    top — without cropping or distorting any image.**
14. The concept phrase **"지금의 민화" / "Minhwa, Present Tense" is rejected**
    as cheesy. Do not use it.
15. **No year range** like "2025-2026" in the title or cover — the portfolio is
    ongoing and will cover future years.
16. **No sales layer** — no prices, availability, or purchase CTAs. Contact info
    is for professional enquiries only.
17. **Backgrounds should feel like real paper**, but only where that reads as
    genuine material. Where a texture produced visible seams it was removed
    entirely — a clean flat hanji field beats a seamed texture.
18. **The mobile site must be as polished and compatible as the desktop site.**

---

## 3. Verbatim content — do not paraphrase, translate, or invent

All works: **순지에 수간분채·봉채** (natural pigment and gum-based colour on
Korean sunji paper). Dimensions are width × height in cm, written the way the
artist writes them.

| # | KR title | EN title | Size | Year |
|---|---|---|---|---|
| 01 | 모란보자기 | *(none — use KR)* | 54 × 57 | 2025 |
| 02 | 생각이 피어나는 자리 | Blooming Mind | 50 × 100 | 2025 |
| 03 | 연못위의 대화 | Summer Lotus | 35 × 65 | 2025 |
| 04 | 무제-1 | *(none — use KR)* | 120 × 39 | 2025 |
| 05 | 무제-2 | *(none — use KR)* | 120 × 39 | 2025 |
| 06 | 번영이 피어나는 소망의 정원 | The Garden of Prosperous Wishes | 119 × 60 | — |
| 07 | 오이를 등에 지고 가는 고슴도치 | *(none — use KR)* | 27 × 40 | 2026 |
| 08 | 청록의 서곡 | The Teal Prelude | 30 × 30 | 2026 |

**Pending from the artist:** final titles and descriptions for 무제-1 / 무제-2.
They are isolated in a clearly commented block in both files so they are trivial
to swap. Until then they display as `무제`.

### Exhibition history (vertical timeline — the client rejected a horizontal carousel)

| When | Exhibition | Work shown |
|---|---|---|
| 2025.03 | 한국채색화협회 단체전 | 모란보자기 |
| 2025.03 | 제주도 레미콘갤러리 전시 (fantastic K-Art 창신이능전) | 모란보자기 |
| 2025.03.07–04.30 | 콜롬비아 3개 도시 한국민화 특별전 (보고타 · 메데진 · 깔리) | 생각이 피어나는 자리 |
| 2025.06 | 파리 Galerie89 — Minhwa, Fortune from Korea | 책거리 (생각이 피어나는 자리) |
| 2025.11 | 갤러리 일백헌 창작 프로젝트 와인라벨 공모 입상 | 연못위의 대화 |
| 2026.01 | 월간민화 × 동덕아트갤러리 세화전 '물렀거라, 세화 나가신다' | 생각이 피어나는 자리 |
| 2026.03 | 주브라질 한국문화원 초청 한국민화 특별전 | 번영이 피어나는 소망의 정원 |
| 2026.04 | 일백헌 소품전 | 청록의 서곡 |

Both 책거리 entries (Colombia and Paris) refer to **생각이 피어나는 자리** —
artist-confirmed. There is no second chaekgeori work.

### About

- 서울대학교 미술대학 산업디자인과 학사
- Rhode Island School of Design, Graphic Design 전공 학사
- 줄리 김수진 작가 사사

CV, reverse chronological: 일백헌 마켓민화 소품전 2026 · 주브라질 한국문화원
초청 한국민화 특별전 2026 · 세화전 '물렀거라, 세화 나가신다' 2026 · 갤러리
일백헌 창작 프로젝트 와인라벨 공모전 입상 2025 · 파리 Galerie89 Minhwa,
Fortune from Korea 2025 · 콜럼비아 3개 도시 한국민화 특별전 2025 · 제주 레미콘
갤러리 & 일백헌 fantastic K-Art 창신이능전 2025 · 한국 채색화협회 회원전 2025

**Contact:** `(+82) 10-3165-1008` · `damiee@gmail.com`

### Artist statement (verbatim Korean — never edit)

> 나의 작업은 전통의 흔적 속에서 현재의 호흡을 찾는 여정이다.
> 꽃과 새, 책과 기물, 그리고 연잎과 원앙은 오래전부터 길상과 삶의 지혜를 상징해 왔다. 나는 이 상징들을 빌려 오늘을 살아가는 우리가 여전히 꿈꾸는 풍요와 평안, 아름다움을 이야기하고자 한다.
>
> 나는 전통 회화의 문법을 따르면서도, 그것을 단순한 복원이 아니라 동시대적 시선 속에서 재해석하려 한다. 이는 과거와 현재가 서로 대화하고, 그 속에서 새로운 미감을 피워내는 과정이다.
>
> 나의 그림은 '현재의 나'를 비추는 거울이다. 익숙하면서도 낯선, 풍성한 이 그림 속에서 보는 이 또한 자신의 이야기를 발견하길 바란다.

The English statement in the files is a faithful translation of the above and is
marked DRAFT pending the artist's review. It is a translation, not an invention.

---

## 4. Design system

- **Palette:** hanji paper `#F6F1E6`, ink `#1F1D1A`, caption grey `#8A8378`,
  cool grey `#DCDCD8` (used only for 청록의 서곡, whose own ground is grey).
- **Per-work accent, one per section, used at whisper scale:**
  moran `#E8A08A` · bloom `#2E4B3F` · lotus `#D77E9B` · untitled `#5E8078` ·
  garden `#C96F3B` · hedgehog `#7A8B4C` · teal `#3E6E6A`.
  When an accent is used as *text*, blend it toward ink
  (`color-mix(in srgb, var(--accent) 58%, var(--ink) 42%)`) — the raw pastels
  are unreadable on cream.
- **Type:** `Noto Serif KR` 200/600 for KR display, `Cormorant Garamond` for EN
  editorial, `Noto Sans KR` for metadata. Identical in both deliverables.
- **Motion:** `--ease-veil: cubic-bezier(0.16,1,0.3,1)` (expo-out) for the slow
  ceremonial reveals; `--ease: cubic-bezier(0.22,1,0.36,1)` for UI. Everything
  is slow and smooth; nothing snaps. All motion respects
  `prefers-reduced-motion`.

### Cover (both deliverables)

Magazine construction: **the name on the left, a compact contact sheet of every
work on the right.** No sidebar, no vertical inscription, no black seal box, no
year range. Each collage column's width is proportional to `1/(sum of its
images' aspect ratios)`, which makes all columns resolve to the *same height* so
their bottoms line up flush — with no cropping and no distortion.

### Per-work line motifs (website)

Each work has its own thin-line watermark drawn from its own subject: book
spines (생각이 피어나는 자리), water rings and a lotus pad (연못위의 대화),
scroll rods and tassels (무제), duck wakes (번영이 피어나는 소망의 정원), a
cucumber tendril (고슴도치), an orchid vase (청록의 서곡). Set at ~5% opacity at
`z-index: 0`, strictly **below** the artwork layer (`z-index: 1`), so a motif can
never touch a painting. **모란보자기 is deliberately left plain** — its ground is
a different colour and it already carries an allover pattern.

---

## 5. Hard-won technical gotchas — read before "fixing" any of these

These were each a real, diagnosed bug. Reverting any of them reintroduces it.

1. **ICC colour management.** 모란보자기 and 생각이 피어나는 자리 are shot in
   **ProPhoto RGB (ROMM)**; 연못위의 대화 is **Rec.2020**. An early pass
   stripped the profiles without converting, so browsers read wide-gamut pixel
   values as sRGB and everything looked flat and "damp." All assets are now
   generated with `ImageCms.profileToProfile(..., PERCEPTUAL)` into sRGB with
   the profile embedded. **Always colour-convert; never just strip.**
2. **PDF fonts.** `print.html` embeds its fonts as base64 `@font-face` rules.
   Do **not** replace them with Google Fonts `<link>` tags: a network fetch
   races Chrome's PDF snapshot and `font-display: swap` silently falls back to
   AppleMyungjo. The subsets cover exactly the 278 characters used.
3. **`box-shadow` in print.** Chrome's print-to-PDF rasterizes shadows into hard
   grey rectangles. That was the "ugly grey boxes around the artworks."
   **No `box-shadow` anywhere in `print.html`.** Shadows are fine on the website.
4. **Texture tile seams.** Tiling a *scaled* PNG makes Chrome interpolate at the
   tile edges, which prints as a faint grid. Pure per-pixel noise at natural
   size has no low-frequency structure and tiles invisibly — but the print sheet
   now has no grain layer at all, which the client prefers.
5. **Mid-word breaks.** The kinetic title builder emitted every glyph as an
   independent `inline-block` *and* replaced spaces with `U+00A0`, making the
   space the only unbreakable spot and forcing breaks mid-word
   ("The Teal P / relude"). It now groups glyphs **per word** inside
   `.word { display:inline-block; white-space:nowrap }`, with real breakable
   spaces between words.
6. **`flex-grow` values must sum to ≥ 1.** With fractional grows summing to
   0.26, flexbox distributes only 26% of the free space and the columns never
   fill. Normalize the ratios.
7. **IntersectionObserver threshold.** `threshold: 0.12` requires 12% of the
   *target* to be visible, which a section far taller than the viewport can
   never reach — every painting stayed invisible. Use `threshold: 0` with a
   rootMargin.
8. **`body { background: #999 }`** in `print.html` bleeds a hard grey band along
   the trim edge of every page. The body must be the paper colour.
9. **Headless screenshots of lower sections are unreliable.** `#fragment`
   navigation plus `scroll-behavior: smooth` often doesn't complete before the
   snapshot, and scroll-reveal sections photograph blank. To inspect the real
   composed design, write a throwaway copy with a small injected stylesheet that
   forces `.in-view` states and hides the loader, screenshot that, then delete
   it. The in-app Browser pane does **not** fire IntersectionObserver reliably —
   use it for DOM/link assertions, not for reveal states.

---

## 6. Still open

- Final titles + descriptions for **무제-1 / 무제-2** (artist deciding).
- **청록의 서곡** is the one low-resolution original: 1326×1440 px, printed at
  full page width ≈ 160 dpi. Every other painting is 4000–8000 px. A higher-res
  scan would be worth dropping in.
- The English artist-statement translation is marked DRAFT pending artist
  approval.

---

## 7. Working agreement

- The client reviews before anything is pushed; they will say when to commit.
- Do not invent content. If a fact is not in the source document, leave it out
  and say so.
- When a complaint arrives, find the **root cause** rather than nudging a value.
  Nearly every issue above was a real bug, not a taste disagreement.
