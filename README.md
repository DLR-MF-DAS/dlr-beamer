# DLR Beamer theme

Editable adaptation of the supplied DLR-PPT-Master_1.31_EN.potx.

## Start

Keep beamerthemeDLR.sty and assets/ beside your .tex file. Compile with XeLaTeX:

    xelatex main.tex
    xelatex main.tex

For the ten-slide demonstration:

    xelatex DLR-preview.tex
    xelatex DLR-preview.tex

Overleaf: upload the ZIP, select main.tex (or DLR-preview.tex) as the main document,
and set the compiler to XeLaTeX. A standard TeX Live installation with Beamer,
TikZ and fontspec is sufficient. LuaLaTeX is also supported by the theme;
the delivered preview was tested with XeLaTeX.

## Theme and commands

Use `\documentclass[aspectratio=169,11pt]{beamer}` and `\usetheme[blue]{DLR}`.
The layout requires 160 x 90 mm, Beamer's standard 16:9 canvas.

- `\usetheme[green]{DLR}` or `[yellow]`: select a different initial variant.
- `\DLRsetcolor{blue}`: select blue, green or yellow between frames.
- `\DLRtitleframe`: cover using the usual title, subtitle, author, institute and date.
- `\DLRsectionframe{Chapter title}`: image-backed chapter divider.
- `\DLRsectionframe[path/to/image.jpg]{Chapter title}`: custom chapter image.
- `\DLRfullimage[Image credit]{path/to/image.jpg}`: full-page image and logo.
- `\DLRsetfooter{Custom footer}`: override the automatic short author/institute/date.
- `\renewcommand{\DLRassetpath}{path/to/assets}`: change the asset directory.

For content use ordinary frames, itemize, columns, tabular and equations. Prefer
`\begin{frame}[t]{Title}` for the source template's top-aligned content.
Chapter dividers are explicit: `\section` alone does not insert a frame.
Numbering counts frames (including covers), not overlay pages.
Use pre-cropped 16:9 images for chapter/fullscreen backgrounds; these fill the
canvas and will stretch images of another aspect ratio. Normal includegraphics
figures preserve their aspect ratio.

## Fidelity and scope

Retains the source's 16:9 proportions, original raster logos and map backgrounds,
sidebar widths, logo placement, grey headings, small footer, square bullets,
and blue/green/yellow variants. Colour changes belong between chapters, as
specified by the source master. The theme does not assign colours to research areas.

Arial is selected when installed. Otherwise XeLaTeX uses TeX Gyre Heros, then
Nimbus Sans. This preview uses Nimbus Sans. Fonts are not bundled. PDFLaTeX
has a Helvetica fallback, but use XeLaTeX for Unicode names and the supplied demo.

This is a Beamer adaptation, not an official DLR-issued LaTeX theme or a literal
conversion of all 37 PowerPoint layouts. Content layouts use Beamer's native
columns/tables; table cell styling and the example block are Beamer adaptations.
Title-page author details are added below the source's subtitle band. Chapter
examples use the supplied maps in place of PowerPoint's empty image placeholders.
Navigation, transitions and PowerPoint editing instructions are not reproduced.
All slide text, equations and layout primitives are editable; the original logos
and map backgrounds remain raster assets. No image assets were redrawn.

## Asset attribution

The assets were extracted without modification from the user-supplied DLR master.
The source imprint states: all images DLR (CC BY-NC-ND 3.0), unless otherwise
stated. Retain relevant credits and follow DLR's logo/brand requirements.
