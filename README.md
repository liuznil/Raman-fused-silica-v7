# Raman-fused-silica
This repository contains the code and documentation associated with the data processing methods, figure generation, and table creation for the accompanying manuscript - Raman band-envelope analysis of indentation-induced spectral evolution in fused silica.

# Directory Structure

├── figures/ (300 dpi; numbered sequentially according to their appearance in the manuscript)
│   ├── fig1_skewness_vs_load.png            Fig.1 [Sec. 3.1]
│   ├── fig2_fwhm_hysteresis.png             Fig.2 [Sec. 3.1]
│   ├── fig3_D2main_ratio.png                Fig.3 [Sec. 3.1]
│   ├── fig4_position_vs_skewness.png        Fig.4 [Sec. 3.1]
│   ├── fig5_spectrum_decomposition.png      Fig.5 [Sec. 3.2] Representative spectral decomposition
│   ├── fig6_d1_d2_only_residual.png         Fig.6 [Sec. 3.2]
│   ├── fig7_fit_quality_waterfall.png       Fig.7 [Sec. 3.2] Waterfall plot of fitting quality across the full sequence
│   ├── fig8_pristine_vs_residual.png        Fig.8 [Sec. 3.4]
│   └── fig9_pca_scores.png                  Fig.9 [Sec. 3.5]
│
├── outputs/
│   ├── TO_sequence_fit_quality.csv          Fitting results for 14 TO spectra
│   ├── peak_shape_results.csv               28 spectral records × all peak shape / load / depth parameters
│   ├── summary_stats.csv                    Summary statistics by configuration (TO/CO × load/unload)
│   ├── correlation_stats.csv                Pearson correlation coefficients and p-values (load vs. peak shape parameters)
│   ├── pca_loadings.csv                     PCA loading matrix (weights of 11 features on PC1/PC2)
│   └── pca_scores.csv                       PCA scores + original features
│
└── src/
    ├── peak_analysis.py   Core module: data I/O, ALS baseline correction, moment analysis, and triple-peak fitting
    ├── run_analysis.py    Batch processing of TO/CO load/unload sequences; generates result tables and summary statistics
    └── make_plots.py      Generates all figures, PCA visualizations, and correlation statistical tests
