# astro-kit-test

A plain static Astro site that contains every section of the BetterCMS Kit library: 142 sections in 14 categories, hand-built with hard-coded sample content. It exists to be imported into BetterCMS and made editable, as a test of the import and make-editable flow.

## Run it

```bash
bun install
bun run dev      # http://localhost:4321
bun run build    # static output in dist/
```

## Structure

- `src/pages/index.astro`: overview of all categories
- `src/pages/<category>/index.astro`: one page per category, rendering its sections in Kit order
- `src/pages/<category>/<entry-id>.astro`: standalone pages for entry-type sections (blog post, product detail, docs page, job posting, event, location…)
- `src/components/<category>/<Section>.astro`: one component per Kit section; each starts with `<!-- kit: <id> -->` and wraps its content in an element with `id="<id>"`
- `src/styles/global.css`: shared tokens and utility classes
- `kit-source/`: the Kit entries (schema + sample value) each section was built from

No CMS wiring and no npm packages beyond Astro: content lives in the markup, as on a normal hand-written site.
