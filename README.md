# kuramoto.dev

A small interactive study of emergence, oscillation, and coupled systems. Each piece is a single
self-contained HTML file you can open directly in a browser — no build step, no package manager,
no dev server.

Live at [kuramoto.dev](https://kuramoto.dev).

## Visualizations

- **[Chaos Theory](https://kuramoto.dev/chaos-theory.html)** — Double pendulum. Real-time RK4 integration; configurable pendulum count for the divergence demo. Sensitive dependence on initial conditions, made physical.
- **[The Limit](https://kuramoto.dev/the-limit.html)** — Riemann sums approaching the definite integral. Three rules (left, midpoint, right), five functions, live convergence panel.
- **[Self Similarity](https://kuramoto.dev/self-similarity.html)** — Apollonian gasket viewer. Descartes circle theorem, Vieta recursion, integer-curvature mode auto-detection, Soddy-swap drawer for any selected circle.
- **[Synchronization](https://kuramoto.dev/synchronization.html)** — The Kuramoto model of coupled phase oscillators. The order parameter as coupling crosses the critical threshold, plus an interactive **chimera mode**: under non-local coupling, part of the population locks while part stays incoherent. Reseed it and the incoherent region relocates.
- **[Position · Navigation · Timing](https://kuramoto.dev/pnt.html)** — Kuramoto–Sakaguchi clocks on a sphere, rendered as a satellite constellation. The held middle between lockstep and scatter — a *standing truce*, not a true chimera. Includes **live in-browser sonification**: each clock sounds as it comes round, so you can hear coherence hold.
- **[The Torus](https://kuramoto.dev/torus.html)** — Two coupled angles live on a torus. A winding flow fills the surface, collapses under coupling, and splits into a **locking state** — a coherent arc beside an incoherent one. Euler in the drawer: χ = 0, not the sphere's 2.
- **[The Torus +](https://kuramoto.dev/torus-plus.html)** — An Apollonian gasket revolved into a torus, so a curvature change ripples around as a wave.

*In progress:* **Resonance** (pulling voices out of noise with coupled oscillators) and a lineage card.

Most pages carry a `M A T H` drawer with the equations, the reasoning, and the citations.

## Stack

Vanilla JavaScript. HTML5 Canvas for the 2D pieces; **three.js (r128, from CDN)** for the 3D ones
(PNT, The Torus, The Torus +). Web Audio for the sonification on PNT. No framework, no bundler,
no build step, no package manager — each visualization is one file with its JS and CSS inline.

The only external requests are the three.js CDN script on the 3D pages and a
[GoatCounter](https://www.goatcounter.com/) analytics beacon (cookie-less, no personal data).
Everything else is in the file.

## Lineage

None of the underlying mathematics is mine, and the interactive-explorable form has real precedent.
Worth naming plainly:

- **Kuramoto model** — Yoshiki Kuramoto (1975); **Kuramoto–Sakaguchi** with phase lag — Sakaguchi & Kuramoto (1986).
- **Chimera states** — Kuramoto & Battogtokh, *Nonlin. Phenom. Complex Syst.* (2002); named and analysed by Abrams & Strogatz, *PRL* (2004).
- **Interactive Kuramoto** — Dirk Brockmann and Steven Strogatz's [Complexity Explorables](https://www.complexity-explorables.org/) got there first ("Ride my Kuramotocycle"). Complexity Explorables also has an interactive chimera — *Janus Bunch* — built on Janus oscillators, a different mechanism from the non-local ring used here.
- **Sonifying Kuramoto** — Nolan Lem's territory (Stanford CCRMA).
- **Winding lines / irrational rotation** — Kronecker, Weyl. **Euler characteristic** — Euler, *Elementa doctrinae solidorum* (1758).
- **Descartes circle theorem** — Descartes (1643), Soddy's *The Kiss Precise* (1936).

What I'd claim as fresh is the craft layer, not the discovery: the non-local-ring chimera as a
hands-on toy, shipping the sonification live in-browser next to the visual, and the PNT framing.
If I've missed prior art on any of it, please tell me.

Two honesty notes so nothing here oversells: the PNT card is a **standing truce** (partial coherence
held across the whole field), not a true chimera; and the torus pieces settle to a **locking state**,
which is also not a chimera. A genuine chimera on a curved surface is still on the list.

## How it was built

Written with [Claude Code](https://claude.com/product/claude-code) as the build tool, by a
millwork/CAD professional who is largely self-taught in code. Every mathematical claim on the site
went through an independent verification pass before shipping — the corrections that came back are
part of why the copy hedges where it does.

## Local development

```bash
git clone https://github.com/HoneySpoons/kuramoto-dev.git
cd kuramoto-dev
```

Open any `.html` file directly in a browser, or run a static server if you prefer:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Contributions / suggestions

Corrections to the mathematics are especially welcome — open an issue, or mail `hello@kuramoto.dev`.

## Why "Kuramoto"

Named for [Yoshiki Kuramoto](https://en.wikipedia.org/wiki/Yoshiki_Kuramoto), the physicist who
built the canonical model of synchronization. The site isn't only his work — it studies a small
neighbouring territory: chaotic divergence, continuous limits, recursive structure, emergent order.
Things that organize without being told to.

## License

MIT — see [LICENSE](LICENSE). Use the code freely with attribution.
