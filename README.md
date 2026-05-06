# The Wage and Mobility Effects of Non-Compete Bans: Evidence from Minnesota
## Replication Package
Final Project for Econ 580 (Nathan Sever, Spring 2026)
Paper: The Wage and Mobility Effects of Non-Compete Bans: Evidence from Minnesota

To replicate the paper's results, see the following:

First, download the ZIP file (folder) "replication_package." This contains all the data and code necessary to reproduce the results.
**Note that "replication_package" is too large to upload to GitHub (>25 MB). This is because I provide some of the data ("synth_final.csv") instead of requiring users to run all API queries, which could take several hours.
Instead, I have shared the replication package with Prof. Alder and Prof. Braxton in a shared Google Drive.**

Important files in the "replication_package" folder:
* "QWI_wisc_control.ipynb" gathers the requisite QWI data to perform the difference-in-difference analysis using the Wisconsin control group.
* "synthetic_control.ipynb" gathers the requisite QWI/BEA/BLS data to construct the synthetic control and run the corresponding regressions.
* "mn_nca_figures.ipynb" re-creates all Figures (1-8) in the final project paper.
* summary.do (Stata) performs all the regressions outlined in the paper once the requisite data is obtained.

## Replication Steps
To replicate the results, I recommend first running QWI_wisc_control.ipynb and synthetic_control.ipynb. 
Note that both of these programs require extensive API querying. Many queries can take 2-4 hours individually. 
To save time, I also include the QWI data in the "Data" folder:
* Data/wi_control --> contains overall regression data for Wisconsin control, along with heterogeneity analysis data.
* Data/synthetic_control --> "synth_final.csv" contains the final synthetic control data used in my regressions.

Once the requisite data has been collected, navigate to "summary.do" in the "replication_package" folder.
All regression results can be re-created in one command using "summary.do." However, I recommend running each command separately to ease the re-creation of figures.
* "wi_control.do" recreates the overall and heterogeneity regressions with the Wisconsin control.
* "synthetic_control.do" recreates the synthetic control construction and regression.
* The rest of the do-files recreate synthetic control robustness checks outlined in section 6 of the paper (donor pool restriction, alternative predictor selection, residualization).

Finally, run "mn_nca_figures.ipynb" to re-create all figures in the paper. 
Note that all of the synthetic control specifications will overwrite each other, so Tables 6-7 depend on the last do-file executed in Stata. 
To re-create Tables 6-7 exactly as in my paper, run "synthetic_control.do" again before creating the figures in Python.

Please contact me with any questions or difficulties in re-creating my results at nsever@wisc.edu.
