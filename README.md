# vic_R_codes_III
![infer_image](https://user-images.githubusercontent.com/89874227/150560900-e25f8623-1259-4444-93ef-1f1f7a398283.jpg)

This code was designed by Victor Jimenez Vasquez - vr.jimenez.vs@gmail.com.
## Intro
There are currently 7 SARS-CoV-2 variants (VOI/VOC) assigned by World Health Organisation (WHO) defined by more than 250 pango-lineages. Metadata downloaded from GISAID contains "lineage" information but not "variant". The knowledge on the regional progression of SARS-CoV-2 variants requires a manual assignation that could be tedious, time-consuming and prone to errors. "Infer variant" allows the user to add a variant column given a metadata downloaded from GISAID and or a dataframe containing a "lineage" column. 

## Usage 
```r
#paste "infer_variant.R" file in your working directory#
source("infer_variant.R")

#load metadata downloaded from GISAID#
meta <- read.csv("metadata.tsv", header=TRUE, sep="\t")

#run infer_variant#
meta2 <- infer_variant(data = data, label = "label")

#save the new metadata#
write.csv(meta2, file="variants.csv", row.names=FALSE)

#"infer_variant" arguments #
- data : a data.frame cointaing a column called "pangolin_lineage". 
- label : a dessired name to inclued in the output csv file .  

```
## Output
a data frame including a new clomun specifying SARS-CoV-2 variant per row store in a "csv" file called "gisaid_label_.csv"

## Utility
Use "infer variant" to obtain a "variant column" added to your dataframe.

This code was designed by Victor Jimenez Vasquez - vr.jimenez.vs@gmail.com.

Vic

