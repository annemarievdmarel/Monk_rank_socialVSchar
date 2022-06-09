# perturbation-MOPA-IDranks

Code for manuscript entitled "Social manipulations disentangle rank effects of individual characteristics and social history"

DESCRIPTION
Dominance rank systems can be conceptualized as a continuum from rank purely as an outcome of the individual’s phenotype to rank purely as an outcome of that individual’s social history in a group. Understanding where species fall on this rank continuum provides insight into the relative weight of individual characteristics versus social factors in determining an individual’s social standing in the group. Researchers often use simple correlations to study whether individual characteristics underly rank. When a weak or no correlation is found, this may not immediately mean that social factors are determining rank, because a cryptic individual characteristic not observed or measured by the human observer may still influence rank. Ideally, we need additional experimental manipulation of the social group (changes in group membership) to distinguish between rank systems. 

We used social manipulations in a captive group of monk parakeets, where we removed and reintroduced the top-ranked bird. Using this experimental approach, we tested whether rank was more based on individual characteristics or more on social processes. We found that body mass was not correlated with rank and that the previously top-ranked bird could not re-take its previous position in the group upon reintroduction. Using an experimental approach, we found that history of past interactions may be used over intrinsic characteristics to infer the rank of others in this group of monk parakeets. 

METADATA
The code provided in the Rmarkdown script titled "Stats_perturbations_individual ranks_2021.Rmd" provides all the code and the description of the code to reproduce our findings. 

The data folder contains the data. 
2021_MOPA_agonistic interactions.csv contains the raw agonistic interaction data. 
  - sessionKEY = date and observer, 
  - session_start_timeStamp = date and time observation session started	
  - date = date of when interaction took place, 
  - time = time that interaction took place
  - actor = aggressor	
  - subject = receiver of aggression 	
  - behavior = interaction type (either crowds or displace)	
  - type = experimental period
  - bin = interaction data is compiled into 3-day bins during the experiment

2021_MOPA_IDs.csv contains the individual information for each monk parakeet used in the experiment. 
  - band_id = unique band number 
  - sex = male of female
  - year_captured	= the year the birds were captured from Southern Florida
  - site_captured	= birds were trpaped in 4 different feral populations 
  - mark_id = unique color code combination (B = blue/ G = Green / P = Purple / O = Orange)

2021_3daybins.csv contains the dates and the rank assessment periods
  - date = year-month-day
  - perturbation = explains at what part of the experiment we are on
  - type = the perturbation type (removal or reintroductio)
  - bin = unique number for the 3-days to obtain rank
  - n_birds = total number of birds in the group
  - capture = the number of the capture event
  - capture_date = date of capture
  - rank_assessment = the 3-days bins used for rank assessment in the paper

morphometrics_focals_2021.csv contains the body weight obtained during the capture events
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
 

LICENSE
CC BY-NC 4.0

CITATION
DOI: 10.5281/zenodo.6418416
https://zenodo.org/badge/DOI/10.5281/zenodo.6418416.svg

