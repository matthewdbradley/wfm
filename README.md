# Introduction to Scientific Workflow Managers

This repository provides a starting point to using three popular scientific workflow managers - Nextflow, Cromwell, and Snakemake. 

## Getting Started

In order to use these workflow managers, first download Miniconda3. This can be done on the command line by doing the following. First, navigate to a directory in which you have at least a few GB of available space. Then, use the following commands.

```
wget https://repo.anaconda.com/miniconda/Miniconda3-py39_4.9.2-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh
```

Once Miniconda is installed, you can then download the required software. Clone the repository, and then run `install.sh` to install the pre-made conda environment.

```
git clone https://github.com/TheJacksonLaboratory/wfm.git
cd wfm
bash install.sh
```

This will create a conda environment named `wfm`, as well as download the Nextflow and Cromwell execution engines into their designated folders. Now you're ready to start using these examples! 

## Running the Examples

For reference, here are the commands that are used to run each of these examples. To run an example, you must first `cd` into the respective directory. Also, please ensure that you have activated the `wfm` conda environment by running `conda activate wfm`.

### Nextflow 
`nextflow pipeline.nf`

### Cromwell
`java -Dconfig.file=[parent-directory]/wfm/cromwell/my.conf -jar cromwell-54.jar run -i inputs.json pipeline.wdl`
OR
`bash start` *(Included for convenience)*

### Snakemake
`snakemake -j1 --profile ./slurm`
