LaTeX Paper Template
====================

A very simple and minimalistic LaTeX template.

Building and Viewing
--------------------

1. Place yourself in the paper's root directory
2. Just call `make` to build using `pdflatex`
3. You can view with `mupdf` by `make view`
4. Clean up directory: `make distclean`

Distributing a Polyglot PDF
---------------------------

A feature of this template is that is supports *polyglot attachments*, as in the wonderful `PoC||GTFO` journal. This enables you to e.g. attach the source code of your publication together with your PDF! Here is how to do it: create a folder called `attachments`, and put whatever you want to bundle in there. Then call the `make polyglot` command, this assumes you are running in a Unix-like environment and have access to `zip` and `unzip`. In the `polyglot` folder, you'll find a modified `paper.pdf` with your `attachments` "secrectly" in there! To get them out of there, just call: `unzip paper.pdf`! If you want to overwrite the original `paper.pdf` in the root folder, just call `make distribute`, and it will also do that for you.

System Requirements
-------------------

Only tested on `pdflatex`-based distributions.

Structure
---------

* `attachments`: files to be attached to the pdf
* `build`: contains stuff generated by `pdflatex`
* `figures`: should contain all figures for the paper
* `license.md`: don't worry, it's MIT licensed.
* `listings`: should contain all annexed code for paper
* `Makefile`: automatically build the paper on request
* `paper.bib`: bibliography used in the paper
* `paper.pdf`: the generated paper!
* `paper.tex`: imports all packages and styling stuff
* `polyglot`: build files for the polyglot attachment
* `readme.md`: this file!
* `sections`: each of these files represents a section
    * `*.tex`: each one of these should be a section
