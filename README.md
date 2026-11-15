# Pip Parker and the Bureau of Lost Things

A complete children's novel, its illustration system, and an interactive flipbook - produced by **Qwen (qwen-4 preview)** running in **[Jouzu](https://shisa.ai)** (shisa.ai's coding-agent harness). This repo ships the **book + the prompts + this README**; the long-form write-up is published separately on dev.to.

Open **`flipbook.html`** in any browser - no server, no dependencies.

---

## The prompts, and what each produced

The whole project came from four short prompts (kept verbatim in [`PROMPT.md`](PROMPT.md)). Reading them in order shows how the artifact grew:

**1 - The book + art brief** (`PROMPT.md`, main section)
A single over-constrained brief: write a *complete* 40-chapter novel (~60k words, per-chapter word windows, an exact final sentence, five plant->payoff pairs, kid-safe rails), then illustrate it as a reusable SVG system (9-character library, locked 8-color palette, identical `<defs>` in every plate).
-> Produced `novel.md`, `chapters/`, and `illustrations/` (library + cover + 40 chapter plates).

**2 - "interactive html ... flipbook style ... all chapters"**
Bind everything into one self-contained reading app.
-> Produced `flipbook.html`: 3D page turns, sound + mute, themes, control dock, SVG export, keyboard nav, mobile mode.

**3 - "split each chapter also into pages"**
Make it read like a real book instead of scrolling walls of text.
-> Chapters paginated into **652 pages** with running heads and folios; zero text overflow at any type size.

**4 - "chapter name above illustration as a break/separate page ... bookmark on left"**
A proper chapter opener and a way to keep your place.
-> Chapter-opener spreads (numeral left, title-above-illustration right) and a left bookmark rail with persistence.

The interesting part isn't any single prompt - it's that the model kept all of these constraints mutually consistent across 63,258 words, 42 SVGs, and a working app, and **tested its own output** (headless Chrome: 0 runtime errors, 0 overflow).

## What's in the repo

```
PROMPT.md           the four prompts, verbatim
README.md           this file
novel.md            the full novel (ends on the exact mandated sentence)
chapters/           ch01-ch40 source markdown
illustrations/      library.svg, cover.svg, ch01-ch40.svg (+ bodies/ scene sources)
flipbook.html       the interactive book (single file)
```

## By the numbers (measured from the Jouzu session trace)

| Metric | Value |
|---|---|
| Novel | 63,258 words - 40 chapters (each 1,400-1,700) |
| Illustrations | 42 SVGs - 9-character library - 8-color palette |
| Flipbook | 1 file - 652 pages |
| Wall clock | ~1 h 42 m - 242 turns - ~256k output tokens |
| Headless runtime errors | 0 |

## Credits & claims

- **Model:** Qwen (qwen-4 preview) - **Harness:** [Jouzu](https://shisa.ai)
- **Write-up:** published on dev.to (link added after publishing).
- One session, one run, one brief - an existence proof of a workflow, **not a benchmark**. It shows long-horizon coherence, constraint-following, and agentic self-verification; it does not show that other models can't do it.