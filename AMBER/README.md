# SharedEUConnectivity

Essential files
---------------
1. Scripts/run_final_invert_barrier_models.R
2. Scripts/run_final_invert_barrier_models.slurm
3. Data/Processed/Final_Invert_Models/invert_richness_final_barrier_type_reduced.rds
4. Data/Processed/Final_Invert_Models/invert_prop_final_barrier_type_reduced.rds

Also useful
-----------
5. A short README explaining:
   - the ecological question;
   - what one row represents in each dataset;
   - how richness, non_native, and total_taxa were calculated;
   - how barrier density and distances were calculated;
   - that all variables beginning z_ were transformed and standardised;
   - the reference categories:
       community_group = native
       barrier_type_reduced = other
   - whether unknown-status taxa were excluded from total_taxa;
   - the R and brms versions used.

6. The script that created the two final RDS files, if the colleague
   needs to audit the complete data-processing workflow.

7. model_data_summary.txt and session_info.txt, after the model script
   has run.

Before submitting the SLURM job
-------------------------------
The Logs directory must already exist because SLURM opens its output
and error files before the job script begins:

mkdir -p Logs completed_models/final_invert_barrier_models

Then submit with:

sbatch Scripts/run_final_invert_barrier_models.slurm

Privacy and file size
---------------------
Check whether site_id or other fields contain sensitive or restricted
location information before sharing. The two prepared model datasets
are sufficient for rerunning these models; raw occurrence records and
spatial files are unnecessary unless the colleague is reviewing data
preparation as well.



