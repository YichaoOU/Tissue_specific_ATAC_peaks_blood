# GATA1 usage in different blood cells

<p><img src='https://raw.githubusercontent.com/YichaoOU/Tissue_specific_ATAC_peaks_blood/master/motif_analysis/GATA1_usage.svg'></p>

## Step 1. Extract DNA sequences given the bed files.

1. install bedtools, https://bedtools.readthedocs.io/en/latest/

2. download human genome sequences (version: hg19)

3. run `bedtools getfasta` to extract DNA sequences

The extracted DNA sequences are provided in the `fasta_sequence` folder.

## Step 2. Perform motif scanning 

1. Run GATA1 motif (`GATA1.meme`) scanning using FIMO with default parameters. 

2. Calculate the number of sequences containing the GATA1 motif.

3. Calculate percentange of sequences containing the GATA1 motif: %Sequence = N_sequence/Total_sequence.

Put the %Sequence in a table like `GATA1_Npeaks.list`

## Step 3. Plot GATA1 usage on blood lineage.

1. Install Python, and dependencies such as pandas, seaborn, matplotlib, numpy, scipy.

2. Run `python plot_blood_lineage.py -f GATA1_Npeaks.list -o GATA1_usage -s blood_lineage_Hchang_13cells.svg`

Output figure is `GATA1_usage.svg`

