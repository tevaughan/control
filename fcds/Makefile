
FIG_FIGS = $(shell ls *.fig)
PDF_FIGS = $(FIG_FIGS:.fig=.pdf)
TEX_FIGS = $(FIG_FIGS:.fig=.tex)

%.pdf : %.fig
	fig2dev -L pdftex $< > $@

%.tex : %.fig
	fig2dev -L pdftex_t -p `echo $< | sed 's/fig/pdf/'` $< > $@

.PHONY : all clean

all : solutions.pdf

solutions.pdf : solutions.tex setup.tex ch01.tex $(PDF_FIGS) $(TEX_FIGS)
	pdflatex solutions
	pdflatex solutions

clean :
	@rm -fv *.aux
	@rm -fv *.log
	@rm -fv *.out
	@rm -fv $(PDF_FIGS)
	@rm -fv *.ps
	@rm -fv $(TEX_FIGS)
	@rm -fv *.toc

