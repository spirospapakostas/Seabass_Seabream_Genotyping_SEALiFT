SNP Genotyping from Nanopore FASTQ Reads

Overview

This script processes Nanopore FASTQ sequencing reads to identify single nucleotide polymorphisms (SNPs) at predefined genomic markers. It searches for SNP sites using flanking sequences with minor mismatches allowed and counts occurrences of each allele.

Features
	•	Automated SNP detection: Identifies SNPs based on predefined flanking sequences.
	•	Supports Nanopore sequencing data: Processes FASTQ files directly.
	•	Handles sequencing errors: Allows minor mismatches in sequence matching.
	•	Reports allele counts: Provides per-marker allele frequency statistics.

Dependencies

Before running the script, install the required dependencies:

pip install biopython regex  

Usage
	1.	Run the script:

 python3 snp_genotyping.py  

 2.	Enter the path to the FASTQ file when prompted.
	3.	The script will process the reads and output allele counts per marker.

Example Output

Processed 10000 reads from file example.fastq  

In file example.fastq there are 250 A and 400 G for seabream vgll3.  
In file example.fastq there are 300 C and 500 T for seabream six6.  

Marker Information

The script analyzes SNPs from multiple genomic regions, including genes such as:
	•	vgll3, six6, pigm, and bcl6a in seabream (Sparus aurata).
	•	vgll3, six6, and bcl6a in seabass (Dicentrarchus labrax).

Each marker includes:
	•	A left flanking sequence (upstream of the SNP).
	•	A right flanking sequence (downstream of the SNP).
	•	Expected allele variations (e.g., A/G, C/T).
