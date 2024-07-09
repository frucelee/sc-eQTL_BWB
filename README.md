# sceQTL_LPS_BWB
Code for the study: Single-cell eQTL analysis identifies cell type-specific regulation of gene expression in peripheral blood mononuclear cells response to lipopolysaccharide in BWB.

All the statistical analyses were performed by in-house R/Python script or published tools/packages.

## 1.1 Single-cell RNA-seq analysis and cell type identification ##

Single-cell analysis by Seurat; cell type was identified by the classical marker.

## 1.2 Identification of single-cell expression quantitative traits loci (sceQTL) and single-cell co-expression QTL ##

The eQTL of each cell type or condition was estimated using a linear model which is implemented in tensorqtl. The single-cell co-expression QTL was identified using a weighted linear model.

## 1.3 Estimation of shared signals ##

MASH was applied to estimate the shared eQTL signals between each pair of eQTL summary statistics.

## 1.4 Colocalization analysis ##

COLOC was used to identify the colocalized genes between sceQTL and clinical diseases. 

## 1.5 Single-cell Co-expression Analysis ##

To determine the co-expression profiles we used CS-CORE, which is powered by WGCNA.

## 1.6 Replication of the identified sc-eQTL ##

To validate the identified eQTL, we checked their effect size in the public GTEx dataset.

## 1.7 Overlapping with epigenome ##

The publicly available dataset scATAC-seq from the steady state and stimulated by LPS was employed.
