# OTC3-OTC% Mawj project
This project was realised for Mawj Mandwie (mmandwie@cmri.org.au) from CMRI.
The aim of this project is to seperate reads following alleles. There is a total of 12 samples from OTC3 patients.
It's a short read, pair ended sequencing.

"I am interested in looking at the number of reads from each allele in each sample. "
 

## **Dataset consist in:** 

S1-LFF10626_L1_1.fq

S1-LFF10626_L1_2.fq

## Workflow
The Snakefile containt the code for the analysis.

**Step 1:**
OTC3
Fatsqc shows that overall reads are of good quality


Quality filtering remove reads of quality under 20: 
Removal is high. I havelet the biologist know about it.
```
Input:                  	6914800 reads 		2074440000 bases.
Low quality discards:   	444330 reads (6.43%) 	133299000 bases (6.43%)
Total Removed:          	444330 reads (6.43%) 	133299000 bases (6.43%)
Result:                 	6470470 reads (93.57%) 	1941141000 bases (93.57%)
 ```

**Step 2:**

merge forward and reverse

```
Read combination statistics:
Pairs:               	3235235
Joined:              	3222645   	99.611%
Ambiguous:           	12522   	0.387%
No Solution:         	68       	0.002%
Too Short:           	0       	0.000%

 ```
**Step 3:**
Download and align against the chrX of the human genome

**Step 4:**
Generate bam files 
**Step 5:**

Aligned read against ChrX=3,222,075

SNP: GRCh38ChrX, position: 38401295 ref A alt G


	
  |**Barcode**|   **Barcode+ Forward primer**    |**Donor cells**|   **mouse ID**   |**Number of reads** |**% of reads** |**Number of reads Allele G**|**Number of reads Allele A**|
|:-----------|:-----------|:-----------|:-----------|:-----------|:-----------|	:-----------|:-----------|	
|**GTTCA**|GTTCATGCTATGGCTATCAGCAGATCTGAA   |        OTC3 P0|229|306060|9.50|35633|269876|
|**GTCAT**|GTCATTGCTATGGCTATCAGCAGATCTGAA  | OTC3 P0|57|364315|11.30|41802|	321912|	     
|**CTGTA**|CTGTATGCTATGGCTATCAGCAGATCTGAA   |        OTC3 P0|76|248130|7.70|32152|	215529|
|**GTATT**|GTATTTGCTATGGCTATCAGCAGATCTGAA   |       OTC3 P0|77|206448|	6.41	|21815|184183	|
|**CTAGT**|CTAGTTGCTATGGCTATCAGCAGATCTGAA   |         OTC3 P0|100|279648	|8.68|26770|252371|
|**ACTTC**|ACTTCTGCTATGGCTATCAGCAGATCTGAA   |        OTC3 P0|101|270527|8.39|25434|	244526	|
|**CCTAT**|CCTATTGCTATGGCTATCAGCAGATCTGAA   |        OTC3 P0|88|263710|8.18	|31285|231813|
|**ACTGA**|ACTGATGCTATGGCTATCAGCAGATCTGAA   |        OTC3 P0|68|316127|9.81	|46307|	269242|		
|**TCCAA**|TCCAATGCTATGGCTATCAGCAGATCTGAA   |        OTC3 P0|98|279552|8.67|46427|232676|	
|**GCATT**|GCATTTGCTATGGCTATCAGCAGATCTGAA   |        OTC3 P0| 99|309494|9.60|41279|267655|	
|**TCAAG**|TCAAGTGCTATGGCTATCAGCAGATCTGAA   |        OTC3 P0|102|234390|7.27|27731|	206261|	




# OTC3-July-2023
