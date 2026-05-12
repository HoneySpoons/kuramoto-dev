# kuramoto.dev

A small interactive study of emergence, oscillation, and coupled systems. Each piece is a single self-contained HTML file that you can open in a browser.

Live at [kuramoto.dev](https://kuramoto.dev).

## Visualizations

- **Chaos Theory** — Double pendulum with chaos demonstration. Real-time RK4 integration; configurable pendulum count for the divergence demo.
- **The Limit** — Riemann sums approaching definite integrals. Three rules (left, midpoint, right), five functions, live convergence panel.
- **Self Similarity** — Apollonian gasket viewer. Descartes circle theorem, Vieta recursion, integer-curvature mode auto-detection. Soddy-swap drawer for any selected circle.
- **Synchronization** *(planned)* — Kuramoto model of coupled phase oscillators. The synchronization order parameter as the coupling parameter crosses the critical threshold.

## Stack

Vanilla JavaScript, HTML5 Canvas, no framework. Each visualization is a single self-contained HTML file with embedded JS and CSS. The landing page is planned to use three.js for a Lo Shu Rubik's-cube animation.

No build step. No package manager. No dev server required.

## Why "Kuramoto"

Named for [Yoshiki Kuramoto](https://en.wikipedia.org/wiki/Yoshiki_Kuramoto), the Japanese physicist who developed the canonical mathematical model of synchronization. The site studies a small territory of mathematics: chaotic divergence, continuous limits, recursive structure, emergent order. Things that organize without being told to.

## Local development

```bash
git clone https://github.com/HoneySpoons/kuramoto-dev.git
cd kuramoto-dev
```

Open any `.html` file directly in a browser, or run a local static server if you prefer:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Contributions / suggestions

Suggestions and corrections welcome at `hello@kuramoto.dev`.

## License

MIT — see [LICENSE](LICENSE). Use the code freely with attribution.
