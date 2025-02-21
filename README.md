# Alphafold3 Server

## Description:
This is a collection of helpful Python scripts for working with Alphafold3, FASTA/Genbank/JSON files, and related scripts! I had found it quite frustrating to work with the AF3 server (found here: https://alphafoldserver.com/), copying and pasting every FASTA sequence, so I created a set of Python3 notebooks to do work with AF3 in a high throughput manner. 

## Note:
Most of these only work for protein sequences without any post-translational modifications (PTMs) including phosphorylation, glycosylation, SUMOlation, etc. Trying to update to include this!

## Contents:
1. FAA_TO_JSON_LOCAL_CLEAN.ipynb will convert a local .faa file to individual .json files formatted for AF3.
   Input: A .faa file, its file location, and an output directory
   Output: Formatted .json files for each protein in the .faa file in your specified directory
2. GB_DIRECTORY_TO_JSON_CLEAN.ipynb will convert a directory of .gb files to new folders in your given output file path, each containing a .json file for each individual .gb file. It will name both the folder and the file based off of the species name in the .gb file.
   Input: A file path to a directory of individual .gb files
   Output: Individual folders with one .json file each both named for the species name of an input .gb file
3. Added NC_ACCESSION_TO_JSON_NCBI_CLEAN.ipynb will download a NCBI Accession number and process it into a .json file formatted for the AF3 Server.
   Input: NCBI NC Accession number, your email, and an output directory.
   Output: .json file formatted for AF3 Server within your specified output directory.
4. Added GB_TO_JSON_UPDATE_2024_11_25.ipynb that will convert .gb files into output .json files. Works for both miRNAs and proteins (note: for miRNAs, AF will just display a small line without much structural information as they are very small).
   Input: Folder containing your .gb files
   Output: .json files in separate folders
5. Added JSON_SUM_CONFID_CLEAN.ipynb that will record, organize, clean, and store output metrics from your "fold_your_protein_summary_confidences_#.json" files in a .csv
   Input: Directory containing your summary confidence files (can be a parent directory of predicted AF3 models and it will walk through all of them)
   Output: .csv containing information on your models' 'fraction_disordered', 'has_clash', 'num_recycles', 'ptm', 'ranking_score', 'chain_iptm', 'chain_pair_iptm', 'chain_pair_pae_min', 'chain_ptm.
6. Added AF3_AVERAGE_PLDDT_JSON_CLEAN_2025_01_06.ipynb that will summarize the length of your predicted structure as well as the average plddt for your model (as the server does not readily give that).
   Input: Directory containing your fold_protein_name_full_data_#.json files
   Output: .csv with your protein name, protein length, and average plddt
7. GB_TO_FAA_WALK_CLEAN_2025_02_21.ipynb will take a parent directory of .gb files and create .faa files for each protein found in your .gb files. Useful when comparing orthologs among related species for downstream MSA.
   Input: Directory containing your .gb files
   Output: Two different files - 1 .faa file for every protein and individual isoforms and combined files of a protein as well as all of its isoforms (i.e. protein_A_alpha.faa, protein_A_beta.faa, and protein_A_combined.faa)

### Updated 2025-02-21
