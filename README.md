# Capstone Poster

Final Harvard SEAS capstone poster source and export for the tennis virtual advertising project.

## Quick Start (New Collaborator)

```bash
git clone git@github.com:enriquedlh97/capstone-poster.git
cd capstone-poster
pdflatex -interaction=nonstopmode "poster.tex"
```

Expected output:
- A new `poster.pdf` in the repo root.
- No missing-file errors for `SEAS Research Poster 48 x 60 Template.pdf` or `figures/*`.

## Environment Setup

This project only requires a LaTeX distribution with `pdflatex`.

### macOS

1. Install MacTeX:
   - [https://www.tug.org/mactex/](https://www.tug.org/mactex/)
2. Verify:

```bash
pdflatex --version
```

### Ubuntu/Debian

```bash
sudo apt update
sudo apt install -y texlive-latex-base texlive-latex-recommended texlive-fonts-recommended texlive-pictures
pdflatex --version
```

### Optional (Preview Export on macOS)

```bash
sips -s format png "poster.pdf" --out "poster_preview.png"
```

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

For clean rebuild:

```bash
rm -f poster.aux poster.log poster.out
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

## Troubleshooting

- `LaTeX Error: File '...sty' not found`
  - Your TeX distribution is incomplete. Install MacTeX (macOS) or the Ubuntu packages listed above.
- `! LaTeX Error: File 'SEAS Research Poster 48 x 60 Template.pdf' not found`
  - Ensure you are running from the repo root and the template PDF is present.
- Images missing in output PDF
  - Confirm all referenced files exist in `figures/` with the exact same names.
