# Epitranscriptome Course Bari 28-April-2023
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
<img src="img1.png"></img>
<ul>
<li>The main procedure begins with the download of RNAseq and WGS data in the standard fastq
format and the subsequent preprocessing to improve their global quality and ensure
that input raw data are not biased.</li> 
<li>To this aim, collected reads are inspected using
FASTQC (https://github.com/s-andrews/FastQC) to perform some quality control checks and cleaned
using FASTP to remove read regions of low quality or potential adaptor sequences or poly(A)-tails
(or long terminal homopolymeric stretches).</li>
<li>Next, cleaned reads are aligned onto the reference genom. While RNAseq reads
are mapped using STAR, an ultrafast splice-aware software, WGS reads are aligned using BWA,
which does not take into account the spliced nature of reads.</li>
<li>Finally, aligned
transcriptome and genome reads are converted in the standard BAM format using SAMtools. <br>
Unlike BWA, STAR parameters can be tuned to directly output reads in BAM format,
saving time and avoiding SAMtools calls.</li>
<img src="img2.png"></img>
After the preprocessing, RNAseq and WGS reads are passed to the REDItoolDnaRna.py script
using non-stringent parameters to identify all potential DNA–RNA variants (Fig. 2). The use of
loosing parameters, deﬁned as basic ﬁlters in Fig. 2, is an expedient to save computing time in all
cases in which a user needs to run multiple instances of REDItools with different option values.</li>

  
</p>


