
.PHONY : all clean

all : solutions.pdf

solutions.pdf : solutions.tex ch01.tex
	pdflatex solutions
	pdflatex solutions

clean :
	rm -fv *.aux
	rm -fv *.log
	rm -fv *.pdf

