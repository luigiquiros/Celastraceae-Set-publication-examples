# The Celastraceae set

This repository gathers scripts used for the paper _"Liquid chromatography high-resolution mass spectrometry data for the study of the specialized metabolome of a set of plants from the Celastraceae family."_

#### -- Project Status: [Active]

## Intro 

The purpose of this publicatio is to describe the chromatographic and spectral data obtained from the profiling of a unique set of 76 plant exatracts from the Celastraceae Family.
Their exploration makes the object of the current Data Descriptor.

### Partners

#### Pierre-Fabre Laboratories

- https://www.pierre-fabre.com/en

#### Phytochemistry & Bioactive Natural Products 

- School of Pharmaceutical Sciences, University of Geneva, CMU, Rue Michel-Servet 1, CH-1211 Geneva 4, Switzerland
- https://ispso.unige.ch/phytochimie/index.php

### Methods Used
* High-Performance Liquid Chromatography
* High-Resolution Mass Spectrometry
* Computational Mass Spectrometry (molecular networking, metabolite annotation etc.)
* Data Visualization


### Technologies

* Python

## Project Abstract 
> 
> Natural products frequently exhibit interesting structural features and significant biological activities. The discovery of new bioactive molecules is frequently impeded by the chemical complexity of the biological matrices. Therefore, collections of natural extracts possess tremendous potential for chemical novelty, but exploiting them within drug-discovery initiatives can be challenging. This Data Descriptor discloses the public availability of a set of 76 natural extracts of the Celastraceae family profiled by untargeted liquid chromatography-mass spectrometry. The spectral annotation results and related chemical and taxonomic metadata are presented to the scientific community, along with proposed examples of data reuse. With the aid of newly developed repository-level data analysis pipelines, this data can be utilized as a reference dataset for untargeted metabolomic analysis of specialized plant metabolites based on MS/MS.
> 



## Data availability  

Raw Data are available in the the MassIVE repository [MSV000087970](https://doi.org/doi:10.25345/C5PJ9N).

## Getting Started

1. Clone this repo (for help see this [tutorial](https://help.github.com/articles/cloning-a-repository/)).

```
git clone https://github.com/mandelbrot-project/pf_1600_datanote.git
cd pf_1600_datanote
```

2. Install and activate the Conda environment from the environment.yml file. The [TMAP package](https://github.com/reymond-group/tmap) is only available on MacOS and Linux. If you are using Windows, you can use WSL.

```
conda env create --file environment.yml
conda activate pf_datanote
```

## Phylogenetic coverage calculation

Here are the instruction to calculate the phylogenetic coverage of the PF1600 dataset.
The resulting data is used to generate Figure 1. and the associated barplots

1. Set parameters in the [phylo_config.yaml](https://github.com/mandelbrot-project/pf_1600_datanote/blob/e23e573e011c498eeb9664337cd1e74229c133d5/config/phylo_config.yaml)

2. Run the [phylogenetic_coverage.R](https://github.com/mandelbrot-project/pf_1600_datanote/blob/e23e573e011c498eeb9664337cd1e74229c133d5/src/phylogenetic_coverage.R) script. Make sure to run it from the repository directory level.

```
Rscript src/phylogenetic_coverage.R
```

## Spectral TMAP establishment    
Here are the instruction to calculate the TMAP clustering of the features' MS/MS spectra of the PF1600 dataset.
The resulting data is used to generate Figure 2.
  
Run the [spectral_tmap.py](https://github.com/mandelbrot-project/pf_1600_datanote/blob/e23e573e011c498eeb9664337cd1e74229c133d5/src/spectral_tmap.py) script.
```
python src/spectral_tmap.py
```

## Structural TMAP establishment    
Here are the instruction to calculate the TMAP clustering of the annotated compounds from the PF1600 dataset.
The resulting data is used to generate Figure 3.
  
Run the [structural_tmap.py](https://github.com/mandelbrot-project/pf_1600_datanote/blob/e23e573e011c498eeb9664337cd1e74229c133d5/src/structural_tmap.py) script.
```
python src/structural_tmap.py
```


## Contributors

|Name     |  Twitter Handle   | 
|---------|-----------------|
|[Luis Quiros-Guerrero](https://github.com/luigiquiros)| @luisquirosg       |



