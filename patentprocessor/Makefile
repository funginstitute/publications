.SUFFIXES : .pdf .tex .zip

LATEX=pdflatex -synctex=1 -interaction=nonstopmode --shell-escape

FLAGS=-shell-escape

TEXFILES = $(wildcard *.tex ../*.tex)

PDF = patentprocessor.pdf

pdf: $(PDF)

%.pdf: %.tex $(TEXFILES)
	pdflatex $(flags) $*
	bibtex $*
	pdflatex $(FLAGS) $*
	pdflatex $(FLAGS) $*
	pdflatex $(Flags) appendix.tex
	pdfjoin patentprocessor.pdf appendix.pdf
	rm appendix.pdf
	mv appendix-joined.pdf patentprocessor.pdf

clean:
	rm -rf *~ *.log patentprocessor.pdf *.aux *.out *.toc *.bbl
