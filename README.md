# L1TD1_ORF1p_Binding_Sites_Prediction

## Files
cleaning_training_final_project.ipynb → Notebook with code for data cleaning and model fine-tuning using Weights & Biases
trained_final_project.ipynb → Notebook with code for final model and analysis of binding sites learned by models
l1td1_seq_df.csv/orf1_seq_df.csv → Data for transcript sequences that have L1TD1 or ORF1p bound or unbound to it

## l1td1_seq_df.csv/orf1_seq_df.csv
L1TD1 RIP-seq Data retrieved from [GSE254459](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE254459)

ORF1p RIP-seq Data retrieved from [GSE287102](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE287102)

Methods:
1. Fastq files were pulled from SRA and aligned to [transcriptome](https://www.gencodegenes.org/human/#) using Salmon.
2. Differential expression analysis was conducted using DESeq2 comparing input and IP samples to determine transcripts as bound (LFC > 1 and padj < 0.05) and unbound (LFC < -1 and padj < 0.05).

## Acknowledgements
Portions of this code were based on code provided by Sofia Salazar in [TF Binding Prediction — Starter Code](https://gene46100-2026.hakyimlab.org/post/unit00/notebook-05-tf-binding-starter)

This project was developed with the assistance of Claude and Gemini for code generation and debugging.
