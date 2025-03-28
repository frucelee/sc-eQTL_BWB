# sc-eQTL_BWB
Code for the study: Single-cell transcriptomics reveals quantitative trait loci regulating cell type-specific gene expression in peripheral blood mononuclear cells response to lipopolysaccharide in BWB.

All the statistical analyses were performed by in-house R/Python script or published tools/packages.

## 1.1 Single-cell RNA-seq analysis and cell type identification ##

Ambient RNA and potential doublets were detected by DecontX and Scrublet, respectively, with default settings. Single-cell analysis was performed by Seurat; cell type was identified by the classical marker.

## 1.2 Covariates preparing for sc-eQTL mapping ##

Ten principal component analyses (PCA) of samples were then carried out by Plink based on the LD-pruned genotypes; Ten probabilistic Estimation of Expression Residuals (PEER) in each of the cell types were estimated using the PEER software package.

## 1.3 sc-eQTL mapping ##

A linear regression model implemented by TensorQTL was used. A linear mixed model with a sparse genetic relationship matrix (GRM) implemented by fastGWA was employed for the validation analysis.

## 1.4 Identification of content-specific eQTL ##

Pseudotime across monocytes was determined by Slingshot, and then the mixed linear model was used to perform dynamic eQTL analysis. The weighted linear model was applied to perform co-expression eQTL mapping.

## 1.5 Estimation of shared signals ##

MASH was applied to estimate the shared eQTL signals between each pair of eQTL summary statistics.

## 1.6 Colocalization and Summary-based Mendelian randomization (SMR) analysis ##

COLOC was used to identify the shared genetic variants between sc-eQTL and 69 clinical traits. This mediation effect of gene expression on the clinical traits was estimated using SMR & HEIDI methods.

## 1.7 Replication of the identified sc-eQTL ##

To validate the identified eQTL, we checked their effect size in the public GTEx dataset.

## 1.8 sc-vQTL mapping ##

The intra-individual dispersion value for each gene in individuals was estimated using the Cox-Reid adjusted MLE approach, and subsequently, TensorQTL was applied to perform QTL mapping.
