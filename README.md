# OVERVIEW

Git Repository for 20.440 pest 4 / final project
Project title: Analysis of cochlear hair cell reprogramming in mice. 

Hair cells in the inner ear are integral for proper hearing, and damage to these cells can lead to hearing loss. In mammals, these cells do not regenerate, yet this is not the case in some non-mammalian vertebrates. It has been shown that reprogramming cochlear cells with certain transcription factors can lead to partially enhanced hearing. We conduct further analysis on gene expression data for reprogrammed cochlear cells using a dataset from Iyer et al., 2022.

For pset 4 - a simple UMAP was generated for wild type cochlear cell mRNA expression.
	

# DATA
scRNA seq of ATOH1, GFI1, and POUF4 reprogrammed cochlear hair cells from 3 genetically engineered mouse models (Iyer et al.).  Mice were bred to create 3 conditional overexpression lines (ATOH1, ATOH1+GFI1, and ATOH1+GFI1+POUF4). Tamoxofin was injected at postnatal day 1 or day 8  (P1/P8) to stimulate reprogramming and cochlear cells were purified on P8 or P15 with FACS (1 week after tamoxofin injection).  These cells were used for scRNA seq. Lastly two additional datasets are available: simulatneous scRNA ATAC seq was done on P1 wild type mouse cochlear cells and P8 wild type mouse cochlear cells.

Raw data is available at: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE182202

**P1-P8 scRNA seq**

- WT P1-P8 Tamoxofin: GSM5520356
- ATOH1 P1-P8 Tamoxofin: GSM5520357
- ATOH1+GFI1 P1-P8 Tamoxofin: GSM5520358
- ATOH1+GFI1+POUF4 P1-P8 Tamoxofin: GSM5520359


**P8-P15 scRNA seq**

- WT P8-P15 Tamoxofin: GSM5520360
- ATOH1 P8-P15 Tamoxofin: GSM5520361
- ATOH1+GFI1 P8-P15 Tamoxofin: GSM5520362
- ATOH1+GFI1+POUF4 P8-P15 Tamoxofin: GSM5520363

**P1 Multiome**

- P1 scRNA seq: GSM6883295
- P1 ATAC seq: GSM6883296

**P8 Multiome**

- P8 scRNA seq: GSM6883297
- P8 ATAC seq: GSM6883298


# FOLDER STRUCTURE
	
- **src/** : 	directory containing all scripts
- **data/** : 	directory containing data used in analysis
    - **raw/** : raw counts and ATAC data (not included in repo due to space constraints)
- **fig/** : 	directory containing outputs from src


# INSTALLATION

Analysis done on OSX 12.6

1. See requirements.txt for library requirements. 
    - run "pip install -r requirements.txt" to install all requirements

2. download data from https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE182202 and place into **data/raw/** directory (create if needed)
    - unzip GSM5520356_s9_rosa26WT_p8.tar.gz to get experiment directory
    - in experiment directory unzip *.tsv.gz and *.mtx.gz to get individual data files

3. Run UMAP.py to generate the figure for pset 4.


# CITATIONS

1. Amrita A Iyer, Ishwar Hosamani, John D Nguyen, Tiantian Cai, Sunita Singh, Melissa M McGovern, Lisa Beyer, Hongyuan Zhang, Hsin-I Jen, Rizwan Yousaf, Onur Birol, Jenny J Sun, Russell S Ray, Yehoash Raphael, Neil Segil, Andrew K Groves (2022) Cellular reprogramming with ATOH1, GFI1, and POU4F3 implicate epigenetic changes and cell-cell signaling as obstacles to hair cell regeneration in mature mammals eLife 11:e79712, https://doi.org/10.7554/eLife.79712