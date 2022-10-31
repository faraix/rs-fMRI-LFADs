# rs-fMRI-LFADs
## Unsupervised representation learning of cortical rsfMRI activity

Resting-state functional MRI (rsfMRI) is a technique used to study functional connectivity of the brain at rest. Functional connectivity refers to anatomically separate GM regions with temporal correlations in neuronal activity patterns. These GM regions form functional networks for individuals or populations in various behavioral or disease states.

Previous studies have implemented the VAE model to represent spatial patterns in rsfMRI data. However, the framework does not integrate the temporal dynamics inherent to rsfMRI data. We have designed a recurrent neural network to complement the VAE framework to further learn sequence representation. We investigate whether the latent space in rsfMRI data might provide new avenues to characterize individual variation and population characteristics of the brain underlying susceptibility to disease.

We hypothesize that the VAE can extract different latent distributions to reveal the distinctive network interactions underlying various states. We also believe the reconstruction of rsfMRI images offers a post-processing strategy for corrupted data recovery and motion correction.

Clone this repo and go INTO the rsFMRI_LFADs folder

Linux:

conda config --add channels conda-forge
conda env create -n DS_tutorial environment.yml

Windows:

conda config --add channels conda-forge
conda env create -f environment_windows.yml
conda activate DS_Tutorial
set CONDA_DLL_SEARCH_MODIFICATION_ENABLE=1 
pip install "jax[cpu]===0.3.14" -f https://whls.blob.core.windows.net/unstable/index.html --use-deprecated legacy-resolver
