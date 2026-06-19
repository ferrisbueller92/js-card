# Just Sorted — Digital Business Card

Dave Calder · Co-founder, Just Sorted. A self-contained, mobile-first HTML business
card you show in person. Two stylised QR codes (website + LinkedIn), tap-to-call,
tap-to-email, and a downloadable vCard.

**Live:** https://ferrisbueller92.github.io/js-card/

Built with the same engine as `ferrisbueller92/nah-card`. Brand tokens sourced from
the Just Sorted brand bible (warm-earth palette · Anton + DM Sans + Space Mono).

## Contents
| File | Purpose |
|------|---------|
| `index.html` | The card (no JS, no build step) |
| `qr-website.png` | QR → justsorted.com.au (js. logo centre, error-correction H) |
| `qr-linkedin.png` | QR → linkedin.com/company/justsorted |
| `dave-calder.vcf` | vCard 3.0 — "Save my contact" |
| `js-logo.png` / `favicon.png` | js. monogram |

## Card details
- **Name / role:** Dave Calder · Co-founder
- **Tagline:** "Take back your week." (justsorted.com.au hero)
- **Phone:** +61 422 616 829 · **Email:** hello@justsorted.com.au
- **QRs decode-verified** (OpenCV) and scan-safe with the centre logo.

## Regenerate the QRs
```bash
python tools/branded_qr.py clean "https://justsorted.com.au" qr-website.png --logo js-logo.png
python tools/branded_qr.py clean "https://www.linkedin.com/company/justsorted" qr-linkedin.png --logo js-logo.png
```
