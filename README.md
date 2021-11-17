## OCTOPUS: Origin Computation and Tracing by Objective Phylogeny and Usable Screensaver 

## First, to get an idea on what is Phylogeny, please download from the "data" folder, a testing dataset for 20 SARS-COV-2 genomes from [GISAID](www.gisaid.org). 
## Then run the following R script:
```
library(Biostrings); library(ape)
fa <- 'D:/data/gisaid/20genome.fa'
gen0 <- readDNAStringSet(fa, format='fasta')
gen <- subseq(gen0, start=21563, end=25384) # to extract spike protein region
gen <- chartr("-","N", replaceAmbiguities(gen0)) # *****
dist_dna <- ape::dist.dna(ape::as.DNAbin(gen)); 
plot(hclust(dist_dna))
tree_nj <- ape::nj(dist_dna)
plot.phylo(as.phylo(tree_nj), type="radial")
```

## A Phylogeny tree could also be drawn by using Python, as shown in below:
> 1. [A basic Python tutorial](https://medium.com/geekculture/phylogenetic-trees-implement-in-python-3f9df96c0c32)
> 2. [Physcraper: a Python package for continually updated phylogenetic trees using the Open Tree of Life](https://physcraper.readthedocs.io/en/latest/index.html)
> 3. Also, check out [Usher](https://www.nature.com/articles/s41588-021-00862-7) from UCSC.

<br/>

## #1. Introduction

### This tool is designed to perform like an octopus, who can "guess" the winner of football game. Of course, for serious scientific question such as the Origins of COVID-19, "guessing" is not allowed. Instead, it will be based on "objective phylogeny", based on analzying virus genome data from GISAID, in real time. Not everybody can afford to have a real "octopus" in a fish tank, but it is not difficult for anyone to simply download an "OCTOPUS" screensaver. Phylogeny analysis is widely used for COVID-19 research, but only a "usable screensaver" can bring that science to a much broad of audience so that more people could learn and even engage the science of "Origins calculation and tracing".
 
![Figure](./images/octopus.gif)

<br/>

### A default phylogeny tree is drawn and displayed. It does not change much, just like the London Eye. More and more virus genome data come everyday, real time. Some of these virus data might be "smoking guns" or even "bombers". When that happens, the "London Eye" will competely change and raise an alarm.  

![Figure](./images/londoneye.gif)

<br/>

### The final product will be a "Usable Screensaver". Since the pandemic has affected everybody, we want to get the public engaged, for them to better understand how orgin tracing is done scientifically. 

![Figure](./images/screensaver.gif)
