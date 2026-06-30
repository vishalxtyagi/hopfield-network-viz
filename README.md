<p align="center">
  <img src="https://shieldcn.dev/header/glow.svg?title=Hopfield+Network+Visualization&subtitle=Interactive+neural+network+visualizations+%E2%80%94+basic+%26+advanced+patterns&logo=simple-icons:jupyter&theme=dark" alt="Hopfield Network Visualization" />
</p>

<p align="center">
  <a href="https://hopfield-network-viz.pages.dev"><img src="https://shieldcn.dev/badge/live%20demo-pages.dev-F38020.svg?logo=cloudflare" alt="Live Demo" /></a>
  <a href="https://github.com/vishalxtyagi/hopfield-network-viz/stargazers"><img src="https://shieldcn.dev/github/stars/vishalxtyagi/hopfield-network-viz.svg" alt="Stars" /></a>
  <a href="https://github.com/vishalxtyagi/hopfield-network-viz"><img src="https://shieldcn.dev/github/license/vishalxtyagi/hopfield-network-viz.svg" alt="License" /></a>
  <img src="https://shieldcn.dev/badge/notebook-Jupyter-F37626.svg?logo=jupyter" alt="Jupyter" />
  <img src="https://shieldcn.dev/badge/deployed-Cloudflare%20Pages-F38020.svg?logo=cloudflare" alt="Cloudflare Pages" />
</p>

---

Interactive Jupyter notebook visualizations of **Hopfield Networks** — a type of recurrent neural network that stores patterns as energy minima and retrieves them through iterative updates.

**🌐 Live:** [hopfield-network-viz.pages.dev](https://hopfield-network-viz.pages.dev)

## What's included

| Notebook | Level | What it explores |
|---|---|---|
| `basic_hopfield_network.ipynb` | Beginner | Pattern storage, Hebbian learning rule, synchronous updates |
| `advance_hopfield_network.ipynb` | Advanced | Capacity limits, spurious states, asynchronous update dynamics |

## Run locally

```bash
# With uv (recommended)
uv run --with notebook jupyter notebook

# Or with pip
pip install -r requirements.txt
jupyter notebook
```

## How Hopfield Networks work

```
Training phase:   Patterns → Weight matrix (Hebbian learning)
Retrieval phase:  Noisy input → Iterative updates → Converge to stored pattern
```

Energy function: `E = -½ ∑ᵢⱼ wᵢⱼ sᵢ sⱼ`

The network settles into the nearest energy minimum — which (ideally) corresponds to a stored pattern.

## Auto-deploy

Every push to `main` converts notebooks to static HTML and deploys to Cloudflare Pages:

```
push to main → GitHub Actions → jupyter nbconvert → wrangler pages deploy
                                                   → hopfield-network-viz.pages.dev
```

---

<p align="center">
  Built by <a href="https://vishalxtyagi.in">Vishal Tyagi</a> ·
  <a href="https://hopfield-network-viz.pages.dev">Live demo</a>
</p>
