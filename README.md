# CCTs_School_Enrollment

This repo contains .do files, .R files, and (intermediate) datasets for the analysis in my paper "Do Early-ending 
Conditional Cash Transfer Programs Discourage Continued School Enrollment?". A working paper version is available
at https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3429762. 

The raw data for my paper "Do early-ending conditional cash transfer programs discourage continued school enrollment?" 
comes from the website https://evaluacion.prospera.gob.mx/en/eval_cuant/p_bases_cuanti.php, which was no longer 
available at the time of writing. 

## How to run it

To merge the various survey rounds, define relevant variables, and construct datasets for analysis in R, open 
"MakeDataset.do" in Stata, change the directory to the adress of the Progresa folder, and run. The location-specific 
variables are constructed in a separate file, "MakeLocationData.do". To run this, change the directory to the
adress of the Progresa folder first. 

To obtain summary statistics, open "SummaryStats.do" in Stata, change the directory to the adress of the Progresa folder, 
and run.

To obtain the DML results, open "Run.R" in R. Change the directory to the adress of the Progresa folder. Change the 
variables "set", "status", and "outcomename" according to the subset and dependent variable of interest. Adjust the 
settings for parallel computing accordingly. Before running the program, make sure all required packages are installed. 
The results of the DML estimation are saved in the matrix "result". The vectors of relative importance are saved in the 
vector "delta.0". 

## Repository structure

```
├── ReadMe.txt        <- You are looking at it. 
│
├── Do files          <- To be run in Stata. Contains files fordataset construction and summary statistics.
│
├── R files           <- To be run in R. Contains all DML analysis files.
│
├── Raw data          <- Contains questionnaires and survey data by year (.dta files ignored).
│   ├── 1997         
│   ├── 1998         
│   ├── 1999         
│   ├── 2000         
│   └── 2003         
│
├── Intermediate data <- Contains .csv files used for analysis
│

```



Martin Wiegand, 26. April 2022
