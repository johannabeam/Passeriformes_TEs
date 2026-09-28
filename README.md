# Passeriformes TEs Project

"Note the repeatmasker is 1-based and the other two are 0-based as far as positioning for counting the bp in the intervals."

## [species].filtered.srf file format
This is for the satellite repeat finder (srf) bed files 
From [Heng Li's github]([url](https://github.com/lh3/srf/issues/6)):
Only the first five columns are of importance. The column header, from left to right: chr, start, end, SRF-contig-name, mean-percent-identity. 

## [species].filtered.ultra files
"The files labeled [species].filtered.srf.bed and [species].filtered.ultra are additional satellites and tandem repeats found in those programs that are not found in the repeatmasker output, so those can be included for total repetitive content in addition to those annotated in the repeatmasker files."


# UCE Phylogeny of the species

Make the genomes.conf file for phyluce:
```
awk '{print $1 ":/path/to/TEs/lastz_genomes/" $1 "/" $1 ".2bit"}' ~/genomes.txt > genomes.conf
```
