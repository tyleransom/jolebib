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