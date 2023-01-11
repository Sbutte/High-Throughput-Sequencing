# High-Throughput-Sequencing
Intro RNAseq Anlysis,  CHIPseq, PCA, Clustering

## 1. Introduction to RNASeq
High Throughput sequencing tells us which genes are active and how much they are transcribed. Mutated cells behaves differently than Normal cells. To understand what genetic mechanisms are causing difference we look at Gene Expression data. So we use RNAseq to measure gene expression in Normal cells and use it to measure gene expression in Mutated cells. After comparison of both we can figure out the difference between both.

Cells --> Chromosomes --> Genes (Collection of active & Non-active genes) --> RNAs (messenger RNAs)

 ### Steps invovled in RNA-Seq:
  1) Prepare a sequencing library
        a. Isolate teh RNA
        b. Break the RNA into small fragments ( *as RNA fragments are 1000s BP long. Sequencing machine can sequence only short fragments.*)
        c. Convert the RNA fragment into Double stranded DNA. 
          (*This is done mainly because Double stranded DNAs are more stable compared to RNA and can easily be modified.*)
        d. Add Sequencing adaptors. 
         (*This allows sequencing machine to recongnize different fragments and allows us to sequence different samples at a time.*)
         e. PCR amplification
         (*Fragments with PCR adaptors are amplified.*)
         f. Quality Control
         (*Check Library Concentration and Library Fragment Length*)  
         
  2) Sequence
        a) DNA Fragments are laid out on Flow cell. One grid can have around 400,000,000 Fragments laid out vertically.
        b) The machine has color coded fluorescent probes to identify the nucleotides.Probes are attacehd to first base in each sequence.
        c) Raw data file 
       1st line : @ --- : indicates the unique sequence code.
       2nd line : contains the bases acalled for sequence fragment
       3rd line : + :  Always a plus Character
       4th line : QC score for each fragment
     
  3) Data Analysis
        a) plot the data Genes Vs Count using PCA
        b) Identify differential Expressed genes between Normal or Mutatated cells. Usally done using edgeR or DESeq2.


## Referenes -
1. StatQuest with Josh Starmer - https://www.youtube.com/watchv=tlf6wYJrwKY&list=PLblh5JKOoLUJo2Q6xK4tZElbIvAACEykp
2. RNA Sequencing Part I: Introduction to Illumina’s RNA library preparation workflows -
https://www.youtube.com/watch?v=M7K801nQZcg
3. 
