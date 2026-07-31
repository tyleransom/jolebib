# jolebib
This repository contains a custom BibTeX style file for the Journal of Labor Economics (`jole.bst`).

## Steps to compile
To create your own BibTeX style file, follow these steps:
1. Download this repository
2. Use your system terminal to compile the file `makebst.tex`. This will launch an interactive session that will present the user with about 25-30 questions regarding citation styles.
3. `makebst.tex` will output a .dbj file. You can then run latex on that file, which will create the .bst file
4. Once you create the .bst file, you need to edit it in the following ways:
	* insert `"t" change.case$` on line 707
	* insert `"t" change.case$` on line 864

## Additional resources
The two PDF files included here contain more background information on how custom BibTeX files can be compiled and edited. Credit goes to the author of the `makebst` package on CTAN.
## DOI links

Both `jole.bst` and `jpe.bst` support an optional `doi` field. When present, the
entry ends with a small hyperlinked `DOI` pointing at `https://doi.org/<doi>`:

```bibtex
@article{chetty2014,
  author  = {Chetty, Raj and Hendren, Nathaniel and Kline, Patrick and Saez, Emmanuel},
  title   = {Where is the Land of Opportunity?},
  journal = {Quarterly Journal of Economics},
  year    = {2014}, volume = {129}, number = {4}, pages = {1553--1623},
  doi     = {10.1093/qje/qju022}
}
```

Load `hyperref` for a clickable link (`beamer` loads it automatically). Without
`hyperref` the entry degrades to `DOI: https://doi.org/...`. Entries with no
`doi` field are unchanged.

To customize, redefine either command *after* `\begin{document}`:

```latex
\renewcommand{\doiprefix}{}                                   % text before the link
\renewcommand{\bibdoi}[1]{\href{https://doi.org/#1}{doi:#1}}  % show the full DOI
```

Note: a literal `#` in a DOI must be written `\#` in the `.bib` file.
