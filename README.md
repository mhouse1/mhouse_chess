# MHouse Chess Board — Production-Ready AI-Assisted Design

This is an **open-source, regulation-size chess board** designed using KiCad 9.0 with AI assistance (GitHub Copilot). The design includes **full fabrication outputs** ([v3 folder](./v3/)), making it **ready for manufacturing** with ENIG (Electroless Nickel Immersion Gold) finish.

---

## Finish and Color Scheme

- **White-and-gold design**:
  - Squares with front solder mask (`F.Mask`) remain white.
  - Mask-open squares plate gold via ENIG.
  - A1 = white, H1 = gold.

- **Black-and-gold option**:
  - Flip mask rectangles so A1 becomes black, H1 remains gold.

## Design Goals

- **Simple & flat**: a minimal-profile board for comfortable play and easy storage.
- **Gold-and-white color scheme**: aesthetic choice implemented via ENIG gold plating and white solder mask.
- **Dual-side functionality**:
  - One side is intentionally simple and uncluttered for standard play.
  - The other side includes an identification marker on each square (beyond the usual rank/file labels) to aid setup, teaching, and accessibility.

---

## Implementation Notes

- The 8×8 squares are drawn as filled rectangles in `tf_chess.kicad_pcb`.
- Visible pattern is controlled via `F.Mask` layer rectangles.
- To tweak the pattern:
  1. Edit `tf_chess.kicad_pcb`
  2. Add/remove `(gr_rect ... (layer "F.Mask") ...)` entries for desired squares.
- Full fabrication outputs are included in the `v3/` folder (or `v3.zip`) — **ready for production**.

## Usage
- Upload `v3.zip` (or files in `v3/`) directly to a PCB manufacturer such as JLCPCB to produce the board.

---

## AI Experiment Context

This board was created to **benchmark AI-assisted hardware design workflows**.
- The design took **a few hours with AI** versus weeks of manual KiCad work.
- The key takeaway: AI significantly compresses design time, but **human oversight and cost evaluation remain critical**.
- Current fabrication costs (including tariffs) are ~$50/unit for small runs (5 boards), compared to typical expected costs of <$25/unit for this scale.

---

## Credits

- Designed with assistance from GitHub Copilot.
