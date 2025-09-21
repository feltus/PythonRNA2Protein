# PythonRNA2Protein

## Python Practice: Translating RNA into Protein

## Background
Eukaryotic cells flow genetic information from DNA to RNA to PROTEIN. The transcription of DNA into RNA with Python was covered in a previous skill. In this lab, you will convert RNA into protein with Python. The genetic code was deciphered in the 1960s after the discovery that DNA stores genetic information in the 1950s. In essence, the genetic code explains how DNA encodes functional information. Transcribed RNA contains codons which are trinucleotides that encode one of twenty amino acids. The genetic code provides a mapping of codons to specific amino acids.

Amino acids are bonded to each other in a specific protein sequence that is assembled during translation. Amino acid sequences (aka proteins) fold into a 3D structure that perform specific functions in a cell. For example, ‘AUG’ is the RNA codon for the amino acid called methionine (abbreviated M) and here is a translation of a nine nucleotide RNA molecule into a three amino acid protein:

```
AUGUCAUCG (RNA) ——> translation ——> MSM (protein)
```

Below is the full genetic code in the form of a Python dictionary. Note that some amino acids are coded by multiple codons. Also, ‘AUG’ typically is the first codon in an RNA so most proteins begin with M as the first amino acid. Three other codons do not code for amino acids but signal the end of translation. These codons are called stop codons and include ‘UGA’, ‘UAA’, and ‘UAG’.

```
rna2protein = {“UUU”:”F”, “UUC”:”F”, “UUA”:”L”, “UUG”:”L”,
“UCU”:”S”, “UCC”:”S”, “UCA”:”S”, “UCG”:”S”,
“UAU”:”Y”, “UAC”:”Y”, “UAA”:””, “UAG”:””,
“UGU”:”C”, “UGC”:”C”, “UGA”:””, “UGG”:”W”,
“CUU”:”L”, “CUC”:”L”, “CUA”:”L”, “CUG”:”L”,
“CCU”:”P”, “CCC”:”P”, “CCA”:”P”, “CCG”:”P”,
“CAU”:”H”, “CAC”:”H”, “CAA”:”Q”, “CAG”:”Q”,
“CGU”:”R”, “CGC”:”R”, “CGA”:”R”, “CGG”:”R”,
“AUU”:”I”, “AUC”:”I”, “AUA”:”I”, “AUG”:”M”,
“ACU”:”T”, “ACC”:”T”, “ACA”:”T”, “ACG”:”T”,
“AAU”:”N”, “AAC”:”N”, “AAA”:”K”, “AAG”:”K”,
“AGU”:”S”, “AGC”:”S”, “AGA”:”R”, “AGG”:”R”,
“GUU”:”V”, “GUC”:”V”, “GUA”:”V”, “GUG”:”V”,
“GCU”:”A”, “GCC”:”A”, “GCA”:”A”, “GCG”:”A”,
“GAU”:”D”, “GAC”:”D”, “GAA”:”E”, “GAG”:”E”,
“GGU”:”G”, “GGC”:”G”, “GGA”:”G”, “GGG”:”G”}
```

In this lab, you will write Python translation code and apply it to all known human protein coding sequences.

## Task: Write Python code that translates RNA to protein in FASTA format.
reads the FASTA formatted DNA sequence file, “transcribes” the DNA into RNA, “translates” the DNA sequences into a peptide sequence, and writes FASTA formatted RNA and protein sequence files.

### Step 1. Make a working directory and create a text file called '2dna.fasta' and paste these two concatenated FASTA-format DNA CDS sequences in the file:

```
>ENST00000632684.1
GGGACAGGGGGC
>ENST00000434970.2
CCTTCCTAC
```

### Step 2. Make a Jupyter notebook called 'dna2rna2protein.ipynb'

Write Python code in dna2rna2protein.ipynb that reads the FASTA formatted DNA sequence file from Step 1, “transcribes” the DNA into RNA, “translates” the DNA sequences into a peptide sequence, and writes FASTA formatted RNA and protein sequence files. Start by mapping out the algorithm in pseudocode. Carefully check that your input and output are correct for both CDS files.

TIP: DO NOT WRITE ANY PYTHON CODE BEFORE YOU HAVE THOUGHT THROUGH THE STEPS IN PSEUDOCODE.
TIP: DO not have Prometheus write your code. Ask for help if you get stuck and make sure you understand each line of your code. That way, you learn how to code and you don't get fired in a job when they ask you to write code ;).

### Step 3. Use a web browser to find the all the protein coding (CDS) sequences for the human genome from ENSEMBL. 
Here is where you can find the single concatenated FASTA CDS DNA sequence file: http://useast.ensembl.org/info/data/ftp/index.html

You can download to your working directory with the command line using this command:

```
wget https://ftp.ensembl.org/pub/release-114/fasta/homo_sapiens/cds/Homo_sapiens.GRCh38.cds.all.fa.gz
```

### Step 4. Use your Python code from Task A to transcribe all DNA CDS sequences into single concatenated RNA sequence file in FASTA format and translate all the RNA sequences into a single concatenated protein sequence file in FASTA format.

### Step 5. Verify that the input (RNA) and output (PROTEIN) sequences are correct and then turn in your jupyter notebook in Canvas.
