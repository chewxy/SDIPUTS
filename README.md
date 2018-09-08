Harvard UTS Referencing .bst file (SDIPUTS)
==================================

# Introduction 
Style Dictionaries for Information Presentations in UTS (_UTS Harvard Referencing Style_ reference and in-text citations).

This style file aims to implement the _UTS Harvard Referencing Style_ in BibTeX

The official style guide for _UTS Harvard Referencing Style_ is available from the UTS Library:
http://www.lib.uts.edu.au/help/referencing/harvard-uts-referencing-guide

# Instructions
## Download
The latest version of the .bst file can be downloaded from this GitHub repo.

The .bst file should be placed in the same directory as your .tex file with the below preamble.

## Using in a LaTeX document
### Preamble 
In the preamble of your .tex document, include the following:

```
\usepackage[british]{datetime2} % For urldate formatting
\usepackage{natbib}
\bibliographystyle{uts} % Import Harvard UTS style
\setcitestyle{aysep={}} % Remove comma separation between author and year for in-text citations
```

### In-Text Citation
In-Text citations can be performed with parenthesis using '\citep{bibtexkey}' or without using '\citet{bibtexkey}'.

#### `\citep`
```
Custom software development is less profitable than developing shrinkwrap software \citep{spolsky_2005}.
```

Results in:
```
Custom software development is less profitable than developing shrinkwrap software (Spolsky 2005).
```

#### `\citet`
```
\citet{spolsky_2005} said that custom software development is less profitable than developing shrinkwrap software.
```

Results in:
```
Spolsky (2005) said that custom software development is less profitable than developing shrinkwrap software
```

### Referencing
In your .bib BibTeX file, all standard BiBTeX reference types should be supported -- but most effort has gone into the following reference types.

* journal articles (with `article`)
* online resources (with `misc`)

Below are examples of each reference type:

#### Journal articles
Google scholar can automatically export journal articles in BibTeX format which is very useful!

```
@article{dijkstra1959note,
  title={A note on two problems in connexion with graphs},
  author={Dijkstra, Edsger W},
  journal={Numerische mathematik},
  volume={1},
  number={1},
  pages={269--271},
  year={1959},
  publisher={Springer}
}
```

#### Online resources
The 'urldate' tag is used for the last viewed element of the reference.

```
@misc{spolsky_2005, 
  title={Set Your Priorities}, 
  url={https://www.joelonsoftware.com/2005/10/12/set-your-priorities/}, 
  urldate = {2018-08-23},
  journal={Joel on Software}, 
  author={Spolsky, Joel}, 
  year={2005}
}
```
