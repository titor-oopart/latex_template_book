latex_template_book

Template for writing a book in LaTeX.

Requirements:

Install these tools:

- texlive
- texstudio (optional)
- biber
- latexmk

Commands (Linux):

sudo apt update
sudo apt install texlive-full texstudio biber latexmk

Compile from TeXstudio (GUI):

In TeXstudio, set the build sequence:

pdflatex → biber → pdflatex → pdflatex

Compile from terminal (recommended):

Note:
Don't use spaces in the NAME value. Instead of "my book" use my_book

Linux (Bash):

```bash
cd /path/to/your/project
latexmk -pdf -jobname=my_book book.tex
```

```bash
latexmk -pdf -pvc -jobname=my_book book.tex
```

Linux (Fish):

```bash
cd /path/to/your/project
latexmk -pdf -jobname=my_book book.tex
```

```bash
latexmk -pdf -pvc -jobname=my_book book.tex
```

Windows (PowerShell):

```bash
cd C:\path\to\your\project
latexmk -pdf -jobname=my_book book.tex
```

```bash
latexmk -pdf -pvc -jobname=my_book book.tex
```

Clean temporary files:

Linux / Windows:

```bash
cd /path/to/your/project
latexmk -c
```

Notes:

- Replace "book.tex" with your main file name if different.
- The PDF output will be named "my_book.pdf" (or the value of NAME).
- If you want a different PDF name, change the NAME value.
- If you want to ignore generated files in git, add them to .gitignore (for example: _.pdf, _.aux, _.log, _.bbl, \*.bcf).
