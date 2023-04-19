# PRauto
 
#### PRauto is a tool that provides two main functionalities: [ Data Retrieval ] and [ Data Preprocessing ]                                                               in Bioinformatic and Chemoinformatics.
_______________________________________________________________________________________________________________________________________
### Install
To install the PRauto, users can input the following command in the command-line interface:
  
```bash
   pip install PRauto
```
###
### Data Retrieval

![PRauto_retrieve map](https://user-images.githubusercontent.com/96029849/232976971-21218261-f0f6-483c-b82f-77594ddf9113.png)
  
  
#### To use the Data Retrieval feature, users can input the following command in the command-line interface:

```bash
   python -m prauto
```

This tool allows users to retrieve the FASTA file of a target protein sequence via a search query in the UniProt API.  
Additionally, using the UniProt accession number, PRauto retrieves the PDB files of target protein from the RCSB PDB API and  
sdf files of ligands that interact with the target protein from the ChEMBL API.

#### The output of this feature includes : 
1. the target protein sequences in a FASTA file format 
2. PDB files of the target protein structures
3. sdf files of the ligands that interact with the target protein

________________________________________________________________________________________________________________________________________
###
### Data Preprocessing

<figure class="half">
    <img src="![unaligned0001](https://user-images.githubusercontent.com/96029849/232978931-2598d4b2-9d89-4aa9-aa03-dbb9cd02efd9.png)">
    <img src="![aligned0001](https://user-images.githubusercontent.com/96029849/232978971-2a6a60b2-5715-41fe-af48-71babf6414ee.png)">
figure>

#### To use the Data Preprocessing feature, users can input the following command in the command-line interface:

```bash
   python -m prauto.prepauto
```

This tool processes PDB files that are located in a single directory.  
It extracts only the chain(s) that correspond to the target protein and aligns them according to the reference PDB file.  
It also removes any unnecessary molecules that are not involved in the binding of the primary ligand.  
In a PSE PyMOL session, these unnecessary molecules are hidden rather than being removed.

#### The output of this feature includes : 
1. preprocessed PDB files
2. PSE PyMOL session file.

___________________________________________________________________________________________________________________________________________
