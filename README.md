# latexmerge

This bash script takes a latex document an creates a new folder that contains a single tex file that includes all included latex files (with \include and \input commands) and all bib items used in the document. In addition the script copies all graphic files used in the document (with the \includegraphics command) and adapts the file paths in the new tex file accordingly.

The script uses standard unix tools, such as `cp` and `sed`, and tools from TeX Live, such as `pdflatex`, `latexmk`, `bibtex`, and `latexpand`.

## Usage

Run the script inside the directory where the main tex file is located. Provide the name of the main tex file (without the .tex file extension) as the first argument. As a second optional argument you can provide wether the tex document uses biber or bibtex as a tool for building the bibliography.

```
./latexmerge main bibtex
```
