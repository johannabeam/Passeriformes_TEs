# Passeriformes TEs Project

"Note the repeatmasker is 1-based and the other two are 0-based as far as positioning for counting the bp in the intervals."

## [species].filtered.srf file format
This is for the satellite repeat finder (srf) bed files 
From [Heng Li's github]([url](https://github.com/lh3/srf/issues/6)):
Only the first five columns are of importance. The column header, from left to right: chr, start, end, SRF-contig-name, mean-percent-identity. 

## [species].filtered.ultra files
"The files labeled [species].filtered.srf.bed and [species].filtered.ultra are additional satellites and tandem repeats found in those programs that are not found in the repeatmasker output, so those can be included for total repetitive content in addition to those annotated in the repeatmasker files."

## [species].out file
For some reason, there are a few instances where repeats are not categorized as they should be. E.g., (CA)n usually is in the repeat_match column, but also show up in the class.family column. These should probably be filtered out?

https://www.girinst.org/repbase/update/browse.php?letter=E&rank=&autonomous=1&nonautonomous=1&simple=1&format=EMBL#browse

CAM2_GG - gallus gallus
CENSTRIG - centromere repeat (tandem) - strigidae
AVIXHoI - W chromosome repeat region - strigidae


# UCE Phylogeny of the species

Make the genomes.conf file for phyluce:
```
awk '{print $1 ":/path/to/TEs/lastz_genomes/" $1 "/" $1 ".2bit"}' ~/genomes.txt > genomes.conf
```
