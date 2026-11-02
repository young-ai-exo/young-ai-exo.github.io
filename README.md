# young-ai-exo.github.io

Personal site listing open-source projects in bioinformatics and agent tooling.

**Live:** https://young-ai-exo.github.io/

## Design

Single static page, no build step, no dependencies.

- Left-right split hero: copy on the left, project cards on the right
- Light base `#fbfbfc` with one forest-green accent `#0F7A52`
- Dark mode via `prefers-color-scheme`; accent lightens to `#3FBF88` so it
  clears WCAG AA on a dark base (7.89:1 measured)
- Motion limited to card hover, button `:active`, and a one-shot entrance
  stagger, all disabled under `prefers-reduced-motion`
- Corner radii restricted to 6px (tags) / 9px (buttons) / 14px (cards)

Design spec and implementation plan live in the
[personal-skills](https://github.com/young-ai-exo/personal-skills) repo under
`docs/specs/` and `docs/plans/`.

## Adding a project

Duplicate the `.project-card` block inside `.hero-right`. The hero holds at
most two cards; beyond three projects, add an `ALL PROJECTS` grid section
between the hero and About (see the plan document for the markup).

Card meta shows language and last-updated month only. Skill counts are
deliberately omitted so nothing goes stale.

## Local preview

```bash
open index.html
```

## License

Content © 2026 Yusheng Yang. Site markup and styles are public domain.
