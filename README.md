# Coping Strategies and Stress Recovery
This repository contains the scripts necessary to preprocess, analyze, print and plot the result to answer the following research question: 

**How do children's coping strategies impact their stress recovery?**

## Background
Stress is a condition of the mind-body interaction [(McEwen, 2006)](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3181832/). The body responds to almost any event or challenge by releasing chemical mediators -e.g., catecholamines that increase heart rate and blood pressure -that help us cope with the situation. However, prolonged stress leads to latent vulnerabilities. At the theoretical level, most prevailing models of developmental psychopathology recognize the potential importance of psychosocial stress in the aetiology and maintenance of both internalizing and externalizing disorders in youth [(McMahon et al., 2003)](https://cdn.vanderbilt.edu/vu-my/wp-content/uploads/sites/2804/2019/04/14195723/McMahon-et-al-2003-J-of-Child-Psychology-and-Psychiatry.pdf).

Therefore, this study aimed to study the impact of children's coping strategies on their stress recovery, represented by `Blood Pressure`. 

## Dataset
Data used in this study is a subset of the CEDS data, which can be found on [UK Data Service ](https://reshare.ukdataservice.ac.uk/851918/). The sample included 400 children (49% female, 51% male) who participated in the Children's Experiences and Development Study (CEDS), conducted from 2009 through 2011 in England. CEDS children were born between 1999 and 2001 and were initially assessed as part of a separate study of over 6,000 families when they were three years old. 

More details of the CEDS sampling frame can be found in the original paper: 
> Jaffee, Sara and Melhuish, Edward and Belsky, Jay (2015). Children's experiences and development study. [Data Collection]. Colchester, Essex: UK Data Archive. 10.5255/UKDA-SN-851918

After downloading and unzipping the dataset from the above repository, locate the file named `Archived_CEDS_Documentation` in the `Data` folder, where you can find the original dataset. 

## Measurement 
The study focused on `Blood Pressure` and `Coping Strategies`. 

**Blood pressure** was measured five times throughout the original study, as shown in the Figure below. Our study focused on stress recovery; therefore, only `BP3Time`, `BP4Time`, and `BP5Time` were considered as predictors. 

<img width="305" alt="image" src="https://github.com/larsond513/CEDS/assets/120323717/198950e4-ad5d-4fc7-ba5e-63972d9a3969">


**Coping Strategies** were measured using the [Manual for the Children's Coping Strategies Checklist & How I coped Under Pressure Scale](https://www.yumpu.com/en/document/read/12240213/manual-for-the-childrens-coping-strategies-checklist). The scoring sheet can also be found in the manual, shown in the figure below.

<img width="543" alt="image" src="https://github.com/larsond513/CEDS/assets/120323717/561b161b-3ef8-431c-a890-3a9b9e62a56b">


## Usage
The script described below is named `LDA.md`. Processed data files will be saved to the `Data/OutFiles` folder. Figures will be saved in the `Figure` folder. We have broken down processing into 3 stages, outlined below.

### Preprocessing 
<details>

<summary>Data Naming Conventions</summary>

|Coping Strategies | Variable Given Name|
| ------------- | ------------- |
| Active Coping Strategies  | act1-12  |
| Avoidant Strategies  | av1-6  |
| Support Seeking Coping Strategies | supp1-4 |
| Distraction Strategies  | distr1-4 |

|Name in `Archived_CEDS_Documentation.csv`  | Name in our script |
| ------------- | ------------- |
| Saliva1Time  | starting_cortisol  |
| Saliva2Time  | t2  |
| Saliva3Time | t3 |
| Saliva4Time  | t4 |
| Saliva5Time | t5  |
| Saliva6Time  | t6 |
| BP1Time  | starting_BP |
| CCSC01|act1-12  |
| CCSC02  | av1 |
| CCSC03  | act2  |
| CCSC04  | act3 |
|CCSC05|av2|
|CCSC06|supp1|
|CCSC07|av3|
|CCSC08|act4|
|CCSC09|av4|
|CCSC10|supp2|
|CCSC11|act5|
|CCSC12|distr1|
|CCSC13|supp3|
|CCSC14|act6|
|CCSC15|distr2|
|CCSC16|act7|
|CCSC17|act8|
|CCSC18|supp4|
|CCSC19|av5|
|CCSC20|distr3|
|CCSC21|act9|
|CCSC22|act10|
|CCSC23|act11|
|CCSC24|av6|
|CCSC25|distr4|
|CCSC26|act12|

</details>

### Model Assumption Testing 

### Model fitting 



