# thesisucsc
Dissertation Template For UC Santa Cruz

Following [**UCSC Dissertation Thesis Guidelines (Rev July, 2021)**](https://graddiv.ucsc.edu/current-students/pdfs/dissertation-thesis-guidelines.pdf)

Inspired by [`UCSCTHESIS`](https://github.com/adamnovak/ucscthesis) class, but I use [`scrbook`](https://www.ctan.org/pkg/scrbook) class instead (so almost none of that class is used here).

### How to use?
1. Put your notation macros in `preambles/math`
2. Put your enviroment definitions (such as `\newtheorem`) in `preambles/envs`
3. Put your metadata (such as `title`, `author`, `field`, `committeemember`, etc.) in `metadata`
4. Put images in `images/`
6. Put actual contents in `contents/`. Note that 
    - `abstract` is in `contents/0.1.abstract`
    - `dedication` is in `contents/0.2.dedication`
    - `acknowledgements` is in `contents/0.3.acknowledgements`
    - `appendix` is in `contents/appendix`
    - `bibliography` is in `contents/bib` [^1]
    - `index` is in `contents/index` [^2]
8. Complie `main.tex`
9. If you need to use packages or midify the settings, see `sample.pdf` or below for which .tex file to edit.

[^1]:I use `amsrefs` and put `bib` data directly in `contents/bib`. If you don't like that, you can instead put `\bibliography{your bib file}` instead of a raw `bib` data. Note that no `\bibliographystyle` is needed.
[^2]:In case you want to customize index

### Modify settings
- Fonts are in file `preamble/font`
  - Text mainly use **PS Type 1 font** based on **Times**. This is done by `newtxtext`
  - Math fonts: use package `newtxmath`. Uncomment to use `mathalpha` and `bm`
- Layout is in file `preamble/layout`
  - For page: use package `geometry`
  - For header and footer: use package `scrlayer-scrpage`
  - For line spacing: use package `setspace`
  - For footnote: use package `footmisc`
- Modify section headings: `preamble/section`

### Some remark
The template minimized the number of packages to avoid conflicts. Some possible conflicts:
- packages modified fonts. Such as `amssymb` (because `newtxmath` already loaded `TXAMSadd` family, if you want to use `amssymb` instead, give `noamssymbols` option to `newtxmath` in ) 
