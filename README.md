## Naturalistic Emotion Processing Analysis

Authors: Jivesh Ramduny & Clare Kelly

### Overview

We leverage an emotional evocative movie to study the brain function at multiple spatial and temporal scales in addition to its phenotypic relevance with depressive symptom severity and emotion regulation strategies in a community-based sample of 50 female adolescents enriched for depressive symptoms. The aims of the study are three-fold:
1. investigate whole-brain full-length and moment-to-moment brain synchrony during naturalistic emotional viewing, and explore its relationships of each with self-reported depressive symptom severity and emotion regulation strategies;
2. examine static and dynamic functional connectivity within an a priori emotion regulation network;
3. characterise the underlying stimulus-evoked brain activity using the Hurst Exponent and to explore associations with the phenotypic measures at the network and ROI level.

### Movie-watching data

The structural and functional scans were acquired using a Philips Achieva 3T scanner from the Trinity College Institute of Neuroscience (TCIN) which is located at Trinity College Dublin. A T1-weighted MPRAGE volume with a spatial resolution of 0.9 x 0.9 x 0.9 mm3 (FOV = 230 mm, TR = 8.4 ms, TE = 3.8 ms, flip angle = 8°) was obtained for each participant. The participants underwent resting-state and movie-watching fMRI scans although the resting-state data were not used in the present study. The movie-watching fMRI data were acquired with 132 echo-planar imaging (EPI) volumes (37 slices, TR = 2000 ms, TE = 30 ms, voxel size = 3.2 x 3 x 3 mm3).

### MRI Preprocessing Pipeline

The structural and functional scans were preprocessed using the fMRIPrep version stable pipeline (https://fmriprep.org/en/stable/; Esteban et al., 2019) and in-house scripts using FSL (https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FSL) and AFNI (https://afni.nimh.nih.gov). The structural data underwent bias field correction, skull stripping, tissue segmentation (i.e., grey matter, white matter, cerebrospinal fluid) and spatial normalisation of the anatomical data to the MNI152 standard space using non-linear transformation. Preprocessing of the functional data comprised volume-based motion correction and functional to anatomical co-registration using boundary-based registration (Greve and Fischl, 2009). Confound regression was performed with 24 motion parameters (i.e., 3 translational and 3 rotational parameters, their first derivatives and the squares of each of these terms) and 12 nuisance signal regressors (i.e., cerebrospinal fluid, white matter, global signal, their squares and the squares of their first derivatives). Spatial smoothing was applied to the functional data with a Gaussian kernel at 6 mm FWHM followed by temporal filtering (0.01 ≤f≤  0.1 Hz). The fMRI timeseries which were extracted from the Shen parcellation are provided in the `movie` directory.

### Scripts

1. `movie_watching_analysis`: main notebook containing full-length ISC analysis, static analysis, hurst exponent analysis among others
2. `emotion_segment`: notebook containing the difference in ISC in the high-emotion segment relative to the low-emotion segment of the movie
3. `dynamic_isc_analysis`: notebook containing dynamic ISC analysis using a tapered cosine sliding window
4. `dynamic_FC_analysis`: notebook containing dynamic FC analysis using a tapered cosine sliding window
5. `hurst_exponent_FDR`: notebook containing the FDR thresholding of the hurst exponent for multiple comparison correction at the network and ROI level

### Citation

Ramduny, J., MacSweeney, M., Petkova, E., Kellaghan, E., Lahert, N., Gallagher, L. et al. Naturalistic emotional processing in adolescent females with depressive symptoms.

