PANDOC=pandoc

PANDOC_OPTIONS_MAIN=--standalone
PANDOC_OPTIONS_CHAPTER=--top-level-division=chapter --listings

SRC=$(wildcard */*.md)

TEMPLATE=lecture-notes.template
MAIN_FILE=lecture-notes

%.tex : %.md
	$(PANDOC) $(PANDOC_OPTIONS_CHAPTER) -o $@ $<

TEXFILES=$(SRC:%.md=%.tex)

texfiles=$(TEXFILES)

@echo =$(TEXFILES)

# Default target builds PDF
all: pdf

# tex target builds all tex files in subdirectories and the main tex file
tex: $(TEXFILES)
	$(PANDOC) $(PANDOC_OPTIONS_MAIN) config.yml --template=$(TEMPLATE) --pdf-engine=lualatex --pdf-engine-opt=--shell-escape -o $(MAIN_FILE).tex

# odf target builds all tex files in subdirectories and the main pdf
pdf: $(TEXFILES)
	$(PANDOC) $(PANDOC_OPTIONS_MAIN) config.yml --template=$(TEMPLATE) --pdf-engine=lualatex --pdf-engine-opt=--shell-escape -o $(MAIN_FILE).pdf

clean:
	rm $(TEXFILES) $(MAIN_FILE).pdf $(MAIN_FILE).tex