# Background

The [Progresa](http://en.wikipedia.org/wiki/Oportunidades) program is a government social assistance program in Mexico. The goal of the program was to improve educational outcomes in poor households by providing subsidies if they send their children to school.

The timeline of the program was:
* Baseline survey conducted in 1997
* Intervention begins in 1998, "Wave 1" of surveys conducted in 1998
* "Wave 2" of surveys conducted in 1999
* Evaluation ends in 2000, at which point the control villages were treated.
 
Each row in the data corresponds to an observation taken for a given child for a given year. There are two years of data (1997 and 1998), and just under 40,000 children who are surveyed in each year. For each child-year observation, the following variables are collected:

| Variable name | Description|
|------|------|
|year	  |year in which data is collected
|sex	  |male = 1|
|indig	  |indigenous = 1|
|dist_sec |nearest distance to a secondary school|
|sc	      |enrolled in school in year of survey|
|grc      |grade enrolled|
|fam_n    |family size|
|min_dist |	min distance to an urban center|
|dist_cap |	min distance to the capital|
|poor     |	poor = 'pobre'|
|progresa |treatment = 'basal'|
|hohedu	  |years of schooling of head of household|
|hohwag	  |monthly wages of head of household|
|welfare_index|	welfare index used to classify poor|
|hohsex	|gender of head of household (male=1)|
|hohage	|age of head of household|
|age	|years old|
|folnum	|individual id|
|village|	village id|
|sc97	|schooling in 1997|
|grc97  |grade enrolled in 1997

# Problem Statement
The goal of this analysis is to evaluate the validity of the experimental design of the Progresa program and measure the program's impact on secondary school enrollment rates.

# Analysis
The full analysis can be found in the **progresa_analysis.ipynb** file.
