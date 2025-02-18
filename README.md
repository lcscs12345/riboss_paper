## Use cases and benchmarking results for RIBOSS

[RIBOSS](https://github.com/lcscs12345/riboss) leverages ribosome profiling and RNA-seq data (with optional transcriptome assembly) to identify non-canonical ORFs in prokaryotes and eukaryotes. RIBOSS employs a unique comparative approach, assessing the translational potential of non-canonical ORFs relative to annotated ORFs, as described in our [preprint](https://doi.org/10.1101/2024.11.07.622529). 

This repository provides Jupyter Notebooks demonstrating RIBOSS's functionality in various scenarios:

*   **_Salmonella enterica_ serovar Typhimurium:** This [notebook](https://github.com/lcscs12345/riboss_paper/blob/main/jupyter_notebooks/styphimurium.ipynb) demonstrates the use of RIBOSS for analysing organisms with incomplete annotations, specifically missing transcription start/termination sites and intercistronic regions. It showcases how RIBOSS can be used to discover novel translational events in these contexts.

*   **_Arabidopsis thaliana_:** This [notebook](https://github.com/lcscs12345/riboss_paper/blob/main/jupyter_notebooks/ribotricer-arabidopsis-wu_2024.ipynb) illustrates how to use RIBOSS with a complete reference transcriptome. It provides a typical use case for eukaryotes.

*   **_Homo sapiens_:**  Similar to the *Arabidopsis* example, this [notebook](https://github.com/lcscs12345/riboss_paper/blob/main/jupyter_notebooks/riboss-human-park_2016.ipynb) demonstrates RIBOSS usage with a complete human reference transcriptome, demonstrating its applicability to complex eukaryotic transcriptomes.

Further details on benchmarking results and performance evaluation can be found within the _Arabidopsis_ and human notebooks. Additional notebooks detail the preparation of positive controls for benchmarking, specifically [human Ribo-Seq ORFs](https://github.com/lcscs12345/riboss_paper/blob/main/jupyter_notebooks/riboseqorfs.ipynb) and [Araport uORFs](https://github.com/lcscs12345/riboss_paper/blob/main/jupyter_notebooks/araport.ipynb).

To visualise the non-canonical ORFs detected, the bigGenePred tracks can be uploaded to the UCSC Genome Browser by pasting the URLs, for example:
```
track type=bigGenePred name="sORFs" description="RIBOSS top hits" baseColorDefault=genomicCodons bigDataUrl=https://github.com/lcscs12345/riboss_paper/raw/refs/heads/main/results/styphimurium/riboss/ERR9130942_3.riboss.sig.sORF.bb
```



