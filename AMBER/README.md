# Shared EU Connectivity Models
This folder contains everything needed to run the six final invertebrate barrier models.


### Model scripts
The main model script is:
Scripts/run_one_A1_A2_A3_model.R

This script runs all six models.

The six SLURM scripts call this R script with the appropriate model name:
run_A1i_Richnesswithtype.slurm
run_A1ii_Richnesswithouttype.slurm
run_A2i_Shannonwithtype.slurm
run_A2ii_Shannonwithouttype.slurm
run_A3i_Propwithtype.slurm
run_A3ii_Propwithouttype.slurm



### Model datasets
These are ready to go:
A1i_Richnesswithtype_data.rds
A1ii_Richnesswithouttype_data.rds

A2i_Shannonwithtype_data.rds
A2ii_Shannonwithouttype_data.rds

A3i_Propwithtype_data.rds
A3ii_Propwithouttype_data.rds


## Model overview
The six models structures are:
| Model | Response | Barrier type |
|-------|----------|--------------|
| A1i | Total richness | Included |
| A1ii | Total richness | Not included |
| A2i | Shannon diversity | Included |
| A2ii | Shannon diversity | Not included |
| A3i | Proportion of non-native taxa | Included |
| A3ii | Proportion of non-native taxa | Not included |

The "with type" models include an interaction with reduced barrier type (other, dam, weir and culvert).

The "without type" models use total barrier density only.

## Data preparation

Here we...
- calculate richness, Shannon diversity and proportion of non-native taxa
- calculate barrier density
- calculate upstream, downstream and distance-to-mouth variables
- join climate and population density data
- standardise all continuous predictors (variables beginning with `z_`)
- create the final model-ready datasets

I haven't sent the raw data through for the prep code but I can if you would like it.

If anything is unclear just let me know!
