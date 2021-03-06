# GP2-pathway-enrichment-pipeline
IPDGC x GP2 Hackathon 2021 Project - Pathway and cell type enrichment pipeline

## Project aim
Build a pipeline on Terra that uses public PD summary statistics to investigate biological pathway enrichment as well as cell type and tissue enrichment in GWAS loci.

## Contributors
Shameemah Abrahams, Inas Elsayed, Vassilene Iankova, Amica Muller, Zunej, Manuela Tan

## Steps

### 1. First import PD GWAS summary statistics into Terra workspace

Using import_GWAS_sumstats_Manuela.ipynb. Summary statistics (excluding 23andMe data) were downloaded from https://pdgenetics.org/resources and are publicly available.


### 2. Format for FUMA 

Using format_for_FUMA_Manuela.ipynb. This saves the GWAS summary statistics in FUMA format, then you can just upload this straight to FUMA. So far we can't find a way to link/embed FUMA within Terra.


### 3. Run WebGestaltR in Terra

Using run_WebGestaltR_Manuela.ipynb. For this we used the PD GWAS significant loci (p < 5 x 10<sup>-8</sup>) annotated with the nearest genes, available from https://www.nature.com/articles/ng.3043 (Supplementary Table 2).


## Notes

We used some of the really helpful setup code at https://app.terra.bio/#workspaces/fc-amp-pd-alpha/AMP%20PD%20-%20Workshop%20-%2020190508
