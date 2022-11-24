# File format definition for instances
Instances can be stored in binary (NumPy) or CSV format. The latter is easily explored manually and will be defined below.

An instance, when stored in .csv-format, comprises two files:
- `constants.csv` contains a semicolon-separated list of constants and their labels associated with the instance.  
  These instances only have a single constant defined, namely `resource_availability` $P$. An example constants-file might look as follows:  
  ```
  resource_availability;25.0
  ```
- `jobs.csv` contains a row (or line) for every job, defining its characteristics in a semicolon-separated list. The first row contains the data for the job with index 0, the second for job with index 1 and so on.  
  An example jobs-file (for five jobs) might look as follows:  
	```
  14.28;1.83;8.76;5.53;11.77;2.57;4.81
  12.12;2.11;9.80;0.73;9.51;1.00;2.04
  82.88;5.46;49.20;5.76;13.20;2.76;0.75
  73.09;3.73;34.65;7.83;14.20;2.22;0.01
  35.06;3.91;20.68;2.06;3.91;4.40;6.77
	```
  The properties listed are, in order:
    - resource requirement $E_j$;
    - resource lower bound $P^-_j$;
    - resource upper bound $P^+_j$;
    - release date $r_j$;
    - deadline $\bar{d}_j$;
    - weight $W_j$;
    - objective constant $B_j$.  
  
