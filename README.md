<img border="0" src="http://bioconductor.org/shields/availability/release/CODEX.svg"/>
<img border="0" src="http://bioconductor.org/shields/downloads/CODEX.svg"/>
<img border="0" src="http://bioconductor.org/shields/build/release/bioc/CODEX.svg"/>
<img border="0" src="http://bioconductor.org/shields/years-in-bioc/CODEX.svg"/>


# CODEX
A Normalization and Copy Number Variation Detection Method for Whole Exome Sequencing

## Install the current release from Bioconductor
```r
## try http:// if https:// URLs are not supported
source("https://bioconductor.org/biocLite.R")
biocLite("CODEX")
```

## Install the devel version from GitHub
```r
install.packages("devtools")
library(devtools)
install_github("yuchaojiang/CODEX/package")
```


## Author
Yuchao Jiang, Nancy R. Zhang

## Maintainer
Yuchao Jiang <yuchaoj@wharton.upenn.edu>

## Description
A normalization and copy number variation calling procedure for
whole exome DNA sequencing data. CODEX relies on the availability of 
multiple samples processed using the same sequencing pipeline for 
normalization, and does not require matched controls. The normalization 
model in CODEX includes terms that specifically remove biases due to GC 
content, exon length and targeting and amplification efficiency, and latent
systemic artifacts. CODEX also includes a Poisson likelihood-based recursive
segmentation procedure that explicitly models the count-based exome 
sequencing data.

## Citation
Jiang, Y., Oldridge, D.A., Diskin, S.J. and Zhang, N.R., 2015. CODEX: a normalization and copy number variation detection method for whole exome sequencing. Nucleic acids research, 43(6), pp.e39-e39.

## Google user group
https://groups.google.com/d/forum/codex_wes_cnv

## Bioconductor
* [Bioconductor page](http://www.bioconductor.org/packages/release/bioc/html/CODEX.html)
* [Vignettes](http://www.bioconductor.org/packages/devel/bioc/vignettes/CODEX/inst/doc/CODEX_vignettes.pdf)
* [Demo code](http://www.bioconductor.org/packages/devel/bioc/vignettes/CODEX/inst/doc/CODEX_vignettes.R)

# CODEX for cancer genomics
When apply CODEX to whole-exome sequencing and targeted sequencing of cancer patients (with or without normal controls):
* use normalize2() function if there are normal samples and specify the index of the normal samples as the normal_index argument;
* use the *fractional* mode for segmentation for somatic CNA detection due to the heterogenous structure of cancer samples and the interger mode for germline CNV detection

## CODEX for targeted sequencing
We've adapted CODEX for targeted sequencing. Refer to codes attached (need to source segment_targeted.R for gene based segmentation).
* [codex_targeted.R](https://dl.dropboxusercontent.com/u/34105617/codex_targeted.R)
* [segment_targeted.R](https://dl.dropboxusercontent.com/u/34105617/segment_targeted.R)

## Load CODEX segmentation results into IGV for visualization
* [CODEX_IGV.R](https://dl.dropboxusercontent.com/u/34105617/CODEX_IGV.R)
