# README.md - workshop

Four draft bacterial assemblies are represented as chromosomes in the files
`chr*.fasta`, with their assembled contigs in `chr*_contigs.gff`. Functional
annotations are given in `chr*_iprscan.raw` (InterPro) and `chr*_RAST.gff` 
(RAST).

A script to convert `glimmer3` output to GFF: `glimmer_to_gff.py` is also 
provided. 

GenBank-derived files for the *Pectobacterium atrosepticum* reference sequence are provided in `NC_004547.???`.

Reciprocal best BLAST hit data for the four Prodigal prediction sets against the reference protein set is provided in `rbbh_ref_vs_chr?_prodigal.tab`

CLUSTAL Omega and T-COFFEE alignments of glucanase sequences are provided in `glucanase_*.aln`, and the source sequences are in `glucanase.fasta`.