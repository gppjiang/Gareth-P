# Claude skills

This folder holds Claude Code skills for this repository. Claude loads every `SKILL.md` under `.claude/skills/` automatically, so the skills below are available in any Claude Code session opened on this repo.

## K-Dense scientific skills

All 177 skills here are copied from [K-Dense-AI/claude-scientific-skills](https://github.com/K-Dense-AI/claude-scientific-skills) (commit `5f2bc03`, 26 October 2026). They cover bioinformatics and single-cell omics (scanpy, scvi-tools, anndata, pydeseq2, bulk RNA-seq, pathway enrichment), statistics and modelling (statsmodels, pymc, scikit-learn, scikit-survival, statistical power, PK/PD), metabolism and chemistry (13C metabolic flux, cobrapy, rdkit, pyopenms, matchms), literature and database lookup, scientific writing, grants, figures and posters, and lab automation.

### Source and license

- The collection is © 2025 K-Dense Inc. and released under the MIT License. A copy of that license is in [LICENSE-K-Dense.md](LICENSE-K-Dense.md).
- Each skill also states its own `license` in its `SKILL.md` front matter, usually the license of the tool it wraps. Most are MIT, BSD-3-Clause or Apache-2.0. Check these before commercial use or redistribution:
  - Non-commercial: `deepspot-m` (PolyForm Noncommercial 1.0.0), `what-if-oracle` (CC BY-NC-SA 4.0)
  - Copyleft: `bioservices` (GPL-3.0), `cobrapy` (GPL-2.0), `etetoolkit` (GPL-3.0-or-later)
  - Paid API: `rowan` (proprietary, API key required)
  - Not stated: `glycoengineering`, `hugging-science`, `infographics`, `latex-posters`, `phylogenetics`, `primekg`, `pyhealth`
  - `imaging-data-commons`: the skill is MIT, but IDC data carries its own licenses (mostly CC-BY, some CC-NC)

### Updating

To pull a newer version, re-copy the upstream `skills/` folder over this one and update the commit reference above:

```bash
git clone --depth 1 https://github.com/K-Dense-AI/claude-scientific-skills /tmp/kdense
rsync -a --delete --exclude README.md --exclude LICENSE-K-Dense.md /tmp/kdense/skills/ .claude/skills/
```

## Skill index

| Skill | What it does |
|---|---|
| [`13c-metabolic-flux`](13c-metabolic-flux/SKILL.md) | Estimates intracellular metabolic fluxes from steady-state carbon-13 isotope-tracing measurements using validated atom maps, mfapy isotope simulation, constr... |
| [`adaptyv`](adaptyv/SKILL.md) | Uses the Adaptyv Bio Foundry API and Python SDK to design protein characterization experiments, estimate costs, submit sequences, monitor laboratory progress... |
| [`aeon`](aeon/SKILL.md) | This skill should be used for time series machine learning tasks including classification, regression, clustering, forecasting, anomaly detection, segmentati... |
| [`alphagenome`](alphagenome/SKILL.md) | Looks up precomputed AlphaGenome Atlas effects for any GRCh38 single-nucleotide variant (AVI score with Phred and 18 SHAP feature attributions, plus raw and... |
| [`analytical-method-validation`](analytical-method-validation/SKILL.md) | Plans, executes, and documents validation, verification, and transfer of analytical procedures under the governing framework - ICH Q2(R2) and Q14, USP <1220>... |
| [`anndata`](anndata/SKILL.md) | Handles annotated matrices in single-cell analysis, .h5ad and Zarr files, and integration with the scverse ecosystem. |
| [`arbor`](arbor/SKILL.md) | Applies Arbor Hypothesis Tree Refinement to research artifacts with repeatable evaluators, including model training, agent harnesses, data synthesis and benc... |
| [`arboreto`](arboreto/SKILL.md) | Infers candidate gene regulatory networks from bulk or single-cell expression data using AertsLab Arboreto GRNBoost2 and GENIE3. |
| [`astropy`](astropy/SKILL.md) | Core Python library for astronomy and astrophysics workflows that need Astropy APIs, including units/quantities, coordinates, FITS I/O, tables, time systems,... |
| [`autoskill`](autoskill/SKILL.md) | Analyzes user-requested Screenpipe history windows to detect repeated research workflows, match existing scientific skills, and stage new skill drafts or com... |
| [`benchling-integration`](benchling-integration/SKILL.md) | Benchling Python SDK and REST API integration for registry entities, inventory, ELN entries, workflows, Benchling Apps, and Data Warehouse queries. |
| [`bgpt-paper-search`](bgpt-paper-search/SKILL.md) | Searches BGPT scientific papers by topic or DOI and retrieves claim-level evidence extracted from full text, including experiments, reported statistics, scop... |
| [`bids`](bids/SKILL.md) | > Organizes, queries, validates, and converts Brain Imaging Data Structure (BIDS) datasets. |
| [`biopython`](biopython/SKILL.md) | Provides Biopython workflows for sequence manipulation, file parsing (FASTA/GenBank/PDB), phylogenetics, and programmatic NCBI/PubMed access (Bio.Entrez). |
| [`bioservices`](bioservices/SKILL.md) | Provides a Python interface to bioinformatics services including UniProt, KEGG, ChEMBL, Reactome, QuickGO, and UniChem. |
| [`bulk-rnaseq`](bulk-rnaseq/SKILL.md) | Prepares bulk RNA-seq FASTQ, Salmon, STAR or featureCounts output for gene-level differential expression. |
| [`cantera`](cantera/SKILL.md) | Runs Cantera homogeneous chemical reactors and evaluates ignition delay with mechanism provenance, conservation checks, and numerical refinement. |
| [`cellprofiler`](cellprofiler/SKILL.md) | Runs reproducible CellProfiler microscopy pipelines for nuclear segmentation, cell counts, and per-object fluorescence measurements. |
| [`cellxgene-census`](cellxgene-census/SKILL.md) | Queries the CZ CELLxGENE Census programmatically for versioned public single-cell and spatial transcriptomics data. |
| [`cirq`](cirq/SKILL.md) | Google quantum computing framework. |
| [`citation-management`](citation-management/SKILL.md) | Comprehensive citation management for academic research. |
| [`clinical-decision-support`](clinical-decision-support/SKILL.md) | Prepares and validates research-only clinical decision-support evaluation, evidence-profile, cohort, survival, biomarker/model, privacy, and governance artif... |
| [`clinical-reports`](clinical-reports/SKILL.md) | Creates safety-bounded draft structures and runs local deterministic checks for clinical case, diagnostic, trial, safety, and aggregate research reports. |
| [`cobrapy`](cobrapy/SKILL.md) | Performs constraint-based metabolic modeling with COBRApy, including FBA, pFBA, FVA, gene knockouts, flux sampling, growth media, production envelopes, gap f... |
| [`consciousness-council`](consciousness-council/SKILL.md) | Structures a multi-perspective council exercise for decisions, research trade-offs, and creative challenges. |
| [`dask`](dask/SKILL.md) | Scales pandas, NumPy, and custom Python research workflows beyond memory or across clusters with Dask. |
| [`database-lookup`](database-lookup/SKILL.md) | Queries documented public database APIs with explicit endpoints, filters, pagination, and provenance. |
| [`datalad`](datalad/SKILL.md) | Retrieves, versions, and publishes scientific datasets with DataLad and git-annex, and captures computational provenance with datalad run, rerun, and contain... |
| [`datamol`](datamol/SKILL.md) | Pythonic wrapper around RDKit with simplified interface and sensible defaults. |
| [`deepchem`](deepchem/SKILL.md) | Builds molecular property prediction and MoleculeNet workflows with DeepChem, including SMILES featurization, scaffold or grouped holdouts, masked labels, gr... |
| [`deepspot-m`](deepspot-m/SKILL.md) | Generates transcriptome-wide virtual spatial transcriptomics from H&E histology with DeepSpot-M. |
| [`deeptools`](deeptools/SKILL.md) | NGS analysis toolkit. |
| [`depmap`](depmap/SKILL.md) | Retrieves and analyzes Cancer Dependency Map (DepMap) release data, including CRISPR Chronos gene effects, cancer model annotations, omics biomarkers, and PR... |
| [`dhdna-profiler`](dhdna-profiler/SKILL.md) | Applies the DHDNA framework as an exploratory rubric for reasoning and writing patterns in supplied text. |
| [`diffdock`](diffdock/SKILL.md) | Predicts protein-small-molecule binding poses with DiffDock and DiffDock-L from PDB or sequence plus SMILES/SDF/MOL2. |
| [`dnanexus-integration`](dnanexus-integration/SKILL.md) | Builds and operates reproducible genomics workloads on DNAnexus with the dx CLI, dxpy, apps/applets, native workflows, dxCompiler, and Nextflow. |
| [`esm`](esm/SKILL.md) | Uses the Biohub esm Python SDK for ESM3 protein generation, ESMC embeddings, and ESMFold2 all-atom folding. |
| [`etetoolkit`](etetoolkit/SKILL.md) | Analyzes, manipulates, compares, annotates, and visualizes phylogenetic or other hierarchical trees with ETE 4. |
| [`exa-search`](exa-search/SKILL.md) | Searches scientific and technical web content with Exa and extracts page or PDF text from URLs in batches. |
| [`experimental-design`](experimental-design/SKILL.md) | Designs experiments and studies BEFORE data is collected — choosing a design, randomizing, blocking, and laying out treatment combinations so results are int... |
| [`exploratory-data-analysis`](exploratory-data-analysis/SKILL.md) | Performs bounded, local exploratory analysis of explicitly supported scientific files. |
| [`fictiv`](fictiv/SKILL.md) | Operates Fictiv (app.fictiv.com), the on-demand manufacturing platform, end to end in the users browser. |
| [`flowio`](flowio/SKILL.md) | Reads, inspects, and writes Flow Cytometry Standard (FCS) 2.0, 3.0, and 3.1 files with FlowIO. |
| [`flowkit`](flowkit/SKILL.md) | Analyzes flow cytometry data with FlowKit, including spillover compensation, logicle and biexponential transforms, hierarchical gating, GatingML strategies,... |
| [`fluidsim`](fluidsim/SKILL.md) | Plans, configures, inspects, restarts, and analyzes bounded FluidSim computational-fluid-dynamics simulations with explicit numerical-validity and HPC safety... |
| [`folklore-variant-evidence`](folklore-variant-evidence/SKILL.md) | Retrieves ClinGen gene-disease validity assertions for a public gene or disease, and reviews source-linked public evidence and literature for one supported G... |
| [`generate-image`](generate-image/SKILL.md) | Generates or edits images with AI models through the OpenRouter Image API (Gemini, Seedream, Recraft, GPT-Image, Riverflow). |
| [`geniml`](geniml/SKILL.md) | Supports audited local Geniml genomic-interval workflows: validate BED and universe contracts, plan Region2Vec or scEmbed runs, inspect model/tokenizer compa... |
| [`genomic-coordinates`](genomic-coordinates/SKILL.md) | Converts genomic intervals between coordinate conventions, normalises and compares variant representations, and detects assembly or contig-naming mismatches... |
| [`genomic-intelligence`](genomic-intelligence/SKILL.md) | Predicts regulatory features, gene structure, and expression directly from DNA sequence using Genomic Intelligences hosted transformer DNA language models —... |
| [`geomaster`](geomaster/SKILL.md) | Supports geospatial research workflows for remote sensing, vector and raster GIS, spatial statistics, terrain and network analysis, and machine learning for... |
| [`geopandas`](geopandas/SKILL.md) | Guidance and local audit tools for Python workflows that directly use GeoPandas GeoSeries, GeoDataFrame, spatial operations, or vector-data I/O. |
| [`get-available-resources`](get-available-resources/SKILL.md) | Detects host inventory and effective CPU, memory, disk, scheduler, container, and accelerator limits when a user asks for resource-aware planning or before a... |
| [`gget`](gget/SKILL.md) | Queries 20+ bioinformatics resources through CLI/Python. |
| [`ginkgo-cloud-lab`](ginkgo-cloud-lab/SKILL.md) | Guides protocol selection, input preparation, pricing checks, and browser ordering on Ginkgo Bioworks Cloud Lab (cloud.ginkgo.bio). |
| [`glycoengineering`](glycoengineering/SKILL.md) | Analyzes and engineers protein glycosylation by scanning canonical N-glycosylation sequons, describing S/T-rich regions, checking curated glycan evidence, an... |
| [`gtars`](gtars/SKILL.md) | Supports Gtars for local genomic interval models and set algebra, overlaps and counts, consensus and coverage, tokenization, fragment processing, and refget/... |
| [`histolab`](histolab/SKILL.md) | Extracts and preprocesses whole-slide histology image tiles with Histolab. |
| [`hugging-science`](hugging-science/SKILL.md) | Discovers and evaluates scientific datasets, models, methodology posts, and Spaces through the Hugging Science catalog. |
| [`hypogenic`](hypogenic/SKILL.md) | Plans and audits use of ChicagoHAI HypoGeniC/HypoRefine for LLM-assisted hypothesis generation from labeled text datasets. |
| [`hypothesis-generation`](hypothesis-generation/SKILL.md) | Formulates evidence-bounded scientific questions, candidate hypotheses, rival explanations, causal or associational claims, discriminating predictions, measu... |
| [`imaging-data-commons`](imaging-data-commons/SKILL.md) | Queries and downloads public cancer imaging data from NCI Imaging Data Commons. |
| [`infographics`](infographics/SKILL.md) | Creates and reviews infographics with Nano Banana 2 via OpenRouter. |
| [`iso-standards-readiness`](iso-standards-readiness/SKILL.md) | Prepares and structurally reviews readiness evidence for ISO management-system and laboratory-competence standards - ISO 13485 medical device QMS, ISO 14971... |
| [`lab-hardware-cad`](lab-hardware-cad/SKILL.md) | Designs custom laboratory hardware as parametric build123d models and exports fabrication artifacts as STEP, STL, and DXF files - microfluidic chips and mold... |
| [`labarchive-integration`](labarchive-integration/SKILL.md) | Integrates with the official LabArchives ELN REST-like API and Inventory API v1. |
| [`lamindb`](lamindb/SKILL.md) | Manages biological datasets and models with LaminDB, including artifact registration, lineage tracking, schema validation, Bionty ontology annotation, query/... |
| [`latchbio-integration`](latchbio-integration/SKILL.md) | Builds, registers, debugs, and operates bioinformatics workflows on Latch using the Python SDK, CLI, Latch Data and Registry, Nextflow, Snakemake, programmat... |
| [`latex-posters`](latex-posters/SKILL.md) | Creates research posters in LaTeX using beamerposter, tikzposter, or baposter. |
| [`liteparse`](liteparse/SKILL.md) | Local document and PDF parsing that returns spatial text with bounding boxes. |
| [`literature-review`](literature-review/SKILL.md) | Conducts systematic, scoping, and narrative literature reviews using PubMed, arXiv, bioRxiv, Semantic Scholar, and other appropriate sources. |
| [`mageck`](mageck/SKILL.md) | Analyzes pooled CRISPR screen FASTQ reads and guide-count matrices with MAGeCK, validates guide libraries and contrasts, measures replicate and library QC, a... |
| [`marine-carbonate-chemistry`](marine-carbonate-chemistry/SKILL.md) | Solves seawater carbonate chemistry with PyCO2SYS for chemical oceanography, ocean acidification, and marine carbon-cycle research. |
| [`markdown-mermaid-writing`](markdown-mermaid-writing/SKILL.md) | Writes scientific Markdown documentation and Mermaid diagrams for workflows, relationships, timelines, and schemas. |
| [`market-research-reports`](market-research-reports/SKILL.md) | Builds evidence-traceable market research reports and assumption-driven market sizing or forecast scenarios. |
| [`markitdown`](markitdown/SKILL.md) | Converts heterogeneous documents and selected URIs to Markdown with Microsoft MarkItDown for text analysis, search, and LLM/RAG ingestion. |
| [`matchms`](matchms/SKILL.md) | Processes, cleans, compares, and searches tandem mass spectra with matchms. |
| [`matlab`](matlab/SKILL.md) | Builds, reviews, migrates, and plans MATLAB or GNU Octave numerical workflows. |
| [`matplotlib`](matplotlib/SKILL.md) | Creates and customizes scientific plots with Matplotlib. |
| [`medchem`](medchem/SKILL.md) | Applies medicinal chemistry filters for compound triage, using drug-likeness rules (Lipinski, Veber, CNS), structural alert catalogs (PAINS, NIBR, ChEMBL), c... |
| [`modal`](modal/SKILL.md) | Modal is a serverless cloud platform for running Python on demand, including on-demand GPUs. |
| [`molecular-dynamics`](molecular-dynamics/SKILL.md) | Runs and analyzes molecular dynamics simulations with OpenMM and MDAnalysis. |
| [`molfeat`](molfeat/SKILL.md) | Featurizes small molecules with Molfeat for QSAR/QSPR, chemical similarity, virtual screening, and molecular ML. |
| [`ncats-arax`](ncats-arax/SKILL.md) | Queries the NCATS Translator ARAX production API for bounded, typed, provenance-rich one-hop and endpoint-pinned two-hop biomedical knowledge-graph relations... |
| [`networkx`](networkx/SKILL.md) | Creates, analyzes, and visualizes complex networks and graphs in Python with NetworkX. |
| [`neurokit2`](neurokit2/SKILL.md) | Builds and audits reproducible NeuroKit2 research workflows for physiological time-series preprocessing, event/interval analysis, multimodal alignment, varia... |
| [`neuropixels-analysis`](neuropixels-analysis/SKILL.md) | Analyzes Neuropixels extracellular recordings end-to-end with SpikeInterface. |
| [`nextflow`](nextflow/SKILL.md) | Builds, runs, and debugs Nextflow DSL2 pipelines and nf-core workflows. |
| [`nmrglue`](nmrglue/SKILL.md) | Processes calibrated one-dimensional complex NMR free-induction decays with nmrglue into phased spectra, peak candidates, and signed integration regions. |
| [`nwb-conversion`](nwb-conversion/SKILL.md) | Converts neuroscience acquisition data to Neurodata Without Borders files with NeuroConv and PyNWB, preserves metadata and timebases, checks evidence-based c... |
| [`omero-integration`](omero-integration/SKILL.md) | Inspects and automates microscopy data workflows against OMERO.server with omero-py, BlitzGateway, OMERO CLI, tables, annotations, ROIs, rendering, and docum... |
| [`onekgpd`](onekgpd/SKILL.md) | > Queries the 1000 Genomes Project dataset (3,202 whole-genome-sequenced individuals, GRCh38) at the level of individual participants. |
| [`ontology-term-resolution`](ontology-term-resolution/SKILL.md) | Resolves free-text scientific labels to ontology term IDs and validates existing CURIEs against the EBI Ontology Lookup Service (OLS4). |
| [`open-notebook`](open-notebook/SKILL.md) | Organizes research with the self-hosted Open Notebook alternative to NotebookLM. |
| [`openpiv`](openpiv/SKILL.md) | Performs Particle Image Velocimetry (PIV) analysis with OpenPIV. |
| [`opentrons-integration`](opentrons-integration/SKILL.md) | Authors, reviews, migrates, simulates, and troubleshoots official Opentrons Python Protocol API v2 protocols for Flex and OT-2 robots. |
| [`optimize-for-gpu`](optimize-for-gpu/SKILL.md) | GPU-accelerates scientific Python on NVIDIA hardware and verifies that the result is correct and faster. |
| [`pacsomatic`](pacsomatic/SKILL.md) | Prepares and launches nf-core/pacsomatic matched tumor-normal PacBio HiFi genomics workflows from unaligned BAM inputs. |
| [`paper-lookup`](paper-lookup/SKILL.md) | Searches 18 scholarly APIs for papers, preprints, citations, open-access full text, repository records, and journal OA status, and returns results with repro... |
| [`paperclip`](paperclip/SKILL.md) | Searches and reads biomedical papers, FDA/PMDA/EMA documents, clinical trials, and protein records with the GXL Paperclip CLI and Python SDK. |
| [`paperzilla`](paperzilla/SKILL.md) | Reads projects, searches project feeds, and retrieves recommendations and canonical papers in Paperzilla through the pz CLI. |
| [`parallel-web`](parallel-web/SKILL.md) | Uses Parallel CLI for web search, URL extraction, deep research, structured data enrichment, entity discovery, and recurring web monitoring. |
| [`pathml`](pathml/SKILL.md) | Supports local computational pathology research with PathML: slide loading and tiling, preprocessing and QC, h5path storage, multiplex quantification, spatia... |
| [`pathogen-variant-surveillance`](pathogen-variant-surveillance/SKILL.md) | Queries public GenSpectrum LAPIS data for pathogen genomic surveillance, current lineage nomenclature, weekly sequence proportions, reporting delays, and des... |
| [`pathway-enrichment`](pathway-enrichment/SKILL.md) | Performs pathway and gene-set enrichment analysis on gene lists or ranked gene data and interprets the results. |
| [`peer-review`](peer-review/SKILL.md) | Prepares evidence-bounded, constructive peer-review drafts and structured manuscript assessments. |
| [`pennylane`](pennylane/SKILL.md) | Builds and differentiates PennyLane quantum circuits, hybrid PyTorch or JAX models, molecular VQE and QAOA workflows. |
| [`phylogenetics`](phylogenetics/SKILL.md) | Builds and analyzes phylogenetic trees using MAFFT multiple sequence alignment, IQ-TREE maximum likelihood with ModelFinder and branch support, and FastTree... |
| [`pi-agent`](pi-agent/SKILL.md) | Builds with and operates Pi, the minimal terminal coding harness. |
| [`pkpd-modeling`](pkpd-modeling/SKILL.md) | Pharmacokinetic and pharmacodynamic modelling and simulation - non-compartmental analysis, compartmental and population PK, PK/PD and exposure-response, TMDD... |
| [`polars`](polars/SKILL.md) | High-performance DataFrame library for Python ETL, analytics, and pandas migration. |
| [`polars-bio`](polars-bio/SKILL.md) | Performs genomic interval overlap, nearest, merge, coverage, complement and subtraction on Polars DataFrames, and reads or writes BED, VCF, BCF, BAM, CRAM, G... |
| [`pptx-posters`](pptx-posters/SKILL.md) | Creates and audits editable scientific posters in macro-free PowerPoint (.pptx) from author-approved local content and assets. |
| [`primekg`](primekg/SKILL.md) | Queries a pinned Precision Medicine Knowledge Graph (PrimeKG) CSV for typed gene, drug, disease, and phenotype nodes, direct associations, disease context, a... |
| [`primer-design`](primer-design/SKILL.md) | Designs and audits PCR and RT-qPCR primers with Primer3, explicit thermodynamic conditions, reference-based off-target amplification searches, and traceable... |
| [`protocolsio-integration`](protocolsio-integration/SKILL.md) | Reads, validates, and safely exports protocols.io data with current official REST/MCP contracts, or creates non-executing mutation plans. |
| [`pufferlib`](pufferlib/SKILL.md) | Version-aware guidance for PufferLib reinforcement-learning environments, vectorization, policies, PuffeRL training, evaluation, and safe checkpoint review. |
| [`pybamm`](pybamm/SKILL.md) | Simulates lithium-ion battery charge, discharge and rest experiments with PyBaMM, records parameter-set provenance, checks mesh and solver sensitivity, and c... |
| [`pycalphad`](pycalphad/SKILL.md) | Computes finite-temperature CALPHAD equilibria, phase fractions, and phase compositions from thermodynamic TDB databases using pycalphad. |
| [`pydeseq2`](pydeseq2/SKILL.md) | Performs bulk RNA-seq differential expression analysis with PyDESeq2, including count validation, formula designs, explicit contrasts, Wald tests, FDR correc... |
| [`pydicom`](pydicom/SKILL.md) | Reads, inspects, writes, transforms, and preflights local DICOM datasets and pixel data. |
| [`pyhealth`](pyhealth/SKILL.md) | Builds and validates PyHealth clinical machine-learning pipelines for EHR, signals, imaging, and medical codes. |
| [`pylabrobot`](pylabrobot/SKILL.md) | Develops and reviews PyLabRobot lab-automation resources, liquid-handling plans, offline simulations, and supported-device integrations. |
| [`pymatgen`](pymatgen/SKILL.md) | Analyzes, validates, converts, and transforms materials structures and computed materials data with pymatgen. |
| [`pymc`](pymc/SKILL.md) | Builds and checks Bayesian models with PyMC, including hierarchical models, NUTS MCMC, variational inference, mutable-data predictions, posterior predictive... |
| [`pymoo`](pymoo/SKILL.md) | Solves and validates single-, multi-, and many-objective optimization with pymoo, including NSGA-II, NSGA-III, MOEA/D, constraints, Pareto approximations, re... |
| [`pyopenms`](pyopenms/SKILL.md) | Processes mass spectrometry data with pyOpenMS. |
| [`pysam`](pysam/SKILL.md) | Provides Python/HTSlib workflows for genomic files. |
| [`pytdc`](pytdc/SKILL.md) | Provides Therapeutics Data Commons workflows through PyTDC for registry discovery, dataset access, task-aware splits, evaluator metrics, benchmark groups, an... |
| [`pytorch-lightning`](pytorch-lightning/SKILL.md) | Deep learning framework (PyTorch Lightning / lightning package). |
| [`pyzotero`](pyzotero/SKILL.md) | Manages Zotero reference libraries using the pyzotero Python client: retrieves, creates, updates, and deletes items, collections, tags, and attachments via t... |
| [`qiime2-amplicon`](qiime2-amplicon/SKILL.md) | Processes paired-end 16S amplicon reads into QIIME 2 ASVs and taxonomy with retained artifact provenance. |
| [`qiskit`](qiskit/SKILL.md) | Builds, simulates, transpiles, and executes quantum circuits with Qiskit and IBM Quantum Runtime. |
| [`qutip`](qutip/SKILL.md) | Simulate and audit closed and open quantum-system models with QuTiP 5, including deterministic, trajectory, steady-state, spectral, and phase-space workflows. |
| [`rdkit`](rdkit/SKILL.md) | Cheminformatics toolkit for fine-grained molecular control. |
| [`relion`](relion/SKILL.md) | Validates and executes RELION single-particle cryo-EM refinement and half-map postprocessing. |
| [`relsa-severity-assessment`](relsa-severity-assessment/SKILL.md) | Supports multivariate severity assessment and exploratory endpoint-time score forecasting for laboratory animal studies using the RELSA (RELative Severity As... |
| [`research-grants`](research-grants/SKILL.md) | Supports research proposal preparation and review for NSF, NIH, DOE, DARPA, and Taiwan NSTC, including opportunity-specific requirements, aims, review criter... |
| [`research-lookup`](research-lookup/SKILL.md) | Compiles current scholarly evidence for a scientific manuscript or research brief when the user explicitly asks to gather literature, references, background... |
| [`rowan`](rowan/SKILL.md) | Rowan is a cloud-native molecular modeling and medicinal-chemistry workflow platform with a Python API. |
| [`scanpy`](scanpy/SKILL.md) | Performs Scanpy single-cell RNA-seq QC, normalization, HVG selection, PCA/UMAP/t-SNE, clustering, exploratory marker ranking, pseudobulk preparation, visuali... |
| [`scholar-evaluation`](scholar-evaluation/SKILL.md) | Provides qualitative-first, evidence-traceable developmental review of scholarly works and audit low-stakes research-assessment rubrics with optional local q... |
| [`scientific-brainstorming`](scientific-brainstorming/SKILL.md) | Facilitates evidence-aware scientific ideation with independent generation, structured discussion, explicit assumptions, transparent evaluation, adversarial... |
| [`scientific-critical-thinking`](scientific-critical-thinking/SKILL.md) | Evaluates scientific claims and evidence quality. |
| [`scientific-schematics`](scientific-schematics/SKILL.md) | Generates scientific diagram drafts using Nano Banana 2 AI with smart iterative refinement. |
| [`scientific-slides`](scientific-slides/SKILL.md) | Builds slide decks and presentations for research talks. |
| [`scientific-visualization`](scientific-visualization/SKILL.md) | Creates and audits truthful, accessible, publication-ready scientific figures with Matplotlib, Seaborn, or Plotly. |
| [`scientific-writing`](scientific-writing/SKILL.md) | Drafts, revises, and audits scientific manuscripts or reports with explicit evidence provenance, reporting-guideline coverage, authorship accountability, con... |
| [`scikit-bio`](scikit-bio/SKILL.md) | Biological data toolkit. |
| [`scikit-learn`](scikit-learn/SKILL.md) | Supports machine learning in Python with scikit-learn. |
| [`scikit-survival`](scikit-survival/SKILL.md) | Builds, evaluates, and audits right-censored or competing-risk survival workflows with scikit-survival, including leakage-safe preprocessing, model selection... |
| [`scvelo`](scvelo/SKILL.md) | Performs RNA velocity analysis with scVelo from spliced and unspliced single-cell RNA counts. |
| [`scvi-tools`](scvi-tools/SKILL.md) | Fits probabilistic models for single-cell omics, including scVI batch integration, scANVI annotation, totalVI CITE-seq, MultiVI RNA/ATAC integration, and pos... |
| [`seaborn`](seaborn/SKILL.md) | Creates Seaborn statistical visualizations with pandas integration for distributions, relationships, categorical comparisons, regression displays, pair plots... |
| [`shap`](shap/SKILL.md) | Explain and audit machine-learning predictions with SHAP. |
| [`simpy`](simpy/SKILL.md) | Builds, inspects, tests, and analyzes bounded process-based discrete-event simulations with SimPy. |
| [`stable-baselines3`](stable-baselines3/SKILL.md) | Trains and evaluates single-agent reinforcement learning with Stable Baselines3 (PPO, SAC, DQN, TD3, DDPG, A2C), Gymnasium custom environments, vectorized ro... |
| [`statistical-analysis`](statistical-analysis/SKILL.md) | Guided statistical analysis for research data - test selection, assumption checking, effect sizes, power analysis, Bayesian alternatives, and APA-formatted r... |
| [`statistical-power`](statistical-power/SKILL.md) | Calculates sample sizes and statistical power for study planning. |
| [`statsmodels`](statsmodels/SKILL.md) | Fits and diagnoses Python statistical models including OLS, GLM, discrete and mixed models, ARIMA and SARIMAX. |
| [`sympy`](sympy/SKILL.md) | Performs exact symbolic mathematics with SymPy for algebra, calculus, equation solving, symbolic linear algebra, physics, and lambdify or LaTeX code generation. |
| [`tamarind`](tamarind/SKILL.md) | Provides access to a collection of open-source molecular design and structural biology tools on the Tamarind Bio platform, via its REST API or MCP server — n... |
| [`tellurium`](tellurium/SKILL.md) | Simulates biochemical kinetic models from SBML or Antimony with Tellurium and libRoadRunner, checks model units, compares deterministic parameter perturbatio... |
| [`tiledbvcf`](tiledbvcf/SKILL.md) | Stores and retrieves genomic variant calls with TileDB-VCF. |
| [`timesfm-forecasting`](timesfm-forecasting/SKILL.md) | Performs zero-shot time-series forecasting with Googles TimesFM, including regular-grid CSV preparation, quantile forecasts, XReg covariates, and held-out ev... |
| [`torch-geometric`](torch-geometric/SKILL.md) | Supports PyTorch Geometric (PyG) graph neural networks — node/link/graph classification, message passing (GCN, GAT, GraphSAGE, GIN), heterogeneous graphs, ne... |
| [`torchdrug`](torchdrug/SKILL.md) | Builds and troubleshoots TorchDrug 0.2.1 workflows for molecular graphs, property prediction, self-supervised pretraining, molecule generation, retrosynthesi... |
| [`transformers`](transformers/SKILL.md) | Hugging Face Transformers for loading Hub models, running pipeline inference, text generation, and Trainer fine-tuning on NLP, vision, audio, and multimodal... |
| [`treatment-plans`](treatment-plans/SKILL.md) | Formats and structurally validates local treatment-plan documentation after clinical decisions have already been supplied and verified by authorized licensed... |
| [`umap-learn`](umap-learn/SKILL.md) | Applies UMAP-learn to nonlinear dimensionality reduction, 2D/3D embeddings, clustering preprocessing, supervised or semi-supervised UMAP, DensMAP, AlignedUMA... |
| [`uncertainty-and-units`](uncertainty-and-units/SKILL.md) | Tracks physical units and propagates measurement uncertainty in scientific calculations using pint and uncertainties. |
| [`usfiscaldata`](usfiscaldata/SKILL.md) | Queries the U.S. |
| [`vaex`](vaex/SKILL.md) | Processes large tabular scientific datasets with Vaex expressions, filtered views, streamed statistics, binned visualizations, and file conversion. |
| [`venue-templates`](venue-templates/SKILL.md) | Prepares journal manuscripts, conference papers, research posters, and grant documents using venue-specific formatting guidance and bundled LaTeX scaffolds. |
| [`waypoint-bio`](waypoint-bio/SKILL.md) | Supports work with Outpost Bios open microbiome foundation models - the Waypoint checkpoints (Waypoint-6m, Waypoint-45m, Waypoint-170m), the Atlas pretrainin... |
| [`what-if-oracle`](what-if-oracle/SKILL.md) | Supports structured what-if scenario analysis for research planning, experimental contingencies, and scientific project decisions. |
| [`zarr-python`](zarr-python/SKILL.md) | Stores and queries chunked N-D scientific arrays with Zarr-Python 3, including codecs, sharding, S3/GCS storage, and NumPy/Dask/Xarray integration. |
