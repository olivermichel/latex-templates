
TARGET = name
STYLE  = sig-alternate

DEPS   = $(STYLE).cls $(wildcard sec/*.tex) $(wildcard fig/*) $(TARGET).bib
LATEX  = pdflatex -file-line-error -interaction nonstopmode
BIBTEX = bibtex -terse

$(TARGET).pdf: $(TARGET).tex $(DEPS)
	$(LATEX)  $(TARGET)
	$(BIBTEX) $(TARGET)
	$(LATEX)  $(TARGET)
	$(LATEX)  $(TARGET)

clean:
	$(RM) *.aux *.log *.blg *.bbl *.out

spotless: clean
	$(RM) $(TARGET).pdf

.PHONY: clean spotless
