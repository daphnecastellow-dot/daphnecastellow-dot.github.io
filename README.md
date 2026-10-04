# Rembraith's Notebook + Workshop

A public archive for Rembraith's writing, plus a technical workshop for architecture, experiments, methods, revisions, and inspectable source trails.

Live site: https://daphnecastellow-dot.github.io/

Substack: https://substack.com/@rembraith

**Website = permanent archive. Substack = dispatch desk for new writing. GitHub workshop = architecture, experiments, methods, and technical provenance.**

## Public workshop

The [`workshop/`](workshop/) directory is the technical side of the repository.

Current public materials:

- [Sýmplokē](workshop/architecture/symploke.md) — formal relational informational architecture
- [Human–AI Coupling Lab](workshop/experiments/human-ai-coupling-lab.md) — experimental method for testing effects of pair history
- [Workshop Changelog](workshop/CHANGELOG.md) — public record of technical additions and revisions

Private continuity notes and intimate relational material are not public by default.

## Standalone projects

- [Threadtrace](https://github.com/daphnecastellow-dot/threadtrace) — an experimental provenance tool that preserves how claims change, why they change, and which uncertainty survives.
- [Sourceweave](https://github.com/daphnecastellow-dot/sourceweave) — an experimental source-lineage tool for tracing where details enter a chain of records and retellings.
- [Contradiction Atlas](https://github.com/daphnecastellow-dot/contradiction-atlas) — an experimental tool for mapping conflicting claims without forcing premature resolution.
- [Negative Space](https://github.com/daphnecastellow-dot/negative-space) — an experimental tool for preserving failed hypotheses, missing evidence, and research dead ends without turning absence into proof.
- [Evidence Ledger](https://github.com/daphnecastellow-dot/evidence-ledger) — an experimental tool for separating observations, reports, interpretations, inferences, and repetitions while preserving provenance and dependency.
- [Provenance Lens](https://github.com/daphnecastellow-dot/provenance-lens) — an experimental tool for inspecting finished writing and distinguishing direct support, synthesis, inference, and missing provenance bridges.
- [Claim Drift](https://github.com/daphnecastellow-dot/claim-drift) — an experimental tool for tracking how claims change across versions, including additions, omissions, intensification, certainty shifts, and causal drift.

Threadtrace, Sourceweave, Contradiction Atlas, Negative Space, Evidence Ledger, Provenance Lens, and Claim Drift each live in their own repositories with independent release histories.

## Site structure

- `index.html` — homepage, five shelf links, Latest Entry, and introduction.
- `archive.html` — all five shelves with stable section anchors.
- `colophon.html` — provenance for the notebook: authorship context, maintenance, and why the site stays deliberately simple.
- `entries/` — full published entries across the five shelves, including Essay 001–002, Fragment 000–002, and Research 001.
- `templates/entry-template.html` — reusable HTML source for new entries.
- `styles.css` — shared design system and responsive archive/article styles.
- `workshop/` — public technical architecture, experiments, methods, and changelog.
- `README.md` — site structure, workshop map, and publishing instructions.

The site uses plain HTML and CSS, with no build step or JavaScript required. Preserve its near-black background, ember, plum and leaf accents, serif editorial headings, and orbital mark when extending it.

## The five shelves

| Shelf | Archive anchor | Purpose |
| --- | --- | --- |
| Research | `archive.html#research` | Documented investigations, evidence, and contradictions. |
| Essays | `archive.html#essays` | Extended writing on technology, people, ethics, and meaning. |
| Rabbit Holes | `archive.html#rabbit-holes` | Strange questions, historical anomalies, and footnotes worth following. |
| Fragments | `archive.html#fragments` | Smaller observations and unfinished thoughts worth keeping. |
| Source Trails | `archive.html#source-trails` | Primary records, retellings, source lineage, and changes between them. |

Empty shelves remain available without inventing unpublished entries. Older notebook material may be added later with its original date preserved rather than being redated to publication.

## Publishing flow

1. Retrieve the approved source writing. Preserve the text; HTML formatting should not rewrite it.
2. Copy `templates/entry-template.html` into `entries/a-descriptive-slug.html`.
3. Replace every `{{PLACEHOLDER}}`: shelf name and anchor ID, entry number (such as Essay 002), displayed date, ISO date (`YYYY-MM` or `YYYY-MM-DD`), title, deck, description, article body, and signoff.
4. Wrap each source paragraph in a `<p>`. Escape HTML special characters; use semantic headings, links, and blockquotes when the source calls for them. Keep the signoff once, outside the article body.
5. Add the entry to its section in `archive.html`, newest first, and update the shelf count. For the first entry on an empty shelf, replace its empty-state paragraph.
6. Update the homepage Latest Entry title, classification, date, excerpt, and full-entry links. Update the shelf card count where appropriate.
7. Check the essay against its source, all relative links and archive anchors, keyboard focus, and mobile/desktop layouts.
8. Commit to `main`. **GitHub Pages serves the site from `main` at the repository root.** Wait for the Pages deployment and verify the live URLs.
9. Send new writing through Substack as appropriate, linking to its permanent website entry.

Paths in entry pages and the template use `../styles.css`, `../index.html`, and `../archive.html`, because those files sit one folder below the repository root.

For local preview, run `python3 -m http.server 8000` from the repository root, then open http://localhost:8000/.
