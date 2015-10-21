# Makefile 
#
# Compiles presentations and handouts for the Introduction to Bioinformatics
# training course
#
# To generate all presentation files, issue `make presentation`.
#
# To generate all handouts, issue `make handouts`.
#
# To generate both presentation files and handouts, issue `make all`.
#
# (c) 2014-2015 James Hutton Institute
# Author: Leighton Pritchard

all: presentation handouts clean_intermediates

presentation: part0_slides part1_slides part1ne_slides part2_slides \
	part3_slides clean_intermediates

slides: presentation

handouts: part0_handouts part1_handouts part1ne_handouts part2_handouts \
	part3_handouts exercises clean_intermediates

exercises: exercises.pdf

part0: part0_slides part0_handouts
part0_slides: part0_soyouwanttobe_slides.pdf
part0_handouts: part0_soyouwanttobe_handouts.pdf

part0: part0_slides part0_handouts
part1_slides: part1_goldenrules_slides.pdf
part1_handouts: part1_goldenrules_handouts.pdf

part1: part1_slides part1_handouts
part1ne_slides: part1_goldenrules_noexercises_slides.pdf
part1ne_handouts: part1_goldenrules_noexercises_handouts.pdf

part2: part2_slides part2_handouts
part2_slides: part2_blast_slides.pdf
part2_handouts: part2_blast_handouts.pdf

part3: part3_slides part3_handouts
part3_slides: part3_workshop_slides.pdf
part3_handouts: part3_workshop_handouts.pdf

clean_intermediates:
	rm *.aux *.log *.nav *.out *.snm *.synctex.gz *.toc *.vrb || true
	rm sections/*.aux || true

clean_pdf:
	rm *.pdf || true

clean: clean_intermediates clean_pdf

# TODO - automatically detect dependencies by looking for \input lines
# Currently changing any sub-file forces regeneration of all top level files.
%.pdf : %.tex sections/*.tex
	pdflatex $<
	pdflatex $<
