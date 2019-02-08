# HSCLSC
## HSCLSC R-package found text mining co-occurence gene-fontion (Hematopoietic stem cell/Leukemic stem cell) with NCBI website

### Synopsis
Hematopoietic stem cell (HSC) and leukemic stem cell (LSK) is an intensive field in research in order to well understand pathological process of leukemia and also mechanism of its relapse under therapies (Holyoake TL 2017). Many computational methods for human gene prioritization in order to associate gene to disease (Moreau Y 2012). Esearch API is important resource to target literature in NCBI website by text mining (NCBI Resource Coordinators 2017). HSCLSC R-package allows to target NCBI esearch API with custom keyword association: (hematopoietic stem cell) OR (leukemic stem cell) to find gene co-occurrence citations in Pubmed database. In second time, an “HSC” score was determined for each gene to quantified their implication in HSC/LSC field, Hypergeometric test of Fisher is also compute and respective p-value are corrected with False Discovery Rate for high dimension data.

![HSC](https://github.com/cdesterke/HSCLSC/blob/master/HSC.png)

## Usage
* query NCBI with input gene list

hsc<-hscquery(c("CXCR4","IDH1","FLT3","TET2","GAPDH","TBP","CD33","CD38"))

* compute hsc score

hscfinal<-hscscore(hsc)

* compute Fisher test with FDR corrected p-values

hscfisher<-hsctest(hsc)

## References

-Holyoake TL, Vetrie D. The chronic myeloid leukemia stem cell: stemming the tide of persistence. Blood. 2017 Mar 23;129(12):1595-1606

-Moreau Y, Tranchevent LC. Computational tools for prioritizing candidate genes: boosting disease gene discovery. Nat Rev Genet. 2012 Jul 3;13(8):523-36

-NCBI Resource Coordinators. Database Resources of the National Center for Biotechnology Information. Nucleic Acids Res. 2017 Jan 4;45(D1):D12-D17.


