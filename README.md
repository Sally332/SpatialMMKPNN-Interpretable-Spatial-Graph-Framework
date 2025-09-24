# SpatialMMKPNN — Interpretable Spatial Graph Framework
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)
![License](https://img.shields.io/badge/License-MIT-green)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17189130.svg)](https://doi.org/10.5281/zenodo.17189130)

*A modular and interpretable graph framework for spatial transcriptomics in the tumor microenvironment.*  

## Overview  
SpatialMMKPNN is a framework for **exploring how signals may be organized in the tumor microenvironment**, not just predicting outcomes. It combines a **Graph Attention Network (GAT)** with a **Knowledge-Primed Neural Network (KPNN)** so predictions stay tied to **biological units—pathways, ligand–receptor pairs, and spatial niches**.  

The framework was built with three guiding principles:  
- **Methodological originality:** the framework does not apply conventional pipelines but introduces a new design that makes graph-based models transparent and adaptable. Each application—immune exclusion, stromal remodeling, and therapy resistance—illustrates this design in practice, addressing major challenges in cancer biology.  
- **Interpretability by design:** results are expressed as pathway attributions, ligand–receptor drivers, and spatial attention maps, so that the reasoning behind model outputs can be directly examined.  
- **Modular structure:** graph construction, role assignment, and interpretation layers are implemented as independent steps, making the workflow flexible and reusable across applications.  

The goal is to show **how interpretable graph models can be applied to spatial transcriptomics** and to make the design decisions visible for scrutiny and refinement.  

Each notebook can be rerun end-to-end to regenerate outputs, with summary CSVs and plots provided for quick reference.  

## Applications  

### Prototype — Framework Demonstration  
A controlled exercise where ligand–receptor axes were deliberately seeded into the design to test whether the model could recover them. This demonstration shows that SpatialMMKPNN can retrieve expected biological signals and map them back to pathways and spatial regions in an interpretable way. It serves as a baseline validation of the framework.  

### 1. Immune Exclusion vs Infiltration (IEvI)  
Focuses on how immune cells access or are excluded from the tumor rim. The module quantifies enrichment of stromal, chemokine, and vascular signals at tumor boundaries, distinguishing exclusion motifs from infiltration patterns. It illustrates how rim geometry can be analyzed transparently and how conclusions remain stable under different parameter choices.  

### 2. Stromal Remodeling  
Explores fibrotic and adhesive rims in FFPE slides, where the stroma builds physical and biochemical barriers around tumors. By analyzing adhesive (SPP1) and fibrotic (TGFB) signaling, this module shows how stromal interfaces reshape the tumor edge. It demonstrates how the framework handles challenging FFPE data while keeping the workflow reproducible.  

### 3. Therapy-Induced Rewiring (TIR)  
Applies the framework to paired pre- and post-therapy samples from hepatocellular carcinoma patients. It reveals how treatment changes not just the strength of signaling axes but also their spatial distribution across tumor interiors and boundaries. This module highlights how therapy shifts the microenvironment, separating **magnitude changes** from **spatial redistribution**, and provides interpretable evidence of rewiring.  

## Organization  
This repository is organized as **modular applications**.  
Each application folder includes:  
- A **README** describing the aim, method, results, limitations, and interpretation.  
- A **notebook** with **cell-by-cell explanations**, design choices, and troubleshooting notes.  
- An **outputs** directory with summary CSVs and plots illustrating the main findings.  

These applications are first implementations of the approach. Future work will focus on **stronger quality control, larger sample sizes, improved robustness analyses, and addressing current limitations** within the same modular structure.  

## Citation  
If you use or adapt this framework, please cite:  
**Yepes S. SpatialMMKPNN: Interpretable Spatial Graph Framework for the Tumor Microenvironment. GitHub, 2025.**  
