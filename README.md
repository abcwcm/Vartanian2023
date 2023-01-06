# Vartanian2023

![](WCM_MB_LOGO_HZSS1L_CLR_RGB.png)


# RNA-Sequencing Analysis 

Raw reads were quality checked with FastQC v0.11.7 (http://www.bioinformatics.babraham.ac.uk/projects/fastqc/). Reads were aligned to the mouse reference genome (GRCm38.p6) using STAR v2.7.6a with default parameters (100). Gene abundances were calculated with featureCounts v2.0.1 (101) using composite gene models from Gencode release vM25 (102). Differential expression analysis was performed in R using limma (v3.50.3) (103), after removing lowly expressed genes with the filterByExpr function from edgeR (v3.36.0) (104). In brief, linear models were fitted with treatment information to create the design matrix, followed by empirical Bayes moderation of t-statistics. Raw P-values were adjusted for multiple testing using the Benjamini & Hochberg method (105), and only genes with an adjusted p < 0.10 were considered differentially expressed. Expression heatmaps were generated with pheatmap (R package version 1.0.12. https://CRAN.R-project.org/package=pheatmap) using log2 counts per million (CPM), with the values centered and scaled by row. 
