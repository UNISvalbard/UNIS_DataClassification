# Readme

This is a repository template that contains the raw files for markdown-based manuscripts.

## Install and use

- Clone this repository
- Populate the text/manuscript.md file and additional data beloning to your manuscript
- Push to *main* branch
- [Alternatively] Push to *publish* branch to automatically generate HTML and DOCX files...
- ... update your user.name and user.email in the *.github/workflows/main.yml* configuration file ...
- ... and do not forget to merge this with the *main* branch.

## Manuscript writing

To keep track of changes and prevent this repository turning into a dump-nightmare, some suggestions are found below:
- Always synchronise (i.e., git pull and push) before and after working on the manuscript
- One sentence is One line: always start a new line after the end of your sentences!
- Figures are to be placed in the dedicated **assets/figures** folder
- Markdown text files are to be placed in the **text** folder
- Biblatex files (.bib extension) are to be placed in the root folder
- Outputs are to be exported to the **export** folder

This repository is linked with the hackmd.io web-based markdown editor.
hackmd.io supports most common markdown features.

### YAML Header
Most of the magic happens as markdown is converted to different formats.
This is for example the case in the *live preview* on hackmd.io.
To add additional features, you can specify a whole bunch of parameters in the YAML header of each document.
Think of these headers as the different packages you can import in $\LaTeX$[^1].

[^1]: Markdown even supports $\LaTeX$'s math features and typesetting! :+1: 

### Extended markdown
Some features, such as citations and automatic numbering of figures are missing.
I therefore provide an overview of these commands below.

#### Reference system
```
@authoretal_bibitemlabel == authors et al. (date)
[@authoretal_bibitemlabel] == (authors et al., date)
[comment, @authoretal_bibitemlabel; @author2etal_bibitemlabel] == (comment, authors et al., date; authors2 et al., date)
@fig:figure-label == Fig. x
(@fig:figure-label) == (Fig. x)
@tbl:table-label == Table x
(@tbl:table-label) == (Table x)
```

### Table with caption and auto numbering
```
| Column 1 | Column 2 | Column 3 |
| -------- | -------- | -------- |
| Text     | Text     | Text     |
 : table caption. {#tbl:table-label}
```

### Figure with caption and auto numbering
```
![Figure caption](assets/figures/figure-file-name.png){#fig:figure-label}
```

