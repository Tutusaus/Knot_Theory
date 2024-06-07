
NAME=report
all: $(NAME).pdf

SECTIONS := $(shell echo ./*.tex)

MYTEX = pdflatex

MYTEXARGS = -interaction=nonstopmode -synctex=1

$(NAME).pdf: $(NAME).tex literature.bib $(SECTIONS) bachelorproject.sty
	$(MYTEX) $(MYTEXARGS) $(NAME)
	bibtex $(NAME).aux
	$(MYTEX) $(MYTEXARGS) $(NAME)
	$(MYTEX) $(MYTEXARGS) $(NAME)
	$(MYTEX) $(MYTEXARGS) $(NAME)

clean:
	rm -f *.aux *.log *.out *.snm *.toc *.vrb *.nav *.synctex.gz *.blg *.bbl *.fdb_latexmk *.fls *.ind *.idx *.ilg *.bcf *.run.xml
