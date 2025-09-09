# Dissertation-V2

This repository contains the LaTeX source for the dissertation.

## Requirements

- A LaTeX distribution such as TeX Live or MikTeX
- The `latexmk` build tool (usually included in the distribution)

On Debian/Ubuntu systems you can install the requirements with:

```bash
sudo apt-get install texlive-full latexmk
```

## Compiling

The main document is `paper.tex`. To build the PDF once, run:

```bash
latexmk -pdf paper.tex
```

`latexmk` will run the necessary tools (e.g., `pdflatex`, `bibtex`) and produce `paper.pdf`.

To automatically recompile when sources change and preview the output:

```bash
latexmk -pdf -pvc paper.tex
```

To clean the auxiliary files generated during the build, use:

```bash
latexmk -c
```
