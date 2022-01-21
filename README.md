# Vic_R_codes_III

This code was designed by Victor Jimenez Vasquez - vr.jimenez.vs@gmail.com.
## Intro
There are currently 10 SARS-CoV-2 variants assigned by World Health Organisation (WHO) defined by more than 200 pango-lineages. Metadata downloaded from GISAID contains "lineage" information but not "variant". The knowledge on the regional progression of SARS-CoV-2 variants requires a manual assignation that could be tedious, time-consuming and prone to errors. "Infer variant" allows the user to add a variant column given a metadata downloaded from GISAID and or a dataframe containing a "lineage" column. 

## Usage 
```r
#load metadata downloaded from GISAID#
meta <- read.csv("metadata.tsv", header=TRUE, sep="\t")
meta2 <- infer_variant(meta)

#save the newmetadata#
write.csv(meta2, file="variants.csv", row.names=FALSE)

## Utility 
Use "infer variant" to obtain a "variant column" added to your dataframe. 
