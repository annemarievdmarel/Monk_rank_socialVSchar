# perturbation-MOPA-IDranks
Data from: Perturbations highlight importance of social history in parakeet rank dynamics.
Published in Behavioral Ecology [add citation]

DESCRIPTION
Dominance rank systems can be conceptualized as a continuum from rank purely as an outcome of the individual’s phenotype to rank purely as an outcome of that individual’s social history in a group. Understanding where species fall on this rank continuum provides insight into the relative weight of individual characteristics versus social factors in determining an individual’s social standing in the group. Researchers often use simple correlations to study whether individual characteristics underly rank. When a weak or no correlation is found, this may not immediately mean that social factors are determining rank, because a cryptic individual characteristic not observed or measured by the human observer may still influence rank. Ideally, we need additional experimental manipulation of the social group (changes in group membership) to distinguish between rank systems. 

We used social manipulations in a captive group of monk parakeets, where we removed and reintroduced differently-ranked birds. Using this experimental approach, we tested whether rank was more based on individual characteristics or more on social processes. We found that body mass was not correlated with rank and that the none of the focal birds could re-take their previous position in the group upon reintroduction. Using an experimental approach, we found that history of past interactions may be used over intrinsic characteristics to infer the rank of others in this group of monk parakeets. 

METADATA
The code provided in the Rmarkdown script titled "Stats_perturbations_individual ranks.Rmd" provides all the code and the description of the code to reproduce our findings. 

The data folder contains the data. 
MOPA_power_score_2021 * 2022 .csv contains the dominance rank information for all birds
 - key	= orderkey
 - bin	= number of 3-day observation period. starts with 0
 - id	  = unique color code combination to identify each bird
 - dom_ec	= eigenvector centrality
 - rank	= ordinal rank measure 
 - power = dominance rank score (closer to 1 -> higher-ranked)
 - group = only for data in 2022 as we had 2 groups


experimental_birds.csv contains the individual information for each monk parakeet used in the experiment. 
  - bandID = unique band number 
  - sex = male or female
  - year = year of experiment
  - site_captured	= birds were trpaped in 4 different feral populations 
  - group_21 = 2021 -> bird was used in the 2021 experimental group
  - mark_21 = unique color code combination (B = blue/ G = Green / P = Purple / O = Orange) for the bird in 2021
  - group_22 = bird was either placed in group 1_west or 2_east. 
  - mark_22 = unique color code combination (B = blue/ G = Green / P = Purple / O = Orange) for the bird in 2022
  

2021_3daybins.csv and 2022_timeline.csv contains the dates and the rank assessment periods for each experimental year

2021_3daybins.csv:
  - date = year-month-day
  - perturbation = explains at what part of the experiment we are on
  - type = the perturbation type (removal or reintroduction)
  - bin_all = unique number for the 3-days to obtain rank for the whole field season
  - n_birds = total number of birds in the group
  - capture = the number of the capture event
  - capture_date = date of capture
  - rank_assessment_2021 = the 3-days bins used for rank assessment in the paper
  - bin = unique number for the 3-days observation period to obtain rank for social manipulation experiment
  
2022_3daybins.csv:
 - date	= year-month-day
 - capture	= the number of the capture event
 - total_obs_day	= total number of observation days
 - perturbation	= experiment trial
 - experiment	= the perturbation type (removal or reintroduction)
 - focal_bird	= which ranked bird to perturb
 - dompattern_focal	= rank assessment periods for each focal rank
 - bin = unique number for the 3-days observation period to obtain rank for social manipulation experiment
 
captures_bins.csv contains the info for the bins before and after each perturbation event used for body mass analysis.
 - year	= year of experiment
 - date	= year-month-day
 - trial	= number of experimental trial
 - type	= perturnation type (removal or reintroduction)
 - focalrank	= rank of the focal bird that was removed
 - capture	= number of capture event
 - capture_date	= date of capture event
 - bin_prior	= 3-day observation period before the perturbation
 - bin_post = 3-day observation period after perturbation


morphometrics_focals_2021.csv and 2022_MOPA_capture_file.csv contains the body weight obtained during the capture events
morphometrics_focals_2021.csv:
  - date = year-month-day captured
  - time = time that bird was captured
  - cage_num	= holding cage ID before birds were placed into the flight pen
  - band_id = unique band number 
  - sex = male or female
  - id =  unique color code combination (B = blue/ G = Green / P = Purple / O = Orange)
  - weight1	= body mass in g of both bird + bird bag + box
  - weight2	= mass of bird bag + box in g
  - weight = body weight in g of bird
  - perturbation = cpature event and perturbation trial

