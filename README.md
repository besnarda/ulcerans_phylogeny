# ulcerans_phylogeny

First step is to install miniconda which will manage our environment.  

``` shell
wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh
```

We will create our working environement
for that we need a file that we call environment.yaml

``` shell
conda env create --name ulcerans_phylogenie --file environment.yaml
```

To activate the environment

``` shell
conda activate ulcerans_phylogenie
```

To remove environment

``` shell
conda deactivate
```

then we need a snakemake file, it is mandatory for snakemake and contain all steps in our process.
check everything is ok with a 'dry-run' with -n option

``` shell
snakemake -n --snakefile ulcerans_phylogeny.rules plots/phylogeny_tree.svg
snakemake --snakefile ulcerans_phylogeny.rules plots/phylogeny_tree.svg
``` 
