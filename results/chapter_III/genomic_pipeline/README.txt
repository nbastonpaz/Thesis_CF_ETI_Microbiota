# Results

This directory contains the main output files generated during the whole-genome sequencing analysis of longitudinal *Pseudomonas aeruginosa* isolates from people with cystic fibrosis.

Only relevant final or summary outputs are included. Large intermediate files, software databases, raw sequencing reads, BAM files, and temporary analysis files are not stored in this directory.

## Directory structure

```text
results/
├── abricate/
├── amr_finder/
├── card-rgi/
├── cgMLST/
├── coverage/
├── mash_tree/
├── oprD/
├── OSA/
├── PubMLST/
├── quast/
├── snippy/
├── starAMR/
└── wecA/
```

### `abricate/`

Results obtained with **ABRicate** using antimicrobial resistance and virulence databases, including ResFinder, NCBI, CARD, ARG-ANNOT, and VFDB.

### `amr_finder/`

Antimicrobial resistance results obtained with **NCBI AMRFinderPlus** for the analyzed *P. aeruginosa* isolates.

### `card-rgi/`

Results obtained with **CARD-RGI**, together with targeted validation of selected antimicrobial resistance-associated genes when required.

This directory also contains additional BLAST-based analyses used to confirm the presence and integrity of specific genes identified during CARD-RGI screening.

### `cgMLST/`

Results from the **core-genome multilocus sequence typing (cgMLST)** analysis performed with **chewBBACA** using the assembled genomes.

All isolates are included in the same cgMLST analysis to provide a global overview of their allelic relatedness. The resulting allelic profiles can subsequently be visualized using a **minimum spanning tree (MST)** with software such as **PHYLOViZ** or **GrapeTree**.

Unlike the core-genome SNP analysis generated with Snippy, cgMLST is performed directly from the assembled genomes and does not depend on the reference genome used for Snippy variant calling.

### `coverage/`

Sequencing coverage summary for the 18 analyzed *P. aeruginosa* isolates.

The `coverage.csv` file contains the following metrics for each isolate:

* **`mean_depth`**: mean sequencing depth across the assembled genome.
* **`breadth_of_coverage_≥1X`**: percentage of positions in the assembly covered by at least one read.

Across all isolates, the mean sequencing depth was approximately **686×**, ranging from **225× to 1179×**. The breadth of coverage ranged from **99.9% to 100%**, with an overall mean of **99.9%**.

### `mash_tree/`

Results from the **Mash** genomic similarity analysis.

Mash uses MinHash-based genome sketches to estimate pairwise genomic distances among the sequenced *P. aeruginosa* isolates. The resulting distance data and tree files provide a global overview of genomic similarity among the isolates and can be visualized using **iTOL**.

### `oprD/`

Results from the targeted analysis of ***oprD***.

BLASTN and TBLASTN comparisons against reference OprD variants were used to identify the closest reference variant and assess whether OprD was complete, altered, fragmented, or potentially truncated in each isolate.

### `OSA/`

Results from **O-antigen serogroup identification** using BLAST against the OSA database.

### `PubMLST/`

Molecular typing results obtained using the **PubMLST** MLST scheme for *P. aeruginosa*.

### `quast/`

Assembly quality statistics generated with **QUAST**.

These results include metrics used to assess the quality of the assembled *P. aeruginosa* genomes, including genome size, number of contigs, N50, N90, L50, L90, AuN, and GC content.

### `snippy/`

Variant-calling results generated with **Snippy/Snippy-multi**.

Two different comparison strategies were used:

1. **Common-reference analysis:** all isolates were analyzed using the same PAO1 reference, providing a common reference coordinate system across the complete collection. This approach allows a common core-genome alignment to be generated and used for a global core-genome SNP tree.

2. **Within-participant pairwise analysis:** longitudinal isolates were compared only within each participant, using different isolates from the same participant as reference genomes. Comparisons include T0 versus subsequent time points and, when available, additional comparisons such as T6 vs T9, T6 vs T12, and T9 vs T12. Different morphotypes collected at the same time point were also used as references when appropriate.

The core alignments generated from the within-participant analyses are independent and **cannot be combined into a single global core-genome SNP tree**, because different reference genomes were used for each participant.

### `starAMR/`

Results obtained with **starAMR**, including antimicrobial resistance and molecular typing information for the analyzed *P. aeruginosa* isolates.

### `wecA/`

Targeted analyses performed to validate variants affecting ***wecA***.

These analyses include local nucleotide alignments and TBLASTN searches used to determine whether the gene is intact, disrupted, fragmented, or potentially pseudogenized in specific longitudinal isolates.

## Genomic relatedness analyses

Several complementary approaches were used to investigate genomic relatedness among the *P. aeruginosa* isolates.

### Mash similarity tree

Mash provides a rapid genome-wide estimate of pairwise genomic distances based on MinHash sketches and was used to obtain an initial overview of genomic similarity among all isolates.

### Core-genome SNP tree

A global core-genome SNP tree can be generated from the Snippy analysis in which **all isolates were analyzed using the same PAO1 reference genome**.

The within-participant Snippy analyses use different reference isolates for each participant and therefore generate independent core alignments that cannot be combined into a single global tree.

### cgMLST and MST

cgMLST is performed directly from the assembled genomes and is independent of the reference genome used for the Snippy analyses.

All isolates can therefore be included in the same cgMLST analysis to assess their overall allelic relatedness. The resulting cgMLST profiles can subsequently be visualized using a **minimum spanning tree (MST)**.

## Notes

The complete analysis workflow, commands, software environments, file preparation steps, and interpretation guidelines are described in the pipeline documentation available in this repository.

Raw sequencing data and large intermediate files are not included in the `results/` directory.