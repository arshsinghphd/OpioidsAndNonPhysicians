PROJECT TITLE: 
Opioids And Non-Physician Prescriptive Powers

<details>
<summary>ABOUT ME</summary>
I am Arsh Singh, my PhD is in Applied Microeconomonics, and I am interested in applied data science. 
</details>

GOAL:
In this project I am testing my hypothesis that laws allowing non-physicians like Physician's Assistant and Nurse Practitioners may have contributed to the opioid crisis. This refers to three kinds of increased freedoms fro non-physicians:  Phycisian's Assistant (PA) can prescribe Sch II drugs, Nurse Practitioners (NP) can Prescribe Sch II drugs such as opioids, and NP no longer need physician's (MD) oversight for prescriptions. 

<details>
  <summary>DATA</summary>
  <details> 
  <summary>SOURCE</summary>
    I am using ARCOS dataset cleaned and made avaliable by WaPo. The dataset spans 2006-2012 and follows every pill prescribed. <a href="https://wpinvestigative.github.io/arcos/#download-the-raw-data">WaPo ARCOS Raw Data</a>.<br>
    For state populations I use data from UC Census. <a href="https://www2.census.gov/programs-surveys/popest/datasets/2000-2010/intercensal/county/co-est00int-tot.csv">2000-2010</a>, <a href="https://www2.census.gov/programs-surveys/popest/datasets/2010-2020/state/totals/nst-est2020.csv">2010-2020.</a><br>
    Various law passage data are taken from <a href=https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4730953/>Gadbois et al. (2015)</a> Accessed on 12-24-2022. 
  </details>
  
  <details> 
  <summary>VARIABLES</summary>
  DRUG AMOUNTS: <br> 
  In the analysis presented here I use Opioid drug amounts sold calculated as Dosage (Units) * Dosage (Strength) for each transaction, summed at the state-month level. I also standardize this by the population of the state to account for the size of the state. <br>
  TIME: <br>
  Time in this analysis is is months passes since the law passage. This is different for the three diffrent laws under consideration law and the states. This is the strength of regressional discontinuity, it lines up time in different states around laws than linear time, making it possible to see how these laws effects the opoid prescription overall. This apporach as takes care of country-wide effects associated with particular years.
  LAW: <br>
  There are 3 kind of laws analysed here: <br>
  NP = law that permits NPs to prescribe opioids <br>
  PA = law that permits PAs to prescribe opioids <br>
  NP_NO_MD = law that permits NPs to prescribe without MD oversight <br>
  I use a binary variable = 0 if the law doesn't permit non-physician to prescribe opioids, becomes 1 after the law is passed in the state. 
  </details>
  
</details>

<details>
  <summary>Statistical Techniques/Skills</summary>
  I am going to infer regression discontinuity (RD) using panel regressions.
  I show visuals that confirm RD and show panel regressions with robust covariance and fixed effects that confirms a regression discontinuity.
</details>

<details>
  <summary>Main Results</summary>
  For the states and the time period I analyse, passage of these laws explain 98+% of variation in the data. <br>
  When I analyse for the laws individually, each laws seem to have very similar effects on the way the opioids are prescribed. As soon as the law is passed the prescription reduces, but comes back to the previous levels at a very fast rate and marginally increases this rate.  <br>
  When I analyse all the laws together, allowing NPs to prescribe seems to have the largest impact.
</details>
