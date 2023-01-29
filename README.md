# Sample code for the manuscript "Accounting for outcome misclassification in complex sample designs: estimation of SARS-CoV-2 seroprevalence in central North Carolina"


This SAS file provides sample code to calculate corrected seroprevalence estimates with corresponding 95% bootstrap confidence intervals.


## Construction of example dataset
The randomly generated data used in this code is designed to illustrate the necessary data structure and variables required to use this method.

Variable descriptions:
- **participant_id** corresponds to id number for each individual study participant
- **sex** sex of participant (=1 if male, =0 if female)
- **age** age in years of participant
- **serostatus** indicates binary serological test result of participant (=1 if positive for SARS-CoV-2 antibodies, =0 otherwise)
- **BASEWT** 
- **STRATUM**
- **CLUSTER_NUM**
- **PSU_WT**
- **PER_WT** indicates the weight for each individual person, the reciprocal of the probability of selection with each household
- **HH_WT**

## Weight calibration
We use PROC WTADJUST procedure from SUDAAN v 11.0.3 for calibration of sample weights. 
Alternatives include:
- A SAS Macro (An, 2020): https://www.sas.com/content/dam/SAS/support/en/sas-global-forum-proceedings/2020/4284-2020.pdf
- The calibrate() function in the R package 'survey' (Lumley, 2022): http://cran.fhcrc.org/web/packages/survey/index.html


## Citation
If using this code, please cite as:
(tbd)
