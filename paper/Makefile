# sane targets
DOCN = main
TARGET=main

all: rubber

normal: main.bib
	pdflatex $(DOCN).tex 
	pdflatex $(DOCN).tex 
	bibtex $(DOCN) || echo "ok"
	pdflatex $(DOCN).tex 
	pdflatex $(DOCN).tex 

rubber: main.bib
	GS_OPTIONS=-dPDFSETTINGS=/prepress rubber --pdf -Wrefs -Wmisc $(TARGET)

clean:
	rm -f *.aux *.dvi *.idx *.ind *.log *.toc *.bak *.blg *.bbl
	rm -f *.ps *.pdf
	rm -f *.aux *.log *.out *.bbl *.blg *~ *.bak $(TARGET).ps $(TARGET).pdf

# Tell versions [3.59,3.63) of GNU make to not export all variables.
# Otherwise a system limit (for SysV at least) may be exceeded.
.NOEXPORT:
