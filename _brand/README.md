# Brand

Working files for the Stuart Pearson, LPC identity.

## GEOMETRY.md

The mark's full construction spec. Everything derives from the arm radius `r = 11`, so
the asterism can be rebuilt at any scale by a printer or sign maker from that file
alone, with no access to the source art.

## proofs/ — present on disk, deliberately not committed

The design record lives at `_brand/proofs/` on this machine and is listed in
`.gitignore`. **This repo is public.** The proofs contain candid working notes about
positioning and one carries a license number, so they are kept off GitHub. They are
plain standalone HTML; open any of them in a browser.

| Proof | What it settled |
|---|---|
| `1-wordmark-specimens.html` | Six typographic directions. Chose the press colophon. |
| `2-colophon-studies.html` | Warmed the colophon in five steps. Chose small caps, flush left. |
| `3-proof-marks.html` | Ten editorial marks as the device. Chose the asterism. |
| `4-asterism-geometry.html` | Why six points rather than five. Settled rotation and terminals. |
| `5-asterism-proof.html` | Final proof: fixed geometry, three optical sizes, lockups. |

Because they are untracked, they exist in one place only. Back them up with the rest of
the practice files rather than relying on git.

## Deployed assets

The mark itself is committed, in `img/`, because the site references it.

| File | Use |
|---|---|
| `asterism-display.svg` | The mark above 48px. Signage, letterhead. |
| `asterism-text.svg` | The mark at 20 to 48px. **This is the nav.** |
| `asterism-small.svg` | The mark below 20px. |
| `asterisk-display.svg` | Single asterisk, the small form, large cut. |
| `favicon.svg` | Single asterisk, optically corrected for 16px. |

The three asterism cuts are **not interchangeable**. They are the same coordinates with
different arm weights and tip radii; scaling one to do another's job is the one way to
break the mark. `GEOMETRY.md` says which to use where.

## Still open

The nav wordmark is the site's original text treatment, not the Cardo small-caps
wordmark the proofs settled on. Adopting Cardo site-wide means loading a web font on
every page and is a larger change than adding the mark was.
