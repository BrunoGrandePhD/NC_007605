# Improved EBV Gene Annotations

This repository exists to track minor improvements made to the EBV gene 
annotations (GenBank: [NC_007605](https://www.ncbi.nlm.nih.gov/nuccore/NC_007605.1)).
Both the original (`NC_007605.original.gff3`) and the improved (`NC_007605.improved.gff3`) 
versions are included. A summary of the improvements are listed below and are described 
in detail in the commit messages. 

## Improvements

1. In the original annotations, EBNA3A was described as an transcript isoform 
   of the LMP2 gene alongside LMP2A and LMP2B. This was problematic when 
   annotating variants using SnpEff, whereby the EBNA3A transcript was the only
   transcript that was considered because it was the longest (944 aa compared
   to 497 and 378 aa for LMP2A and LMP2B, respectively). We created a new gene
   entry in the GFF3 file for EBNA3A and marked it as the parent for the EBNA3A
   transcript. See [`ad4b15cd`](https://github.com/brunogrande/NC_007605/commit/ad4b15cd560deb194f3f5b4089d0c9887719f5c6) 
   for more details.
