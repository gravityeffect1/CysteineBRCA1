# BRCA1 Protein Cysteine Residue Analysis

This Google Colab notebook provides a pipeline to fetch protein data from the UniProt API, extract its sequence, identify Cysteine (C) residue positions, and visualize these positions.

## Table of Contents
1.  [Introduction](#introduction)
2.  [Pipeline Steps](#pipeline-steps)
3.  [Default Protein](#default-protein)
4.  [Usage](#usage)
5.  [Functions](#functions)

## Introduction
Cysteine residues play crucial roles in protein structure and function, often forming disulfide bonds that stabilize protein folds or participating in catalytic activities. This notebook offers a programmatic way to analyze the distribution of Cysteine residues within a given protein sequence using public bioinformatics data.

## Pipeline Steps
1.  **Fetch Protein Data**: Retrieves comprehensive protein information, including the amino acid sequence, from the UniProt API using a specified accession ID.
2.  **Extract Protein Sequence**: Parses the fetched data to isolate the raw amino acid sequence.
3.  **Find Cysteine Positions**: Identifies all occurrences of Cysteine residues ('C') within the extracted sequence and records their 0-based indices.
4.  **Plot Cysteine Positions**: Generates a scatter plot visualizing the 1-based positions of Cysteine residues along the protein sequence, providing a quick overview of their distribution.

## Default Protein
By default, this notebook is configured to analyze the **BRCA1 protein** (UniProt Accession ID: `P38398`).

## Usage
To use this notebook, simply run all cells. You can modify the `brca1_accession_id` and `protein_name` variables in the last code cell to analyze a different protein.

## Functions
-   `fetch_protein_data(accession_id)`: Fetches protein data from UniProt.
-   `extract_protein_sequence(protein_data)`: Extracts the sequence from the fetched data.
-   `find_cysteine_positions(sequence)`: Locates Cysteine residues in a sequence.
-   `plot_cysteine_positions(sequence_length, cysteine_positions, protein_name)`: Plots the positions of Cysteine residues.
