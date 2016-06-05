all: thesis.pdf

# LaTeX must be run multiple times to get references right
thesis.pdf: thesis.tex $(wildcard *.tex) bibliography.bib
	pdflatex -draftmode $<
	bibtex thesis
	makeglossaries thesis
	pdflatex -draftmode $<
	pdflatex $<

poster.pdf: poster.tex $(wildcard *.tex)
	pdflatex $<

clean:
	rm -f *.log *.dvi *.aux *.toc *.lof *.lot *.out *.bbl *.blg *.acn *.glo *.glsdefs *.ist *.acr *.alg *.glg *.gls
	rm -f thesis.pdf
