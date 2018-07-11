# Baseline Human Antibody Repertoire Project

This repository contains code and data used for analysis of the baseline human antibody repertoire. Briefly, we performed
ultra-deep sequencing of the antibody repertoires of 10 healthy, adult subjects (approxmately 3 billion total antibody sequences). This sequencing revealed a massively diverse antibody repertoire with surprisingly high overlap between the repertoires of different subjects.

## Code
The code used in this project is assembled into a series of Juypter notecooks. There are two sets of notebooks, those containing code used for [DATA PROCESSING](https://github.com/briney/grp_paper/tree/master/data_processing) and those containing code used to [MAKE FIGURES](https://github.com/briney/grp_paper/tree/master/make_figures). GitHub will render each of the notebooks, but the code cannot be executed from within GitHub. If you'd like to actually run the code contained in the notebooks, you must clone the repository.

**_NOTE:_** *Whenever possible, the intermediate datasets required to run the code are included in this repository, however, many intermediate datasets are too large to be included. In such cases, links to the required datasets are provided in the appropriate notebook.*

## Datasets  
We have generated several large datasets, in two primary groups: antibody sequences from healthy adult subjects, and synthetic antibody sequences using statistical models of V(D)J recombination. 

### Antibody sequencing data
Raw and processed datasets from each subject can be downloaded using the following links. Some of these datasets are quite large (the compressed raw FASTQs are roughly 100GB per subject, and the uncompressed JSON datasets range from ~100GB to nearly 1TB).

  - 316188
    - Sequences: [**raw FASTQs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/316188_HNCHNBCXY_raw-fastqs.tar.gz), [**consensus FASTAs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/316188_HNCHNBCXY_consensus_UID18-cdr3nt-90_071817.tar.gz)
    - FASTQC: [**pre-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/316188_HNCHNBCXY_pre-trimmed-fastqc.tar.gz), [**post-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/316188_HNCHNBCXY_post-trimmed-fastqc.tar.gz)
    - Annotated data: [**consensus CSVs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/316188_HNCHNBCXY_consensus_UID18-cdr3nt-90_minimal_071817.tar.gz), [**consensus JSONs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/316188_HNCHNBCXY_consensus_UID18-cdr3nt-90_json_071817.tar.gz)
  - 326650
    - Sequences: [**raw FASTQs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326650_HCGCYBCXY_raw-fastqs.tar.gz), [**consensus FASTAs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326650_HCGCYBCXY_consensus_UID18-cdr3nt-90_071817.tar.gz)
    - FASTQC: [**pre-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326650_HCGCYBCXY_pre-trimmed-fastqc.tar.gz), [**post-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326650_HCGCYBCXY_post-trimmed-fastqc.tar.gz)
    - Annotated data: [**consensus CSVs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326650_HCGCYBCXY_consensus_UID18-cdr3nt-90_minimal_071817.tar.gz), [**consensus JSONs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326650_HCGCYBCXY_consensus_UID18-cdr3nt-90_json_071817.tar.gz)
  - 326651
    - Sequences: [**raw FASTQs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326651_HC5LVBCXY_raw-fastqs.tar.gz), [**consensus FASTAs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326651_HC5LVBCXY_consensus_UID18-cdr3nt-90_071817.tar.gz)
    - FASTQC: [**pre-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326651_HC5LVBCXY_pre-trimmed-fastqc.tar.gz), [**post-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326651_HC5LVBCXY_post-trimmed-fastqc.tar.gz)
    - Annotated data: **consensus CSVs**, [**consensus JSONs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326651_HC5LVBCXY_consensus_UID18-cdr3nt-90_jsons_071817.tar.gz)
  - 326713
    - Sequences: [**raw FASTQs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326713_HJLLNBCXY_raw-fastqs.tar.gz), [**consensus FASTAs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326713_HJLLNBCXY_consensus_UID18-cdr3nt-90_071817.tar.gz)
    - FASTQC: [**pre-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326713_HJLLNBCXY_pre-trimmed-fastqc.tar.gz), [**post-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326713_HJLLNBCXY_post-trimmed-fastqc.tar.gz)
    - Annotated data: **consensus CSVs**, [**consensus JSONs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326713_HJLLNBCXY_consensus_UID18-cdr3nt-90_jsons_071817.tar.gz)
  - 326737
    - Sequences: [**raw FASTQs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326737_HNKVKBCXY_raw-fastqs.tar.gz), [**consensus FASTAs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326737_HNKVKBCXY_consensus_UID18-cdr3nt-90_071817.tar.gz)
    - FASTQC:  [**pre-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326737_HNKVKBCXY_pre-trimmed-fastqc.tar.gz), [**post-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326737_HNKVKBCXY_post-trimmed-fastqc.tar.gz)
    - Annotated data: [**consensos CSVs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326737_HNKVKBCXY_consensus_UID18-cdr3nt-90_minimal_071817.tar.gz), [**consensus JSONs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326737_HNKVKBCXY_consensus_UID18-cdr3nt-90_json_071817.tar.gz)
  - 326780
    - Sequences: [**raw FASTQs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326780_HLH7KBCXY_raw-fastqs.tar.gz), [**consensus FASTAs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326780_HLH7KBCXY_consensus_UID18-cdr3nt-90_071817.tar.gz)
    - FASTQC:  [**pre-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326780_HLH7KBCXY_pre-trimmed-fastqc.tar.gz), [**post-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326780_HLH7KBCXY_post-trimmed-fastqc.tar.gz)
    - Annotated data: [**consensus CSVs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326780_HLH7KBCXY_consensus_UID18-cdr3nt-90_minimal_071817.tar.gz), [**consensus JSONs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326780_HLH7KBCXY_consensus_UID18-cdr3nt-90_json_071817.tar.gz)
  - 326797
    - Sequences: raw FASTQs [**1**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326797_HJLN5BCXY_raw-fastqs.tar.gz) [**2**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326797_HCGNLBCXY_raw-fastqs.tar.gz), [**consensus FASTAs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326797_HCGNLBCXY%2BHJLN5BCXY_consensus_UID18-cdr3nt-90_071817.tar.gz)
    - FASTQC: pre-trimming [**1**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326797_HJLN5BCXY_pre-trimmed-fastqc.tar.gz) [**2**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326797_HCGNLBCXY_pre-trimmed-fastqc.tar.gz), post-trimming [**1**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326797_HJLN5BCXY_post-trimmed-fastqc.tar.gz) [**2**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326797_HCGNLBCXY_post-trimmed-fastqc.tar.gz)
    - Annotated data: [**consensus CSVs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326797_HCGNLBCXY%2BHJLN5BCXY_consensus_UID18-cdr3nt-90_minimal_071817.tar.gz), [**consensus JSONs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326797_HCGNLBCXY%2BHJLN5BCXY_consensus_UID18-cdr3nt-90_json_071817.tar.gz)
  - 326907
    - Sequences: [**raw FASTQs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326907_HLT33BCXY_raw-fastqs.tar.gz), [**consensus FASTAs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326907_HLT33BCXY_consensus_UID18-cdr3nt-90_071817.tar.gz)
    - FASTQC:  [**pre-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326907_HLT33BCXY_pre-trimmed-fastqc.tar.gz), [**post-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326907_HLT33BCXY_post-trimmed-fastqc.tar.gz)
    - Annotated data: [**consensus CSVs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326907_HLT33BCXY_consensus_UID18-cdr3nt-90_minimal_071817.tar.gz), [**consensus JSONs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/326907_HLT33BCXY_consensus_UID18-cdr3nt-90_json_071817.tar.gz)
  - 327059
    - Sequences: [**raw FASTQs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/327059_HCGTCBCXY_raw-fastqs.tar.gz), [**consensus FASTAs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/327059_HCGTCBCXY_consensus_UID18-cdr3nt-90_071817.tar.gz)
    - FASTQC:  [**pre-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/327059_HCGTCBCXY_pre-trimmed-fastqc.tar.gz), [**post-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/327059_HCGTCBCXY_post-trimmed-fastqc.tar.gz)
    - Annotated data: [**consensus CSVs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/327059_HCGTCBCXY_consensus_UID18-cdr3nt-90_minimal_071817.tar.gz), [**consensus JSONs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/327059_HCGTCBCXY_consensus_UID18-cdr3nt-90_json_071817.tar.gz)
  - D103
    - Sequences: [**raw FASTQs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/D103_HCGCLBCXY_raw-fastqs.tar.gz), [**consensus FASTAs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/D103_HCGCLBCXY_consensus_UID18-cdr3nt-90_071817.tar.gz)
    - FASTQC:  [**pre-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/D103_HCGCLBCXY_pre-trimmed-fastqc.tar.gz), [**post-trimming**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/D103_HCGCLBCXY_post-trimmed-fastqc.tar.gz)
    - Annotated data: [**consensus CSVs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/D103_HCGCLBCXY_consensus_UID18-cdr3nt-90_minimal_071817.tar.gz), [**consensus JSONs**](http://burtonlab.s3.amazonaws.com/sequencing-data/hiseq_2016-supplement/D103_HCGCLBCXY_consensus_UID18-cdr3nt-90_json_071817.tar.gz)

For each subject, there are a total of 18 samples: 3 technical replicates of each of 6 biological replicates. Biological replicates refer to different aliquots of peripheral blood monomuclear cells (**PBMCs**), from which total RNA was separately isolated and processed. Thus, sequences or clonotypes found in multiple biological replicates are assumed to have independently occurred in different cells. Technical relicates refer to independent library preparations using the same aliquot of PBMC-derived RNA. In each of the above datasets, samples 1-6 are biological replicates. Samples 7-12 and 13-18 are technical replicates of samples 1-6.

Due to technical issues, the sequence data for subject 326797 was spread across two HiSeq flowcells. Thus, the raw FASTQs and FASTQC results can be downloaded in two separate batches. Starting with the first processed dataset (UMI-corrected consensus FASTAs), reads from both flowcells were pooled.  

### Synthetic antibody sequences 
We generated synthetic antibody sequences using [IGoR](https://github.com/qmarcou/IGoR). Two datasets of synthetic sequences are available. As with the repertoire sequencing datasets above, the annotated datasets are quite large (uncompressed, each exceeds 1TB in size).

  - Ten batches of 100M synthetic sequences, generated with IGoR's default V(D)J recombination model:
    - [**FASTAs**](http://burtonlab.s3.amazonaws.com/GRP_github_data/igor_synthetic_100M_default-model_fastas.tar.gz)
    - [**Annotated CSVs**](http://burtonlab.s3.amazonaws.com/GRP_github_data/synthetic_default-model_minimal.tar.gz)
  - Ten batches of 100M synthetic sequences, generated with subject-specific recombination models, inferred by IGoR using 500,000 unmutated antibody sequences from each subject:
    -  [**Subject-specific IGoR models**](http://burtonlab.s3.amazonaws.com/GRP_github_data/subject-specific_igor_models.tar.gz)
    - [**FASTAs**](http://burtonlab.s3.amazonaws.com/GRP_github_data/igor_synthetic_100M_subject-specific-models_fastas.tar.gz)
    - [**Annotated CSVs**](http://burtonlab.s3.amazonaws.com/GRP_github_data/synthetic_subject-specific-models_minimal.tar.gz)

## Requirements

  - Python 3.3+ (although Python 2.7 may work for many or most notebooks, this has not been tested)
  - [Jupyter Notebook](https://jupyter.org/install)

*Additionally, each notebook may require additional third-party Python packages. Any notebook-specific requirements, as well as instructions for package installation with [pip](https://pip.pypa.io/en/stable/installing/), are provided in each notebook.*

If you're new to Python, a great way to get started is to install the [Anaconda Python distribution](https://www.continuum.io/downloads), which includes pip as well as a ton of useful scientific Python packages.

