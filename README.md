# RIGID — Paper website

Project page for **Relational Spatial Alignment for Vision-Language-Action Models**.

This `gh-pages` branch contains a self-contained static website. No package installation, JavaScript framework, or build step is required.

## Preview

Open `index.html` directly, or run:

```sh
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## GitHub Pages

The intended public address is https://qm-ipalab.github.io/RIGID/.

Push this branch with `git push -u origin gh-pages`. In the repository's **Settings → Pages**, select **Deploy from a branch**, **gh-pages**, and **/ (root)**. The `.nojekyll` file enables plain static serving. All page asset paths are relative, including the URL-encoded original supplementary-video filename.

## Content and sources

The content follows the supplied local manuscript in `../corl-2026-rigid`, with the author's names and affiliations supplied in the task. Author links are taken from `../LaVA-Man` and the supplied Chenglin Cui and Taein Kwon URLs. Yazhe Wan is shown without a link because no verified personal homepage was provided or found.

| Section | Source | Website treatment |
| --- | --- | --- |
| Motivation | Figure 1; Introduction; Method §3.1 | Three concise lines and the original two-panel figure |
| Abstract | Abstract; Method; Simulation; Real-world experiments | Shortened, evidence-grounded abstract |
| Method Overview | Figure 2; Method §3.2 | Original framework figure and attention/optimal-transport explanation |
| Experiment Results | Tables 1 and 2 (`tables/libero_comb.tex`) | Original tables cropped together from manuscript page 6, preserving all rows, typography, highlighting, and captions |
| Real-world Experiments | Figures 7 and 8; Real-world experiments | Original setup/results figures and the supplied supplementary video |

Figure 1 and Figure 8 are cropped from manuscript pages 2 and 9 to preserve the original LaTeX plots. Tables 1 and 2 are cropped from page 6 and exported as a lossless WebP image without retypesetting. Figures 2 and 7 are rendered from `imgs/framework.pdf` and `imgs/real_robot_setup2.pdf`. WebP images can be opened at full resolution by clicking them. `static/papers/rigid.pdf` is the supplied manuscript, including its supplement, copied unchanged. The original MP4 is also unchanged.

## Editorial checks

- **Contribution:** relational spatial alignment, rather than a new backbone; supported by Method §3.
- **Clarity:** feature-space rotation invariance is distinguished from physical camera rotation; supported by §3.1.
- **Experimental strength:** 98.5% on LIBERO is a tie for the best reported average in Table 1. The 75.0% LIBERO-Plus result is 4.7 percentage points above Spatial Forcing's 70.3%, from Table 2. No claim of winning every category is made.
- **Evaluation scope:** real-world comparisons cover three methods, six tasks, and 10 trials per task. Figure 8's displayed rounded averages are retained, including π₀'s original value of 41%; no new rounding convention is imposed on the figure.
- **Method validity:** RGB-only inference and a frozen 3D teacher during training are described separately. Rank preservation is reported as an empirical observation, not a universal guarantee.

The website preserves the manuscript's baseline names and aggregate values even where labels differ between individual suites and the overall block. It does not infer a publication venue, acceptance status, or arXiv identifier.

## Design credit

The layout follows [LaVA-Man](https://qm-ipalab.github.io/LaVA-Man/), the [Academic Project Page Template](https://github.com/eliahuhorwitz/Academic-project-page-template), and [Nerfies](https://nerfies.github.io/). Styles are implemented locally, without external font, JavaScript, or CSS dependencies.
