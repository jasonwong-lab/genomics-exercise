# Genomics data analysis exercise

Provided are three files, (1) WGS_mutations.bed, is a list of somatic mutations from a cancer sample, (2) Replication_timing.bed, is a file containing the replication timing for all regions in the human genome. (3) GENCODE_known_canonical_TSS.bed, is a file containing the transcription start site of all coding genes. 

Replication timing refers to whether a region in the genome is replicated early or late when a cell undergoes replication. Each line in the file is a region in the genome, and the 4th column is the replication time, where the higher the value, the earlier the region is replicated (i.e. early replicating regions have the highest values, and late replicating regions have the lowest values). The WGS_mutations.bed file contains the mutation coordinates on each line and the reference and mutant base in the 5th and 6th columns. The GENCODE_known_canonical_TSS.bed contains the TSS coordinates for each gene on each row with the strand on the 6th column. All files are in BED format and are in hg38 coordinates.

Using these files, please answer the following questions and provide a brief explanation/screen capture of how you reached the answer:

1. How many mutations are in the cancer genome?
2. What is the median size (in base pairs) of regions in the replication timing file?
3. List the top 5 earliest replicating region in the genome.
4. How many mutations are there in the 10,000 latest replicating regions?
5. Is the mutation rate generally higher in early or late replicating regions?
6. What type of DNA repair defect is this cancer likely to have based on the difference in mutation rate of the early and late replicating regions? (You will probably need to do literature search)
7. What cancer type do you think this sample is from?
8. Using GENCODE_known_canonical_TSS.bed, write a script to generate a file containing all genes with bidirectional promoters (i.e. non-overlapping promoters that are at most 1kb apart on opposing strands - see schematic below).

![alt text](https://github.com/jasonwong-lab/genomics-exercise/blob/master/bidirectional.jpg?raw=true)

_Hints: The BED format is used to store information about regions in genomes. Column 1 is the chromosome, column 2 is the start position and column 3 is the end position of a region. Additional columns provide information about each region. For questions 4 and 5, you will need to use BedTools. The [BedTools tutorial](http://quinlanlab.org/tutorials/bedtools/bedtools.html) provides all information necessary to use bedtools to get the answer for 4 and 5._
