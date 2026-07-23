# Thesis_CF_ETI_Microbiota
_**“Impact of New Cystic Fibrosis Treatments on the Composition and Functionality of the Lung and Gut Microbiota”**_
- Chapter I: Composition and functionality of the gut and airway microbiota after one year of elexacaftor-tezacaftor-ivacaftor.
- Chapter II: Dietary intake, body composition, and fecal microbiome characterization in children and adolescents after one year of elexacaftor-tezacaftor-ivacaftor.
- Chapter III: Longitudinal genomic dynamics of Pseudomonas aeruginosa after one year of elexacaftor-tezacaftor-ivacaftor.

## SUMMARY
In recent years, the clinical landscape of cystic fibrosis (CF) has changed substantially thanks to early diagnosis, multidisciplinary management, and especially the emergence of highly effective CFTR modulators, such as the triple combination elexacaftor-tezacaftor-ivacaftor (ETI). Although several studies have described a clear clinical improvement, particularly in respiratory outcomes, in people with cystic fibrosis (pwCF) carrying at least one Phe508del variant, fewer studies have evaluated its impact on the lung and gut microbiome from a multi-omics perspective. In this thesis, we studied not only the composition and functionality of both compartments but also the evolution of chronic respiratory pathogens such as _Pseudomonas aeruginosa_ during treatment.

In **Chapter I**, we evaluated the clinical response and changes in the composition and functionality of the gut and lung microbiota after one year of treatment in a cohort including children, adolescents, and adults, and explored associations between microbiota composition and clinical parameters. Clinical outcomes improved, with few adverse effects and scarce exacerbations, together with a significant improvement in lung function and the reduction of concomitant therapies, including antibiotics. At the respiratory level, although colonization by pathogens persisted, longitudinal cultures showed a lower burden of _P. aeruginosa_, whereas the population of _Staphylococcus aureus_ increased after one year of treatment. At the gastrointestinal level, an improvement in pancreatic function was observed, with no elevation in transaminases and a downward trend in fecal calprotectin. Finally, body mass index increased in adults.
From the microbiota perspective, fecal and respiratory communities remained compositionally stable, with individual changes and no evidence of global restructuring. The resistome also remained stable. At the host level, functional analyses showed a reduction in intestinal inflammation, whereas proteins related to the extracellular matrix persisted in the lung. At the microbial level, changes were limited to specific proteins or pathways, including enzymes involved in butanoate metabolism in the gut and methane metabolism in the lung. In addition, short-chain fatty acid (SCFA) concentrations did not show significant global changes. Exploratory analyses indicated clearer associations between the microbiota, liver enzymes, and elastase, suggesting possible species-dependent associations within anaerobic genera.

In **Chapter II**, the pediatric population was analyzed specifically. After one year of treatment, a favorable clinical response was also observed, with better sweat test results and a spirometric pattern consistent with less obstruction. Liver enzymes did not increase, and inflammatory markers tended to improve, although measures of fat absorption remained globally stable. From a nutritional perspective, the body mass index (BMI) z-score increased without a clearly parallel increase in fat intake, whereas serum lipids and body composition suggested modest trends toward greater adiposity. The gut microbiome remained broadly stable in composition and functionality, and the resistome persisted without a clear reduction despite lower antibiotic exposure. Exploratory analyses suggested that nutritional changes were more closely related to dietary pattern than to fat absorption, the microbiota, serum lipids, or SCFAs.

In **Chapter III**, we studied the genomic evolution of longitudinal _P. aeruginosa_ isolates in participants with chronic colonization. Although colonization persisted, some cases shifted toward intermittent colonization. Genomic analyses showed two main dynamics: replacement of the baseline strain by another clone, or persistence of closely related isolates. No high-risk sequence types were detected, and the profiles of genes associated with antimicrobial resistance were generally stable within the same lineage, whereas differences between baseline and follow-up isolates were mainly explained by strain replacement. No strains carrying acquired carbapenemases were detected, and the OprD protein was largely preserved. Persistent lineages accumulated variants in genes related to alginate, siderophores, lipopolysaccharide, quorum sensing, and biofilm, with patterns that depended on each participant and lineage.

To the best of our knowledge, this work constitutes one of the first studies in Spain to longitudinally evaluate the impact of ETI on the gut and lung microbiota from a multi-omics perspective, while also integrating the microbiological and genomic evolution of _P. aeruginosa_ during treatment. Taken together, this thesis shows that this therapy is associated with clinically relevant improvements in pwCF carrying at least one Phe508del variant. Despite the absence of marked microbial compositional restructuring, functional analyses suggest a reduction in intestinal inflammation and changes in pathways related to butanoate metabolism, as well as oxidative metabolism in the lung. In the pediatric population, nutritional changes appear to be more closely related to dietary pattern than to marked changes in the microbiota or intestinal absorption. Finally, the persistence of _P. aeruginosa_ and the observed lineage patterns of persistence and its replacement support the need to maintain microbiological surveillance through strategies that optimize its detection and characterization.


## Repository overview
This repository contains the scripts and analysis workflows developed as part of a doctoral thesis **“Impact of New Cystic Fibrosis Treatments on the Composition and Functionality of the Lung and Gut Microbiota”**. Here, we evaluated the clinical and microbiological impact of one year of ETI treatment in pwCF. The analyses include longitudinal gut and lung microbiome profiling, metaproteomics, SCFA quantification, antimicrobial resistance gene (ARG) characterization, and analyses of clinical variables, including lung function, liver enzymes, fecal elastase, calprotectin, dietary intake, and body composition. Lastly, we characterized the longitudinal genomic dynamics of _Pseudomonas aeruginosa_ isolates.

