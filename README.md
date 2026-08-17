# Landing page: Controlling Uncertainty and Hallucination Risk in Multi-Agent Fact Verification

Static landing page for the UAI 2026 paper by Adam Kostka and Jarosław A. Chudziak
(Warsaw University of Technology).

**Live:** https://feilaz.github.io/uai2026/

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole page. Plain HTML, no JavaScript. |
| `style.css` | Single stylesheet. Mobile-first, dark-mode aware. No framework. |
| `poster.pdf` | Conference poster (A0 portrait, 277 KB). |
| `qr.png` / `qr.svg` | QR code pointing at the live page. Use the SVG for print. |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is, without Jekyll. |

## How to change things

Everything is edited by hand; there is no build step. Commit to `main` and
GitHub Pages redeploys within about a minute.

- **Replace the poster:** overwrite `poster.pdf`, keeping the filename so the
  QR code and any printed links stay valid. Update the size shown in the
  Poster button in `index.html` if it changes noticeably.
- **Add a code link:** `index.html` contains a commented-out `Code` button
  inside the `<nav class="links">` block. Uncomment it and set the URL. The
  repository must be **public** or visitors will get a 404.
- **Regenerate the QR code** (only needed if the URL changes):

  ```sh
  qrencode -o qr.png -s 12 -m 3 -l M "https://feilaz.github.io/uai2026/"
  qrencode -t SVG -o qr.svg -s 12 -m 3 -l M "https://feilaz.github.io/uai2026/"
  ```

- **Preview locally:**

  ```sh
  python3 -m http.server 8000    # then open http://localhost:8000
  ```

## Notes

- The QR code points at this page rather than directly at `poster.pdf`, so the
  poster file, links and contact details can be changed after printing.
- The description text is taken verbatim from the poster; the abstract is taken
  verbatim from the published PMLR version (v337, pages 3143–3161).
