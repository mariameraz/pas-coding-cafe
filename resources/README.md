# Resources

This document collects **libraries, tools, tutorials, and learning resources**
shared by the PAS community, with a focus on **plant breeding, plant genetics, genomics, and omics**.  

This is a **living document**, feel free to contribute! ₊˚⊹♡

## How to contribute

- Add a short description (reference if available)
- Tool type: Library / Software / Tutorial / Book / Pipeline / Web tool
- Language/environment: R / Python / CLI / GUI

---

## 🌱 Plant Breeding & Genomic Selection

- **[rrBLUP](https://cran.r-project.org/package=rrBLUP)** (R): Ridge regression BLUP and G-BLUP for genomic prediction, including genomic relationship matrix estimation and mixed-model GWAS (Endelman, 2011).

- **[BGLR](https://cran.r-project.org/package=BGLR)** (R): Bayesian whole-genome regression (BayesA/B/C, RKHS) for continuous, binary, and ordinal traits, with multi-environment GxE support (Pérez & de los Campos, 2014, *Genetics*).

- **[sommer](https://cran.r-project.org/package=sommer)** (R): Mixed model solver with flexible covariance structures for hybrid prediction (GCA, SCA), multi-environment trials, and additive + dominance models (Covarrubias-Pazaran, 2016, *PLOS ONE*).

- **[AlphaSimR](https://gaynorr.github.io/AlphaSimR/)** (R): Stochastic simulation of breeding programs, supporting genomic selection, doubled haploids, speed breeding, and selection indices for diploid and autopolyploid species (Gaynor et al., 2021, *G3*).

- **[GAPIT](https://zzlab.net/GAPIT/)** (R): GWAS and genomic prediction suite implementing MLM, MLMM, FarmCPU, and BLINK with automatic Manhattan and Q-Q plot output (Lipka et al., 2012, *Bioinformatics*; Tang et al., 2016, *PLOS Genetics*).

---

## 🧬 Genetic Mapping & QTL Analysis

- **[R/qtl](https://rqtl.org)** (R): Classic QTL mapping for experimental crosses (F2, RILs, DH) using interval mapping, composite interval mapping, and permutation-based thresholds (Arends et al., 2010, *Bioinformatics*).

- **[qtl2](https://kbroman.org/qtl2/)** (R): Modern reimplementation of R/qtl for high-density markers and multiparental populations (MAGIC, CC/DO lines), with LMM support for population structure (Broman et al., 2019, *Genetics*).

- **[ASMap](https://cran.r-project.org/package=ASMap)** (R): Builds genetic linkage maps via the MSTmap algorithm, efficient for large marker sets, with map diagnostics and R/qtl integration (Taylor & Butler, 2017, *Journal of Statistical Software*).

---

## 🖥️ GWAS & Genome-wide Association

- **[PLINK 1.9](https://www.cog-genomics.org/plink/)** (CLI): Standard toolkit for genotype QC (HWE, call rate, MAF), LD pruning, PCA, and basic association tests (Chang et al., 2015, *GigaScience*).

- **[PLINK 2.0](https://www.cog-genomics.org/plink/2.0/)** (CLI): Full PLINK rewrite for WGS and biobank-scale data, introducing the PGEN format, multi-allelic variant support, and parallelized GLM (Chang & Rivas, actively maintained 2024).

- **[GCTA](https://yanglab.westlake.edu.cn/software/gcta/)** (CLI): Suite for SNP-based heritability (GREML), LMM-GWAS (fastGWA), conditional and joint analysis (COJO), and genomic prediction (Yang et al., 2011, *American Journal of Human Genetics*).

- **[GEMMA](https://github.com/genetics-statistics/GEMMA)** (CLI): Univariate and multivariate LMM for GWAS with population structure correction; active development continues as PanGEMMA (Dec. 2024) (Zhou & Stephens, 2012, *Nature Genetics*).

- **[REGENIE](https://rgcgithub.github.io/regenie/)** (CLI): Whole-genome block ridge regression for large cohorts and thousands of phenotypes, with approximate Firth logistic test for unbalanced binary traits (Mbatchou et al., 2021, *Nature Genetics*).

---

## 🌍 Population Genetics & Introgression

- **[Dsuite](https://github.com/millanek/Dsuite)** (CLI): Fast C++ implementation of Patterson's D (ABBA-BABA) and f4-ratio statistics across all population combinations from VCF files, including windowed analyses and the f-branch method (Malinsky et al., 2021, *Molecular Ecology Resources*).

- **[VCFtools](https://vcftools.github.io)** (CLI): Filters, summarizes, and compares VCF files; calculates FST, HWE, and LD statistics for population genetics analyses (Danecek et al., 2011, *Bioinformatics*).

- **[bcftools](https://samtools.github.io/bcftools/)** (CLI): Fast VCF/BCF manipulation, filtering, and annotation; more capable than VCFtools for most tasks and recommended for modern variant pipelines (Danecek et al., 2021, *GigaScience*).

---

## 🌟 Omics & High-throughput Data Analysis

- **[HISAT2](https://daehwankimlab.github.io/hisat2/)** (CLI): Splice-aware aligner based on a hierarchical graph FM index; memory-efficient (~6.7 GB for large genomes) and faster than STAR, with higher accuracy for reads containing SNPs (Kim et al., 2019, Nature Biotechnology).

- **[kallisto](https://pachterlab.github.io/kallisto/)** (CLI): Ultra-fast transcript quantification via pseudoalignment — processes 30M reads in under 3 minutes without full genome alignment (Bray et al., 2016, *Nature Biotechnology*).

- **[Salmon](https://combine-lab.github.io/salmon/)** (CLI): Quasi-mapping transcript quantification with bias correction; integrates directly with DESeq2 via tximeta/tximport (Patro et al., 2017, *Nature Methods*).

- **[STAR](https://github.com/alexdobin/STAR)** (CLI): Splice-aware RNA-seq aligner for mapping reads to annotated reference genomes; fast, accurate, and widely used in plant transcriptomics (Dobin et al., 2013, *Bioinformatics*).

- **[MultiQC](https://multiqc.info/)** (CLI/Python): Aggregates QC reports from FastQC, STAR, Salmon, and dozens of other tools into a single interactive HTML report across all samples (Ewels et al., 2016, *Bioinformatics*).

- **[DESeq2](https://bioconductor.org/packages/DESeq2)** (R/Bioconductor): Standard for RNA-seq differential expression using negative binomial models with empirical Bayes dispersion shrinkage; robust with small sample sizes (Love et al., 2014, *Genome Biology*).

- **[edgeR](https://bioconductor.org/packages/edgeR)** (R/Bioconductor): Differential expression for count data (RNA-seq, ATAC-seq, ChIP-seq) using quasi-likelihood GLMs; a solid alternative to DESeq2 for very small sample sizes (Robinson et al., 2010, *Bioinformatics*).

- **[topGO](https://bioconductor.org/packages/topGO)** (R/Bioconductor): GO term enrichment that accounts for the topology of the GO graph, reducing false positives from parent-child dependencies between terms (Alexa et al., 2006, *Bioinformatics*).

- **[clusterProfiler](https://bioconductor.org/packages/clusterProfiler)** (R/Bioconductor): ORA and GSEA enrichment against GO, KEGG, and Reactome with publication-ready visualizations; the most widely used enrichment package in plant transcriptomics (Wu et al., 2021, *The Innovation*).

- **[mixOmics](https://mixomics.org)** (R): Multi-omics integration using latent projection methods (PCA, PLS, DIABLO) for studies combining transcriptomic, metabolomic, proteomic, and genomic data (Rohart et al., 2017, *PLOS Computational Biology*).

- **[QIIME 2](https://qiime2.org)** (CLI/Python): End-to-end microbiome analysis platform for amplicon and metagenomic data, with a plugin system, interactive visualizations, and built-in data provenance tracking (Bolyen et al., 2019, *Nature Biotechnology*).

- **[WGCNA](https://cran.r-project.org/web/packages/WGCNA/index.html)** (R): Builds weighted gene co-expression networks and identifies modules of highly correlated genes; widely used to link gene clusters to traits or conditions (Langfelder & Horvath, 2008, BMC Bioinformatics).

- **[Cytoscape](https://cytoscape.org)** (GUI): Open sourcce-Desktop platform for visualizing and analyzing biological networks and graphs; supports plugins for co-expression, protein-protein interaction, and pathway visualization (Shannon et al., 2003, Genome Research).

---

## 💻 Bioinformatics & Genomics

- **[Bioconductor](https://www.bioconductor.org)** (R): Ecosystem of hundreds of R packages for genomic data analysis (RNA-seq, ChIP-seq, variant annotation), with strict versioning standards for reproducibility (Gentleman et al., 2004, *Genome Biology*).

---

## 📊 Data Visualization

- **[ggplot2](https://ggplot2.tidyverse.org)** (R): The dominant R plotting system based on the grammar of graphics, with a large extension ecosystem for publication-ready figures (Wickham, 2016, Springer).

- **[patchwork](https://patchwork.data-imaginist.com)** (R): Combines multiple ggplot2 figures into composite layouts using `+`, `/`, and `|`; handles alignment, sizing, and shared legends automatically (Pedersen, 2024).

- **[CMplot](https://cran.r-project.org/package=CMplot)** (R): Generates Manhattan and Q-Q plots — including Circular Manhattan Plots — directly from GWAS result tables; widely used in plant genomics publications (Yin et al., actively maintained).

- **[matplotlib](https://matplotlib.org)** (Python): Core Python plotting library with fine-grained control over every figure element; the foundation for most Python visualization tools (Hunter, 2007, *Computing in Science & Engineering*).

- **[seaborn](https://seaborn.pydata.org)** (Python): High-level statistical graphics in Python for distributions, correlations, and categorical data; integrates naturally with pandas DataFrames (Waskom, 2021, *Journal of Open Source Software*).

---

## 📈 Statistics & Experimental Analysis

- **[lme4](https://cran.r-project.org/package=lme4)** (R): Standard package for linear and generalized linear mixed-effects models (LMM/GLMM) for nested designs, repeated measures, and multi-environment experiments (Bates et al., 2015, *Journal of Statistical Software*).

- **[emmeans](https://cran.r-project.org/package=emmeans)** (R): Computes estimated marginal means from fitted models with pairwise comparisons, contrasts, and multiple testing corrections; compatible with lme4, lm, glm, and many others (Lenth, 2024).

- **[SpATS](https://cran.r-project.org/package=SpATS)** (R): Fits spatial trend models in field trials using two-dimensional P-splines to correct for soil variability without requiring a predefined experimental structure (Rodríguez-Álvarez et al., 2018, *JABES*).

- **[statsmodels](https://www.statsmodels.org)** (Python): Statistical modeling in Python — OLS/GLS, GLMs, time series, and hypothesis tests — with R-style formula interfaces and detailed model summaries (Seabold & Perktold, 2010, *Proceedings of SciPy*).

---

## 🔁 Reproducibility & Workflow Management

- **[Quarto](https://quarto.org)**: Next-generation scientific publishing system unifying R Markdown and Jupyter for reproducible documents, presentations, and websites across R, Python, Julia, and Observable.

- **[Snakemake](https://snakemake.readthedocs.io)**: Python-based workflow manager for bioinformatics pipelines with explicit input/output rules, automatic parallelization, and HPC/cloud support (Mölder et al., 2021, *F1000Research*).

- **[renv](https://rstudio.github.io/renv/)** (R): Per-project R package libraries with lockfiles for reproducibility across machines and time (Ushey & Wickham, 2023).

- **[conda / mamba](https://docs.conda.io)**: Environment and package managers for Python, R, and CLI tools; `mamba` offers significantly faster dependency solving and is recommended for complex bioinformatics environments.

---

## 📚 Learning & References

- **[R for Data Science](https://r4ds.hadley.nz)** (2nd ed.) — Wickham, Çetinkaya-Rundel & Grolemund (2023)

- **[The Tidyverse Style Guide](https://style.tidyverse.org)** — Wickham

- **[Happy Git with R](https://happygitwithr.com)** — Bryan et al.

- **[Bioinformatics Handbook](https://eriqande.github.io/eca-bioinf-handbook/)** — Anderson et al.: Comprehensive open handbook covering Unix, reproducible workflows, sequence alignment, variant calling, and population genomics — a great all-in-one reference for bioinformatics in R and the command line.


