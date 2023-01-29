# Code for the manuscript "Accounting for outcome misclassification in complex sample designs: estimation of SARS-CoV-2 seroprevalence in central North Carolina"


This SAS file provides code to calculate corrected seroprevalence estimates with corresponding 95% bootstrap confidence intervals.


## Construction of example dataset
The randomly generated data used in this code is designed to illustrate the necessary data structure and variables required to use this method. Note that we demonstrate this method using a hypothetical three-stage sample, but this method can be applied to a different number of stages.

Variable descriptions:
- **participant_id** ID number for each individual study participant
- **sex** sex of participant (In example, =1 if male, =0 if female)
- **age** age in years of participant
- **age_cat** age category of participant (In example, =1 if age between 18 and 49 , =2 if age 50+)
- **serostatus** indicates binary serological test result of participant (In example, =1 if positive for SARS-CoV-2 antibodies, =0 otherwise)
- **BASEWT** base weight (how to describe?))
- **STRATUM** stratum number (In example, =1,2, or 3)
- **CLUSTER_NUM** cluster number (In example, =1,2,3,4,5,6,7,8, or 9)
- **PSU_WT** weight for each PSU (In C4/example, census blocks served as PSUs)
- **HH_WT** weight for each SSU (In C4/example, households served as SSUs)
- **PER_WT** weight for each individual person, the reciprocal of the probability of selection with each household


## Weight calibration
We use PROC WTADJUST procedure from SUDAAN v 11.0.3 for calibration of sample weights. 
Alternatives include:
- A SAS Macro (An, 2020): https://www.sas.com/content/dam/SAS/support/en/sas-global-forum-proceedings/2020/4284-2020.pdf
- The calibrate() function in the R package 'survey' (Lumley, 2022): http://cran.fhcrc.org/web/packages/survey/index.html


## Citation
If using this code, please cite as:
(tbd)
