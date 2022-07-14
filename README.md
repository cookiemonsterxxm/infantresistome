# infantresistome
The Python custome scripts were used for upstream metagenomics workflow:

ARGnTAXA_finaltab.py -- This script generates the "final" output file of the ARG workflow. It combines output from three different intermediate steps:
(1) step6-megares alignment file providing ARG read/sequence ID and MEGID
(2) step9-Contig ID and the aligned ARG read ID
(3) step10-Contig ID and the taxonomy assignment


make_RPKG_normtab.py -- This script requies 4 input files 2 and output file paths:
	Input:
	(1) (Optional) MicrobeCensus output txt file. 
	(2) (Optional) Organized table of MEGARes database gene length. 
	(3) (Optional) Resistome Analyzer gene level output. Other levels are also included in this file and can be collapsed in final output files if desired. 
	(4) (Optional) A wildcard input indicating normalized tables to be merged. 
	Output:
	(1) (Required for python 2.x) Individual normalized table.
	(2) (Optional) Merged normalized table containg multiple samples from Input(4). Can be omitted to not have a merged table.


prefix_to_compline.py -- This script converts partial headers extracted from sam file to full headers based on contigs. 
For example, convert "k141_0" to "k141_0 flag=0 multi=1.0000 len=225". 
The output file containing all the headers is used to select contigs containg ARGs. 