2022_MOPA_capture_file.csv:
 - date	= year-month-day captured
 - time	= time that bird was captured
 - cage_num =  holding cage ID before birds were placed into the flight pen
 - band_id	= unique band number 
 - mark_id	= unique color code combination
 - weight1 = body mass in g of both bird + bird bag + box
 - weight2 = mass of bird bag + box in g
 - weight = body weight of bird in g 
 - wing_cord = measurement of wing length in mm
 - tail_length = measurement of tail lenght in mm
 - culmen_width	= width of culmen (mm)
 - culmen_length	= length of culmen (mm)
 - measurement_taker	= initials of observer who took measurements
 - body_condition	= body condition on a scale of 1-5, 5 is a lot of fat, don't feel sternum. 
 - notes
 
SESSIONINFO R 
R version 4.2.2 (2022-10-31 ucrt)
Platform: x86_64-w64-mingw32/x64 (64-bit)
Running under: Windows 10 x64 (build 22621)

Matrix products: default

locale:
[1] LC_COLLATE=English_Canada.utf8 
[2] LC_CTYPE=English_Canada.utf8   
[3] LC_MONETARY=English_Canada.utf8
[4] LC_NUMERIC=C                   
[5] LC_TIME=English_Canada.utf8    

attached base packages:
[1] stats     graphics  grDevices utils     datasets 
[6] methods   base     

other attached packages:
[1] forcats_0.5.2   stringr_1.5.0   dplyr_1.0.10   
[4] purrr_0.3.5     readr_2.1.3     tidyr_1.2.1    
[7] tibble_3.1.8    ggplot2_3.4.1   tidyverse_1.3.2

loaded via a namespace (and not attached):
 [1] nlme_3.1-160         fs_1.5.2            
 [3] lubridate_1.9.0      RColorBrewer_1.1-3  
 [5] httr_1.4.4           numDeriv_2016.8-1.1 
 [7] tools_4.2.2          TMB_1.9.1           
 [9] backports_1.4.1      utf8_1.2.2          
[11] R6_2.5.1             DBI_1.1.3           
[13] colorspace_2.0-3     ggdist_3.2.0        
[15] withr_2.5.0          tidyselect_1.2.0    
[17] emmeans_1.8.3        compiler_4.2.2      
[19] rvest_1.0.3          cli_3.4.1           
[21] xml2_1.3.3           sandwich_3.0-2      
[23] scales_1.2.1         mvtnorm_1.1-3       
[25] gamlss_5.4-10        ggbump_0.1.0        
[27] digest_0.6.31        minqa_1.2.5         
[29] rmarkdown_2.18       DHARMa_0.4.6        
[31] pkgconfig_2.0.3      htmltools_0.5.4     
[33] lme4_1.1-31          dbplyr_2.2.1        
[35] fastmap_1.1.0        readxl_1.4.1        
[37] rlang_1.0.6          rstudioapi_0.14     
[39] farver_2.1.1         generics_0.1.3      
[41] gamlss.data_6.0-2    zoo_1.8-11          
[43] jsonlite_1.8.4       car_3.1-1           
[45] googlesheets4_1.0.1  distributional_0.3.1
[47] magrittr_2.0.3       Matrix_1.5-1        
[49] Rcpp_1.0.9           munsell_0.5.0       
[51] fansi_1.0.3          abind_1.4-5         
[53] lifecycle_1.0.3      stringi_1.7.8       
[55] multcomp_1.4-20      yaml_2.3.6          
[57] carData_3.0-5        MASS_7.3-58.1       
[59] gamlss.dist_6.0-5    grid_4.2.2          
[61] parallel_4.2.2       crayon_1.5.2        
[63] lattice_0.20-45      haven_2.5.1         
[65] cowplot_1.1.1        splines_4.2.2       
[67] hms_1.1.2            knitr_1.41          
[69] pillar_1.8.1         ggpubr_0.5.0        
[71] boot_1.3-28          estimability_1.4.1  
[73] ggsignif_0.6.4       codetools_0.2-18    
[75] reprex_2.0.2         glue_1.6.2          
[77] evaluate_0.19        effsize_0.8.1       
[79] modelr_0.1.10        vctrs_0.5.1         
[81] nloptr_2.0.3         tzdb_0.3.0          
[83] cellranger_1.1.0     gtable_0.3.1        
[85] assertthat_0.2.1     xfun_0.35           
[87] xtable_1.8-4         broom_1.0.1         
[89] coda_0.19-4          rstatix_0.7.1       
[91] survival_3.4-0       googledrive_2.0.0   
[93] gargle_1.2.1         glmmTMB_1.1.5       
[95] timechange_0.1.1     fitdistrplus_1.1-8  
[97] TH.data_1.1-1        ellipsis_0.3.2 


LICENSE
CC0

CITATION
DOI: 10.5281/zenodo.6418416
https://zenodo.org/badge/DOI/10.5281/zenodo.6418416.svg

