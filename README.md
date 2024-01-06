# PPM
**P**ersonal **P**DB **M**aker
*A.D. 2023*

PPM.Mk.I.Beta

*β_σ version contains residues A, G and K only*

Code for a Python function to generate a Protein Data Base (PDB) file with the added option of Ubiquitylation and side chain modification.

This generates a linear PDB file **based** off of a single letter amino acid code (FASTSA) sequence **e.g** input = AAA generates a pdb file that contains three alanines.

The residues are generated from N->C termini, along with the proper PDB CONECT record.

The user merely enters their desired sequence and ends with a \* to signify the C-terminus. Following the above example, the input AAA* generates three alanines with connection records and a proper C-terminus. 

#**Branched version**
This version allows the user to modify a respecitve amino acid. The '^' symbol specifies when the branched sequence should start, and the '*' specifies when to end the branched sequence.

Since Ubiquitylation is common, the sequence of the branched chain will start in reverse: So, K^AAG\*KK\* sequence consists of three lysienes, with the first lysine having the sequence GAA attached to its sidechain via a isopeptide bond. 

If reverse is set to false, then the branched sequence will connect to the respective residue via its N-terminus. 

#**Issues**
* Does not contain hydrogen records (use pyMol or WebMo to add hydrogens)
* Atom Index jumps by +1 after branched chain
* CONECT record stops short of last few residues
* some bond lengths are not ideal so your vizualizer (VMD, pyMol, etc.) might add some random bonds here and there
* Isopeptide bond between Lys and branched C-term. is too short
* messy code pls dont hate me

This code was written by me (peter swanson) and me alone. I have no professional affiliations to any company/institution 

# I WILL CONTINUE TO UPDATE THIS STUFF SO PLS BE NICE TO ME
