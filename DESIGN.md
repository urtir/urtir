# DESIGN — urtir profile README

## World
Cyber-maximalism / terminal-brutalist sticker wall. Single surface: GitHub profile `README.md`.

## Palette
| Role | Hex |
|------|-----|
| Ground | `#000000` / GitHub `#0d1117` (dark), `#FAFAFA` (light) |
| Primary | `#00FF41` (acid green) |
| Secondary | `#FF00FF` (magenta), `#FFE600` (yellow), `#FF3333` / `#FF6633` (alert) |
| Text | `#E0E0E0` dark / `#111111` light |

## Type
- Display: monospace ASCII banner (block characters) in fenced code.
- Headings: GitHub markdown `#` + `═══` rules. No soft kickers.
- Body: default GitHub sans; badges carry color, not CSS (GitHub strips `<style>`).

## Components
- **Badge sticker** — shields.io `for-the-badge` / `flat-square`, hard `labelColor=000000`, no gradients.
- **Skill strip** — skillicons strips by category (AI/ML, backend, data/cloud, sec/os). Only verified icon IDs; broken IDs (`sql`, `burp`, `jupyter` as skillicon) → shields instead.
- **Stats grid** — HTML `<table>` with fixed `width` % cells (34/33/33), `valign="top"`, `<picture>` for theme.
- **Research table** — HTML table, `th width=68% / 32%`, venue as color-coded shields (not plain text).
- **Rules** — `═══` section bars, `---` markdown HR. No rounded cards, glass, gradient text.

## Hard rules
- No `<style>`, no custom CSS, no AI-slop pastel hero, no empty centered “Hi I’m”.
- Every skillicons URL verified live (non-empty SVG, no `undefined`).
- Table columns always get explicit `width` attributes.
- alt text on every `<img>`; decorative footer badge alt present.

## Finish evidence
- `impeccable detect --json README.md` → `[]`
- Tag balance check → all open/close pairs OK
- Live URL probe → all skillicons strips OK; sample shields 200
