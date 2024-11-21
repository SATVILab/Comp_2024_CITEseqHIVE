# README


The purpose of this compendium is to
`[briefly describe the compendium's goals and objectives]`

## Contact

For more information, please contact:
- `[Name]`, `[Email Address]`
- `[Name]`, `[Email Address]`

## Links

- `[URLs to data sources (e.g. OneDrive), GitHub repos, publications, etc.]`

## Details

### How to run within a container on the HPC

- Ensure that `"$HOME"/dotfiles/install-hpc.sh` has been run.
- Switch to the directory in the HPC in which you wish to keep all the repos associated with this project.
- Run `git clone https://github.com/SATVILab/Comp_2024_CITEseqHIVE`.
- Run `cd Comp_2024_CITEseqHIVE`
- Run `apptainer-pull`
- Run `apptainer-vscode`
- Within VS Code:
    - In a terminal where the working directory is `Comp_2024_CITEseqHIVE`, run `repos-git-clone`.
    - For each analysis/data processing repo (just not this infrastructure repo), e.g. `M72_CITEseqHIVE_scRNAseq_Pipeline`:
      - Switch to them as your working directory, e.g. `cd ../M72_CITEseqHIVE_scRNAseq_Pipeline`.
      - Run `config-r-renv-restore`.
    - In the repo in which you want to work, run `radian` to start `R` and then e.g. `quarto::quarto_render()` to build the `quarto` project.

### How to run within a container on GitHub Codespaces

- Ensure that the GitHub Codespace has access to the following environment variables:
  - `GH_TOKEN`: Classic PAT for GitHub
- Open GitHub Codespace
- In a terminal where the working directory is `Comp_2024_CITEseqHIVE`, run `repos-git-clone`.
- For each analysis/data processing repo (just not this infrastructure repo), e.g. `M72_CITEseqHIVE_scRNAseq_Pipeline`:
  - Switch to them as your working directory, e.g. `cd ../M72_CITEseqHIVE_scRNAseq_Pipeline`.
  - Run `config-r-renv-restore`.
- In the repo in which you want to work, run `radian` to start `R` and then e.g. `quarto::quarto_render()` to build the `quarto` project.
