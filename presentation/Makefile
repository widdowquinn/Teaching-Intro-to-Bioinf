all : part0 part1 part1ne part2 part3 exercises.pdf

part0 : part0_soyouwanttobe.pdf

part1 : part1_goldenrules.pdf

part1ne : part1_goldenrules_noexercises.pdf

part2 : part2_blast.pdf

part3 : part3_workshop.pdf

# TODO - automatically detect dependencies by looking for \input lines
# Currently changing any sub-file forces regeneration of all top level files.
%.pdf : %.tex sections/*.tex
	pdflatex $<
	pdflatex $<
