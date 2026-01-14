# Ausführliches Makefile für LaTeX-Projekt
# Kompiliert PDF, Bibliographie, Glossar und reinigt Hilfsdateien

PDF=main.pdf
TEX=main.tex
BIB=main.bib
AUX=main.aux
LOG=main.log
BLG=main.blg
BCF=main.bcf
GLS=main.gls
IST=main.ist

all: $(PDF)

$(PDF): $(TEX) $(BIB)
	pdflatex $(TEX)
	biber main
	makeglossaries main
	pdflatex $(TEX)
	pdflatex $(TEX)

biber:
	biber main

makeglossaries:
	makeglossaries main

clean:
	rm -f *.aux *.log *.bbl *.blg *.bcf *.run.xml *.toc *.lof *.lot *.lol *.out *.gls *.glo *.ist *.acn *.acr *.alg *.glg *.gls *.glg *.glsdefs *.synctex.gz

mrproper: clean
	rm -f $(PDF)

.PHONY: all clean mrproper biber makeglossaries