## Cohort & sampling
This study included 35 <ins>clinically stable</ins> individuals with CF (adults, adolescents, and children). Four samples were collected from each participant: one fecal sample and one sputum sample before starting treatment with ETI (time point 0 months, T0), and one fecal sample and one sputum sample after 12 months of treatment with ETI (time point 12 months, T12).

**Total initial number of samples = 140**
- Feces = 70  
- Sputum = 70

One fecal sample and five sputum samples were excluded from the analysis due to the inability to generate shotgun sequencing libraries. Therefore, to maintain a paired analysis, both timepoint samples from one participant (P3) were removed from the fecal dataset, and both time-point samples of five patients (A12, A20, A26, P16, and P21) were removed from the sputum dataset. The paired design was also maintained in the metaproteomic, targeted metabolomic, and clinical analyses. For sputum ARG analyses, participant A4 was additionally excluded because no ARG reads were obtained for the T0 sample, resulting in a final dataset of 29 participants.

**Final number of samples**
- For metagenomic, metaproteomic, and SCFA quantification analyses in Chapter I:
  - Feces = 68 (34 at time 0 and 34 at time 12)
  - Sputum = 60 (30 at time 0 and 30 at time 12)
    - ARG in sputum: 58 (29 at time 0 and 29 at time 12)
- For metagenomic, metaproteomic, and SCFA quantification analyses in Chapter II:
  - Feces = 18 (9 at time 0 and 9 at time 12)
- For the longitudinal genomic analysis of _P. aeruginosa_:
  - Isolates from chronically colonized participants: 18


To understand how samples are coded, here are some examples:
- A1H0: Adult 1, feces at T0  
- A1H12: Adult 1, feces at T12  
- A1E0: Adult 1, sputum at T0  
- A1E12: Adult 1, sputum at T12  
- P2H0: Pediatric 2, feces at T0  
- P2H12: Pediatric 2, feces at T12  
- P2E0: Pediatric 2, sputum at T0  
- P2E12: Pediatric 2, sputum at T12
(H and E refer to the Spanish terms heces (feces) and esputo (sputum), respectively)

## Contents of the repository
In this repository you will find the data, metadata, and R scripts for the following analyses.
Microbiome, metaproteomic, metabolomic, and ARG analyses were performed **separately for fecal and sputum samples** to account for the distinct microbial and physiological environments of the gut and lungs.

1. **Statistical analysis of clinical, anthropometric, and dietary variables**: lung function parameters (percent predicted forced expiratory volume in one second, ppFEV<sub>1</sub>; percent predicted forced vital capacity, ppFVC; and FEV<sub>1</sub>/FVC ratio), sweat chloride concentration, liver transaminases (alanine aminotransferase, ALT; aspartate aminotransferase, AST; and gamma-glutamyl transferase, GGT), fecal elastase and calprotectin concentrations, pulmonary exacerbations, concomitant treatments, body mass index (BMI), body composition, and data obtained from 3-day dietary records.
2. **Longitudinal culture-based analysis of the main respiratory pathogens**: _Pseudomonas aeruginosa_ and _Staphylococcus aureus_.   
3. **Microbiome compositional analysis**  
   - Taxonomic profiling of gut and lung microbial communities using shotgun metagenomics.
   - Alpha- and beta-diversity analyses.
   - Differential abundance analysis.
   - Characterization of the antimicrobial resistance gene repertoire.  
4. **Functional analysis**
   - Metaproteomic analysis<sup>*</sup>
     - Functional characterization of microbial proteins.
     - Protein–protein interaction and functional enrichment analyses of human proteins using STRING (version 12.0) (https://string-db.org/).  
   - Targeted metabolomic analysis (SCFA quantification): acetate, propionate, and butyrate.  
5. **Associations between clinical outcomes and microbiome composition**
   - Associations between microbial community composition and clinical parameters.
   - Associations of changes in clinical variables, dietary intake, and body composition with changes in microbial taxa.
6. **Longitudinal genomic analysis of _Pseudomonas aeruginosa_**
   - Molecular typing using MLST and cgMLST.
   - Phylogenetic and pairwise genomic variant analyses.
   - Assessment of lineage persistence and replacement.
   - Characterization of variants in genes associated with chronic infection, virulence, biofilm formation, and antimicrobial resistance.
   - Analysis of antimicrobial resistance genes and β-lactamase variants.

\* Due to GitHub file size limitations, the raw metaproteomic tables (proteins, peptides, and functions) could not be uploaded. This repository includes filtered versions of these files for reproducibility purposes. If you require access to the original raw files, please contact me at **natalia.baston.paz@gmail.com**.

## Limitations
Please consider the **limitations** described in the **Discussion** section of the thesis, particularly those related to sample size and sputum sample quality.

## Recommended citation
Bastón-Paz N. Impact of New Cystic Fibrosis Treatments on the Composition and Functionality of the Lung and Gut Microbiota. Doctoral thesis, Universidad Complutense de Madrid, 2026.

## Contact
For any issues or questions, please contact: **natalia.baston.paz@gmail.com**.

### Affiliation
This thesis was developed at the Department of Microbiology of Ramón y Cajal University Hospital, affiliated with the Ramón y Cajal Health Research Institute, as part of the Doctoral Programme in Microbiology and Parasitology at the Complutense University of Madrid.
