# Databricks Champion — Rupert Parchment

## Live deck (share this link)

After GitHub Pages is enabled:

**https://rupertparchment.github.io/Champion/**

Panelists can open that URL on any device — no install required. Use arrow keys or swipe; **F** for fullscreen. **Start** (bottom-left) returns to the title slide.

---

All deliverables for your **45-minute panel / peer review** live in this folder.

## Deck structure — two stories

**`index.html`** is organized chronologically:

| Section | Slides | Content |
|---------|--------|---------|
| Opening | 0–3 | Title, intro, **Two Stories** agenda, journey |
| **Story 1** | 4–8 | **Accenture Federal / DoD** — architecture, gov governance, impact |
| **Story 2** | 9–18 | **Blueprint / Partner** — NXP, **Liquid Clustering**, **KUDU/compute lesson**, MDFSG |
| Closing | 19–23 | Why Lakehouse, features, community, thank you |

See **`SPEAKER-NOTES.md`** for ~10 min + ~12 min timing per story.

## Start here

| File | Use |
|------|-----|
| **`Rupert Parchment - Databricks Champion Panel Review.pptx`** | Main presentation — matches colleague template structure |
| **`SPEAKER-NOTES.md`** | 30-min walkthrough + Q&A bank aligned to program guide |
| **`index.html`** | Browser rehearsal — double-click or `start index.html` |
| **`CONTENT.yaml`** | Structured content source of truth |
| **`Nick Fill DBX Champion Panel Review.pptx`** | Style/structure reference |
| **`Databricks Partner Champions Program Guide.pdf`** | Official requirements |

## Quick commands

```powershell
cd "C:\Users\rparc\OneDrive\Databricks\Champion"

# Open main deck
start "Rupert Parchment - Databricks Champion Panel Review.pptx"

# Animated diagrams gallery (browser)
start diagrams.html

# Browser rehearsal deck (includes animated SVG slides)
start index.html

# Generate / refresh animated GIFs for PowerPoint
python create_animated_gifs.py

# Embed GIFs into PowerPoint (close PPT first if open)
python add_diagrams_to_pptx.py

# Re-apply text updates to main PowerPoint
python update_rupert_deck.py
```

## Animated diagrams

| Asset | Type | Use |
|-------|------|-----|
| `assets/lakehouse-flow-animated.svg` | Animated SVG | **Story 1** — Accenture DoD (`index.html` ~6) |
| `assets/nxp-lift-shift-animated.svg` | Animated SVG | **Story 2** — NXP migration (~11) |
| `assets/metadata-framework-flow-animated.svg` | Animated SVG | **Story 2** — MDFSG framework (~14) |
| `assets/warehouse-lake-lakehouse-animated.svg` | Animated SVG | Optional evolution reference |
| `assets/data-intelligence-platform.png` | Static PNG | **Same as PPT slide 11** (Nick's deck) |
| `assets/*.gif` | Animated GIF | **Insert into PowerPoint** — loops in slideshow |
| `diagrams.html` | Gallery page | Preview all flows in one place |

**Why text-only before?** Slide 11 already had the PNG in Nick's template, but slide 9 used a **Visio OLE object** (only animates inside PowerPoint with Visio installed). The HTML deck and our scripts didn't copy that. Run `python add_diagrams_to_pptx.py` to replace slide 9 with an animated GIF and ensure slide 11 has the Data Intelligence Platform image.

## What was personalized

Based on **`DataEngineerRP-2026.docx`** and your started deck:

- **Slide 2** — Your bio, certifications, Blueprint role  
- **Slide 3** — Your career timeline (Ceridian → deCor → Mortgage Patriots → Accenture → Blueprint)  
- **Slides 4–10** — Metadata Silver/Gold framework (kept UI/flow images from colleague template)  
- **Slide 12** — Your impact metrics (2+ PB migration, 100B+ rows, etc.)  
- **Slides 13–14** — Community and Champion next steps  
- **Slide 15** — Your contact info (was still Nicholas Fill)  

## Still recommended before the panel

1. Add **source + target architecture diagrams** (required per program guide)  
2. Review slides 6–9 — confirm UI screenshots reflect work you can speak to  
3. Dry-run with a Blueprint Champion using `SPEAKER-NOTES.md`  
4. Prepare **one current + one future** Databricks feature (slide content included in `index.html`)  

## Edit workflow

1. Update **`CONTENT.yaml`** with any new metrics or project details  
2. Run **`python update_rupert_deck.py`** for the main `.pptx`  
3. Manually adjust slides 6–9 images/diagrams in PowerPoint as needed  
