.SUFFIXES : .pdf .tex .zip

LATEX=pdflatex

FLAGS=-shell-escape

TEXFILES = $(wildcard *.tex ../*.tex)

PDF = manifesto.pdf

pdf: $(PDF)

%.pdf: %.tex $(TEXFILES)
	pdflatex $(FLAGS) $*
	pdflatex $(FLAGS) $*
	bibtex $*
	pdflatex $(FLAGS) $*
	pdflatex $(FLAGS) $*

clean:
	rm -rf *~ *.log manifesto.pdf *.aux *.out *.toc *.bbl
