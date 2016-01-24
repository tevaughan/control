
FIG_FIGS = $(shell ls *.fig)
PDF_FIGS = $(FIG_FIGS:.fig=.pdf)

%.pdf : %.fig
	fig2dev -L pdf $< > $@

.PHONY : all clean

all : solutions.pdf

solutions.pdf : solutions.tex setup.tex ch01.tex $(PDF_FIGS)
	pdflatex solutions
	pdflatex solutions

clean :
	@rm -fv *.aux
	@rm -fv *.log
	@rm -fv *.out
	@rm -fv *.pdf
	@rm -fv *.ps
	@rm -fv *.toc

