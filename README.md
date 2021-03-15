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
The full analysis can be found in the [**Progresa Analysis.ipynb**] (https://github.com/colleensun/progresa_analysis/blob/main/Progresa%20Analysis.ipynb) file.

# Methodology
Some analyses that were performed include:

* Summary statistics to get a sense of the distribution of data
* Checking for missing values, encoded variables as dummy variables to use for further analysis
* T-test to check whether the difference between treatment and control groups is significant at the baseline (before treatment is rolled out)
* Visualized outcome distributions of treatment/control groups before/after treatment using histograms
* Performed impact evaluation by examining the simple-difference and difference-in-difference estimates of impact, this was done through linear regression models
* Checked for spillover effects

# Findings
* There exists some differences between treatment and control villages at baseline, which could suggest that the randomization was not done properly. This is important because having many significant differences between the control and treatment groups suggests that the groups differ systematically, and any subsequent differences in outcomes between the groups cannot be attributed to the treatment, since they could intead be due to pre-existing systematic differences.
* There was no evidence of spillover effects. That is, none of the treatment effects got spilled over to the control group, which is what we want to see.
* I conclude that Progresa had a causal impact on the enrollment rates of poor households in Mexico because:
  * Targeting was performed on two levels during the experiment design (village- and household-level)
  * Both the simple difference and difference-in-difference evaluation tell us that the treatment outcome is statistically significant
