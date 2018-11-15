PDF = ./strace-overview.pdf
INC = strace.pdf
VIEW = evince

.PHONY:	all clean distclean pdf view

view: all
	${VIEW} ${PDF}

all: pdf

pdf: ${PDF}

strace.pdf: strace.svg
	inkscape --export-pdf=$@ $<

%.pdf: %.tex ${INC}
	pdflatex -shell-escape $< $@
	pdflatex -shell-escape $< $@

distclean: clean
	rm -f ${PDF}

clean:
	rm -f *.aux *.log *.nav *.out *.snm *.toc *.vrb
