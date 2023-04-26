# Epitranscriptome Course Bari 28-April-2023
# EPITRAN workshop -RNA Editing 24/06/21
<p align="justify"> Epitranscriptome refers to all biochemical RNA modifications affecting cellular RNAs. 
Nowadays, RNAseq is the de facto standard approach to discover RNA editing candidates in whole
eukaryotic. <br> Although the identiﬁcation of editing sites is, in principle, quite simple, it
represents a computational challenge because true RNA editing events have to be discriminated from
genome-encoded single-nucleotide polymorphisms (SNPs) and technical artefacts caused by
sequencing or read-mapping errors.<br>
The use of genomic reads from whole genome sequencing (WGS) or whole exome sequencing (WXS) experiments in single individuals, 
annotations in the database of SNPs (dbSNP) and several stringent ﬁlters can minimize the detection of false RNA editing candidates. <br>
The entire procedure is human speciﬁc but can be applied to other organisms
with available transcriptomic and genomic reads. <br> 
The detection of RNA editing is carried out by our
REDItools package, which is able to handle RNAseq data alone or combine RNAseq and genomic
reads from WGS or WXS experiments to reduce the false discovery rate due to SNPs.<br>
The main procedure begins with the download of RNAseq and WGS data in the standard fastq
format and the subsequent preprocessing to improve their global quality and ensure
that input raw data are not biased. To this aim, collected reads are inspected using
FASTQC (https://github.com/s-andrews/FastQC) to perform some quality control checks and cleaned
using FASTP 23 to remove read regions of low quality or potential adaptor sequences or poly(A)-tails
(or long terminal homopolymeric stretches).
  
<img src=""></img>
</p>

