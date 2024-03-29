<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/github_username/repo_name">
    <img src="images/GP2_logo.png" alt="Logo" width="300" height="70">
  </a>

<h3 align="center">Pathway and cell type enrichment pipeline</h3>

  <p align="center">
    One of the projects from the 2021 GP2/IPDGC Hackathon. The related manuscript can be found on [biorxiv](https://www.biorxiv.org/content/10.1101/2022.05.04.490670v1) 
    <br />
    Contributers: Shameemah Abrahams, Inas Elsayed, Vassilene Iankova, Amica Muller, Zunej, Manuela Tan
    <br />
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#quick-description">Quick Description</a></li>
        <li><a href="#background/motivation">Background/motivation</a></li>
        <li><a href="#workflow-summary">Workflow Summary</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

![Project Screen Shot][project-screenshot]

### Quick Description

The goal for this project was to build a pipeline on Terra that uses public PD summary statistics to investigate biological pathway enrichment as well as cell type and tissue enrichment in GWAS loci.

### Background/motivation

Investigating GWAS loci enrichment in pathways, cell types, and tissues is an important part of linking genetic risk to biological mechanisms. Peparing GWAS summary statistics and performing enrichment analyses can be time-consuming. This workflow serves as an example for how to use and format summary statistics for popular software FUMA and WebGestaltR.     

### Workflow Summary

1. Setting up and importing summary statistics
2. Formatting summary statistics for FUMA
3. Using WebGestaltR

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->
## Getting Started

### Prerequisites

* [WebGestaltR](https://cran.r-project.org/web/packages/WebGestaltR/index.html) 

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/ipdgc/GP2-pathway-enrichment-pipeline.git
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## Usage

These notebooks can be directly uploaded to your workspace on Terra. They are designed to be used on Terra with AMP-PD data, but by changing the file paths you can use these notebooks anywhere other than Terra and for any data.


### 1. First import PD GWAS summary statistics into Terra workspace

Using import_GWAS_sumstats_Manuela.ipynb. Summary statistics (excluding 23andMe data) were downloaded from https://pdgenetics.org/resources and are publicly available.


### 2. Format for FUMA 

Using format_for_FUMA_Manuela.ipynb. This saves the GWAS summary statistics in FUMA format, then you can just upload this straight to FUMA. So far we can't find a way to link/embed FUMA within Terra.

### 3. Run WebGestaltR in Terra

Using run_WebGestaltR_Manuela.ipynb. For this we used the PD GWAS significant loci (p < 5 x 10<sup>-8</sup>) annotated with the nearest genes, available from https://www.nature.com/articles/ng.3043 (Supplementary Table 2).

_For more examples, please refer to FUMA [documentation](https://fuma.ctglab.nl/tutorial) and WebGestaltR [documentation](https://cran.r-project.org/web/packages/WebGestaltR/index.html)_

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* We used some of AMP-PD's really helpful [setup code](https://app.terra.bio/#workspaces/fc-amp-pd-alpha/AMP%20PD%20-%20Workshop%20-%2020190508)

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[project-screenshot]: images/project_screenshot.png

