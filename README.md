# Gyrase_Topo-seq
Exploring gyrase cleavage sites accross E. coli W3110 genome

DNA-gyrase is a type II topoisomerase that introduces negative superhelicity into topologically closed DNA molecules. It operates with two DNA segments - so called G and T. During catalysis the enzyme introduces temporal double-stranded break into the G-segment, transferres the T-segment through it and religates the gap. The 5'-ends of the DNA break are stabilized by the formation of the intermediate covalent complex between DNA and gyrase.
Topo-Seq is a ChIP-Seq-like approach that exploits the formation the complexes to map the gyrase cleavage sites with a single-base precision.

This repositorium contains a set of bash, python and R scripts that were used for Topo-Seq data analysis and visualization.

######################

## GCSs_filtering_and_overlapping.py

The script takes raw GCSs data, returns only trusted GCSs, computes GCSs shared between different conditions, draws Venn diagrams of the sets overlappings, writes GCSs sets.

######################

## Raw_reads_processing.sh

Shell script that makes QC of the reads before and after the trimming procedure. Than script maps trimmed and paired reads to the reference genome, prepares sorted and indexed BAM-files suitable for visualization with IGV
Requirements: factqc, trimmomatic, bwa mem, samtools 
