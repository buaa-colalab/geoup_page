# GeoUP pipeline source

This directory is self-contained and does not depend on the repository's
`paper/` directory.

Build the vector figure from `pipeline.tex`:

```powershell
pdflatex -interaction=nonstopmode -halt-on-error -jobname=pipeline-figure pipeline-standalone.tex
pdftocairo -png -singlefile -r 300 pipeline-figure.pdf ../pipeline
```

`assets/camera2.png` is a transparent raster rendering of the retained
`assets/camera2.svg`, used so the build does not require Inkscape.
