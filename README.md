# Alphafold3

## Description:
This is a collection of helpful Python scripts for working with Alphafold3, FASTA/Genbank/JSON files, and related scripts! I had found it quite frustrating to work with the AF3 server (found here: https://alphafoldserver.com/), copying and pasting every FASTA sequence, so I created a set of Python3 notebooks to do work with AF3 in a high throughput manner.

## Contents:
1. FAA_TO_JSON_LOCAL_CLEAN.ipynb will convert a local .faa file to individual .json files formatted for AF3.
   Input: A .faa file, its file location, and an output directory
   Output: Formatted .json files for each protein in the .faa file in your specified directory
2. GB_DIRECTORY_TO_JSON_CLEAN.ipynb will convert a directory of .gb files to new folders in your given output file       path, each containing a .json file for each individual .gb file. It will name both the folder and the file based      off of the species name in the .gb file.
   Input: A file path to a directory of individual .gb files
   Output: Individual folders with one .json file each both named for the species name of an input .gb file

## Update log:
1. 2024-07-15 Initial commit of FAA_TO_JSON_LOCAL_CLEAN.ipynb
2. 2024-07-16 Initial commit of GB_DIRECTORY_TO_JSON_CLEAN.ipynb
