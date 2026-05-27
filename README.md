# Single-Cell RNA-seq Neuronal Cell Type Classification in Mouse

## Project Summary
This project predicts neuronal cell types from mouse single-cell RNA-seq expression profiles. It uses curated labels from the Allen Brain Atlas, applies standard preprocessing (QC, normalization, and highly variable gene selection), and compares a baseline multinomial logistic regression model with a stronger ensemble classifier. It is machine learning classification of mouse neuronal cell types from Allen Brain Atlas single-cell RNA-seq expression profiles.

## Abstract
We propose a supervised learning approach to classify neuronal cell types from mouse single-cell RNA-seq expression profiles. Expression matrices and curated cell-type labels were obtained from the Allen Brain Atlas Cell Types dataset. After quality filtering, normalization, and selection of highly variable genes, models were trained to predict neuronal cell-type labels. We compare a baseline multinomial logistic regression model to a stronger ensemble method and evaluate performance using accuracy, macro F1, and confusion matrices. Results show that transcriptomic signatures are highly informative for distinguishing neuronal subtypes, while errors highlight closely related cell types with overlapping gene expression. This study demonstrates how machine learning can support automated annotation of neuronal identity from single-cell data.

## Repository Structure
- allen_mouse_celltype_ml.ipynb: Main analysis notebook
- data/: place the downloaded dataset here (not tracked)
- outputs/: saved figures or exported tables (not tracked)
- requirements.txt: Python dependencies

## Dataset Download
1. Visit the Allen Brain Atlas Cell Types portal: https://celltypes.brain-map.org/
2. The notebook is configured for the mouse cortex/hippocampus SMART-seq expression matrix and matching metadata CSV.
3. Place downloaded files in the `data/` folder, or let the notebook download missing files when internet access is available.

## Quick Start
1. Create and activate a Python environment.
2. Install dependencies:
   - pip install -r requirements.txt
3. Open and run `allen_mouse_celltype_ml.ipynb`.

## Notes
- The default target is `subclass_label`, which gives a biologically meaningful neuronal subtype task.
- The notebook caps each class at 300 cells to keep runtime manageable on a laptop while preserving class balance.

## Citation
If you use this project, please cite the following:
- Data source: https://celltypes.brain-map.org/ (Allen Brain Atlas Cell Types)
- Dataset: Allen Institute for Brain Science mouse cortex/hippocampus SMART-seq cell types data.
- Project Source: https://github.com/iamsinghridima/RNA-seq-Neuron-Classification

## Authors
- Name: Ridima Singh, Prabhleen Kaur Saini, Mani Gupta, Eshita Tandon, and Aaryak Srivastava
- Affiliation: Indian Institute of Science Education and Research, Mohali, India
