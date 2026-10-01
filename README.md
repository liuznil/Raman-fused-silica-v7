# Raman-fused-silica
This repository contains the code and documentation associated with the data processing methods, figure generation, and table creation for the accompanying manuscript - Raman band-envelope analysis of indentation-induced spectral evolution in fused silica.

# Directory Structure

├── figures/ (300 dpi; numbered sequentially according to their appearance in the manuscript) <br>
│   ├── fig1_skewness_vs_load.png            Fig.1 [Sec. 3.1]<br>
│   ├── fig2_fwhm_hysteresis.png             Fig.2 [Sec. 3.1]<br>
│   ├── fig3_D2main_ratio.png                Fig.3 [Sec. 3.1]<br>
│   ├── fig4_position_vs_skewness.png        Fig.4 [Sec. 3.1]<br>
│   ├── fig5_spectrum_decomposition.png      Fig.5 [Sec. 3.2] Representative spectral decomposition<br>
│   ├── fig6_d1_d2_only_residual.png         Fig.6 [Sec. 3.2]<br>
│   ├── fig7_fit_quality_waterfall.png       Fig.7 [Sec. 3.2] Waterfall plot of fitting quality across the full sequence<br>
│   ├── fig8_pristine_vs_residual.png        Fig.8 [Sec. 3.4]<br>
│   └── fig9_pca_scores.png                  Fig.9 [Sec. 3.5]<br>
│<br>
├── outputs/<br>
│   ├── TO_sequence_fit_quality.csv          Fitting results for 14 TO spectra<br>
│   ├── peak_shape_results.csv               28 spectral records × all peak shape / load / depth parameters<br>
│   ├── summary_stats.csv                    Summary statistics by configuration (TO/CO × load/unload)<br>
│   ├── correlation_stats.csv                Pearson correlation coefficients and p-values (load vs. peak shape parameters)<br>
│   ├── pca_loadings.csv                     PCA loading matrix (weights of 11 features on PC1/PC2)<br>
│   └── pca_scores.csv                       PCA scores + original features<br>
│<br>
└── src/<br>
    ├── peak_analysis.py   Core module: data I/O, ALS baseline correction, moment analysis, and triple-peak fitting<br>
    ├── run_analysis.py    Batch processing of TO/CO load/unload sequences; generates result tables and summary statistics<br>
    └── make_plots.py      Generates all figures, PCA visualizations, and correlation statistical tests<br>
