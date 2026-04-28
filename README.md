# Capstone Poster

Final Harvard SEAS capstone poster source and export for the tennis virtual advertising project.

## Files

- `poster.tex`: Main editable source.
- `poster.pdf`: Current compiled submission PDF.
- `SEAS Research Poster 48 x 60 Template.pdf`: Official template base.
- `figures/`: Image assets used in the poster.

## Build

Run from this directory:

```bash
pdflatex -interaction=nonstopmode "poster.tex"
```

Optional preview export:

```bash
sips -s format png "poster.pdf" --out "poster_preview.png"
```

## Update Workflow

1. Replace figure files in `figures/` (keep filenames stable to avoid editing LaTeX paths).
2. Edit text blocks in `poster.tex`.
3. Rebuild with `pdflatex`.
4. Open `poster.pdf` and verify:
   - Harvard logos and frame are intact.
   - Content stays inside the three column regions.
   - No clipped text or overlapping image blocks.

## Figure Inputs Currently Referenced

- `figures/original_frame_300.png`
- `figures/result_v36_full_300.png`
- `figures/original_frame_700.png`
- `figures/result_v36_full_700.png`
- `figures/evo_v7_foot.png`
- `figures/evo_v12_foot.png`
- `figures/evo_v33_foot.png`
- `figures/evo_v36_foot.png`

## Teammate/Agent Handoff Notes

- Keep `poster.tex` as the single source of truth.
- Do not edit generated files (`.aux`, `.log`, `.out`).
- Commit figure updates and text updates together so diffs stay meaningful.
- If a late experiment (v37+) becomes best, update the metrics rows and relevant frame assets, then rebuild.
