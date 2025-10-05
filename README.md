# Overview
An opensource regulation size chess board designed using copilot.

## Finish and color scheme
This board is intended to be produced with ENIG (Electroless Nickel Immersion Gold) so the exposed copper will be plated with a gold finish while masked areas remain covered by soldermask and printed with silkscreen for the white squares.

- A1 is configured to be white (front solder mask covers the A1 square).
- H1 is configured to be gold (front solder mask is removed over the H1 square so the copper will receive ENIG).

Implementation notes
- The 8×8 squares are drawn as filled rectangles in `tf_chess.kicad_pcb`. The visible gold/white pattern is controlled by front solder mask rectangles on the `F.Mask` layer. Squares that have an `F.Mask` rectangle are covered (white), and squares without an `F.Mask` rectangle are mask-open and will plate gold with ENIG.
- To invert or tweak the pattern, edit `tf_chess.kicad_pcb` and add/remove the appropriate `(gr_rect ... (layer "F.Mask") ...)` entries for the target square coordinates.
 
Note on black-and-gold option
- If you prefer a black-and-gold board instead of white-and-gold, invert the pattern so A1 becomes black and H1 remains gold. Practically this means flipping which front mask (`F.Mask`) rectangles are present: add `F.Mask` rectangles for squares you want black (masked) and remove them for squares you want gold (mask-open).

## Credits
- Designed with assistance from GitHub Copilot.
