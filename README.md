# Sequence Analysis Toolkit

A Python notebook for basic DNA sequence analysis.
Built while learning Python and bioinformatics. 
The code includes my own notes to help me understand how certain parts works.

## What does it do?

Given a DNA sequence, the notebook reports:

- 📏 Sequence length
- 🧬 GC content (as a percentage)
- 🔄 Reverse complement
- 🟢 Translation to protein sequence
- 📖 ORF finding (forward strand, frame 1 only)

## How to run it

1. Open `sequence_analysis_toolkit.ipynb` in Jupyter Notebook or JupyterLab.
2. Run each cell from top to bottom (**Kernel → Restart Kernel and Run All Cells**).
3. When prompted, type or paste a DNA sequence and press Enter.

No extra libraries are needed, only standard Python.

## Example

**Input:**

```
GCTAGCTAGCTAGCTAGCATGGCAACCGTCTTAGCATAAAGCTAGCTAGCTAGCTA
```

**Output:**

```
Length: 56
GC content as a %: 48.214285714285715
The reverse complement of this sequence is: TAGCTAGCTAGCTAGCTTTATGCTAAGACGGTTGCCATGCTAGCTAGCTAGCTAGC
The codon sequence is: AS*LASMATVLA*S*LAS
The ORF is: ['ATGGCAACCGTCTTAGCATAA']
```

## Limitations

- The ORF finder only searches the forward strand and reading frame 1, so ORFs starting at other positions or on the reverse strand are missed.
- Input must contain only A, C, G and T. Other characters (such as N) will cause an error.
- It takes typed input and does not read FASTA files yet.

## Possible future improvements

- Search all three reading frames (frame 1, 2 and 3) on both strands
- Read sequences from FASTA files
