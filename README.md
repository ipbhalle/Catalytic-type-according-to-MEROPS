# Secreted Protease Annotation Pipeline

This repository provides a workflow for identifying and annotating secreted proteases based on PFAM domain information, with catalytic types classified according to [MEROPS - the Peptidase Database](https://www.ebi.ac.uk/merops/).

## Overview

The pipeline extracts protease-related PFAM domains and traces their corresponding catalytic types. Each protease is annotated with metadata indicating its catalytic type.

### Catalytic Types

| Code | Catalytic Type |
|------|----------------|
| A    | Aspartic       |
| C    | Cysteine       |
| G    | Glutamic       |
| M    | Metallo        |
| N    | Asparagine     |
| P    | Mixed          |
| S    | Serine         |
| T    | Threonine      |
| U    | Unknown        |

## Required Files

The following Excel files are required for running the pipeline:

- `Guy_11_Compiled.xlsx`  
- `Protein_accession_final.xlsx`  
- `PFAM.xlsx`

## Workflow

1. **Gene-PFAM Mapping**  
   Use `Protein_accession_final.xlsx` to connect `Gene_ID`s from `Guy_11_Compiled.xlsx` with their corresponding PFAM domains.

2. **PFAM Annotation**  
   Retrieve PFAM family and subfamily information for the mapped genes using `PFAM.xlsx`.

3. **Catalytic Type Assignment**  
   Using MEROPS classification, assign a catalytic type to each protease based on its associated PFAM domain.

## Output

The final output includes all matched genes with:

- PFAM domain(s)
- Family and subfamily information
- Assigned catalytic type

## License

This project is intended for academic and research purposes. Please cite relevant sources when using this dataset or pipeline

