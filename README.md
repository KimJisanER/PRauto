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
  <a href="link"><img src="https://user-images.githubusercontent.com/96029849/232979848-cf3af836-33f2-49a0-a024-abc690adc746.png"align="center" width="49%"></a>
  <a href="link"><img src="https://user-images.githubusercontent.com/96029849/232979950-e8c047a7-ef85-4917-b88f-b3c9da7302bc.png"align="center" width="49%"></a>
  <figcaption>Input PDB and output PDB (color and result are irrelevant)</figcaption>
</figure>

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
