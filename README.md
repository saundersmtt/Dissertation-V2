# Dissertation V2

This repository hosts the full LaTeX source for a dissertation manuscript.  The
primary entry point is `paper.tex`, which pulls in the individual chapter files
(`ch1.tex` … `ch5.tex`) and supporting assets stored under the `CH*/figures`
directories, the shared bibliography `refs.bib`, and the pre-generated PDFs in
the root for quick reference.

## Requirements

- A recent LaTeX distribution (TeX Live, MiKTeX, or MacTeX) that provides
  `pdflatex`, `bibtex`, and the commonly used packages already declared in
  `paper.tex`.
- `latexmk` (bundled with TeX Live/MacTeX; installable separately on other
  platforms).

Examples:

```bash
# Debian / Ubuntu
sudo apt-get install texlive-full latexmk

# macOS (Homebrew)
brew install --cask mactex
```

## How to Compile

The recommended way to build is via `latexmk`, which automatically runs the
required passes and stops only after all references, citations, and lists
resolve.

```bash
# one-off build
latexmk -pdf paper.tex

# continuous build and preview on changes
latexmk -pdf -pvc paper.tex

# remove auxiliary files
latexmk -c
```

If `latexmk` is unavailable you can fall back to manual compilation:

```bash
pdflatex paper.tex
bibtex paper
pdflatex paper.tex
pdflatex paper.tex
```

The final PDF will be written to `paper.pdf`.
