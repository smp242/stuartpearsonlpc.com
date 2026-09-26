# The asterism mark — geometry

Everything below derives from one number, the arm radius `r = 11`. Any sign maker,
printer or developer can rebuild the mark at any scale from this page alone. No font
is involved and no tracing is required: the mark is nine straight rules and eighteen
circles.

## Concept

An **asterism** is three asterisks set in a triangle, used in typesetting to mark a
break in thought between passages. Not a chapter end and not a full stop: a held pause
where the subject is allowed to change direction.

## The single asterisk

Three rules of length `2r`, crossing at their midpoints, at **0°, 60° and 120°**.

Six points, never five. An odd number of points has to be built from spokes radiating
out of a hub, and a hub with rays reads as a star or an insignia. An even number is
built from whole rules passing through a centre, which reads as punctuation. This is
the whole reason the mark is six-pointed.

**Flat axis.** One arm is horizontal; nothing points straight up. Rotating the
asterisk 30° puts a point at the top and it immediately reads as a star. Do not rotate
it.

No interior shape is ever enclosed, which is what keeps a six-pointed figure legible as
an asterisk rather than a hexagram.

## The asterism

Three asterisks with their centres on an **equilateral triangle of side 28** (`2.55r`),
**point up** — one above two.

| Asterisk | Centre |
|---|---|
| top | `(32, 12.83)` |
| bottom left | `(18, 37.08)` |
| bottom right | `(46, 37.08)` |

Nearest tips of adjacent asterisks are `6` apart: close enough to read as one object,
open enough that the arms never appear to touch.

Canonical viewBox: `0 0 64 50`.

Arm endpoints for an asterisk centred at `(cx, cy)`, where `dx = 5.5` and `dy = 9.53`
(that is `r·cos60` and `r·sin60`):

```
horizontal   (cx - 11, cy)      →  (cx + 11, cy)
60 degrees   (cx - dx, cy - dy) →  (cx + dx, cy + dy)
120 degrees  (cx + dx, cy - dy) →  (cx - dx, cy + dy)
```

A filled circle sits at each of the eighteen arm ends, centred exactly on the endpoint.

## Optical sizes

The terminals are teardrops: hairline arms swelling to a round tip. That detail does
not survive being scaled, so the mark ships as **three cuts of the same coordinates**.
Only the arm weight and the tip radius change. **Never scale one cut to do another
cut's job** — scaled down the arms go sub-pixel and vanish, scaled up they go clumsy.

| Cut | Use at | Arm weight | Tip radius | File |
|---|---|---|---|---|
| Display | above 48px | 1.0 | 1.75 | `img/asterism-display.svg` |
| Text | 20 to 48px | 1.5 | 2.1 | `img/asterism-text.svg` |
| Small | below 20px | 2.2 | 2.7 | `img/asterism-small.svg` |

The ratio of arm weight to tip radius is what makes the mark look drawn rather than
plotted. Keep it.

## The small form

Below about 24px the asterism fails: eighteen arms cannot resolve in sixteen pixels,
and no amount of weight fixes it. Under that size use a **single asterisk** instead.
This is a normal large-form / small-form pair, not a compromise.

- `img/asterisk-display.svg` — arm radius 9, weight 1.0, tips 1.75
- `img/favicon.svg` — arm radius 8.5, weight 2.0, tips 2.6, optically corrected for 16px

The favicon arms are inset slightly (radius 8.5 rather than 9) to leave room for the
heavier tips inside the same box.

## Clear space and lockup

- **Clear space:** minimum `r` on all four sides. Nothing sets inside it, including the
  wordmark.
- **Lockup:** mark to the left of the wordmark, its centre on the optical centre of the
  two-line block. Gap between mark and wordmark is `2r`, the width of one asterisk.
- **Centred variant** exists for documents; flush left is the everyday mark.

## Colour

| | Value |
|---|---|
| Sage (the mark) | `#5c7a6e` |
| Paper | `#f9f7f4` |
| Ink | `#2c2c2c` |
| Wash (tile ground) | `#eaf0ee` |

One flat ink where colour is unavailable: solid black on white, which is how it prints
on a superbill or a fax cover. Reversed (paper on sage) is approved for square tiles.

## The wordmark

Cardo, hand-built small caps, flush left, uppercase with `letter-spacing: 0.17em`. Small
caps are built as a full-size initial followed by the remaining letters at `0.74em` with
`letter-spacing: 0.23em`, rather than relying on an OpenType `smcp` feature the web font
may not carry.

Credential sits beneath in the site's utility sans, uppercase, `letter-spacing: 0.26em`,
in sage.

## What this replaces

Nothing. There was no prior mark and no favicon.
