# Off-Target Profiling of CRISPR Editing at the LRRK2 Gene Using the CHANGE-seq Dataset

This project analyzes off-target effects of CHANGE-seq data, focusing on the LRRK2 gene region, using BigWig files containing histone modification signals.
The notebook automatically fetches signal data, visualizes histone modifications across the LRRK2 region, identifies genome-wide off-target peaks, and ranks the strongest off-target sites.

Additionally, this work is part of building a larger NGS pipeline for CRISPR genome editing experiments. We are preparing for upcoming sequencing data from our own experiments. To gain experience and develop robust analysis workflows, I'm working first with existing public datasets like this one to understand off-target effects — and this project serves as a foundation for applying similar analyses to our own upcoming sequenced datasets.

## Colab notebook: Change_seq_LRRK2_off-target_analysis.ipynb ; Output files: Per-histone-mark off-target peak CSV files, Combined master peak file, LRRK2-specific peak file, Top 50 off-target peaks ranked by signal strength

### Steps performed:
(1) Loaded histone modification BigWig files.

(2) Visualized signal intensity across the LRRK2 region.

(3) Detected genome-wide off-target peaks above a defined threshold.

(4) Generated a combined peak file.

(5) Filtered peaks specific to LRRK2.

(6) Visualized off-target peak distribution across chromosomes.

(7) Ranked top 50 strongest off-target peaks.

####  Visualizations:
(1) Histone mark signals over the LRRK2 gene.

(2) Bar plot of off-target peaks across all chromosomes.

##### How to Run:
(1) Upload the notebook to Google Colab (2) Set the correct paths to your project folders (3) Run the cells step-by-step (4) Outputs will be saved automatically

###### Notes:
A signal threshold of 5 was used to define off-target peaks. Focused analysis was performed on chromosome 12 (LRRK2: chr12:40,567,000–40,653,000).

**Requirements:**
CHANGE_seq dataset: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE149295 ;

Python 3.x, Packages: pyBigWig, numpy, matplotlib, pandas, os

**Contributing:** Pull requests are welcome. If you have suggestions for improving the analysis or visualizations, feel free to open an issue.
