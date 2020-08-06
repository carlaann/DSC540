#
Fuzzy Matching on Infectious Disease by US CDC
#
Librairies
#
1. Pandas
2. Numpy
3. Fuzzywuzzy
#
The project consist one of the tables from the disease outbreaks which consisted of gonorrhea, Haemophilus Influenza Invasive Disease. The law requires monitoring of the disease to prevent outbreaks.  The dataset contains provisional cases of national notifiable diseases from the National Notifiable Diseases Surveillance System (NNDSS). NNDSS data from the 50 states, New York City, the District of Columbia and the U.S. territories are collated and published weekly on the NNDSS Data and Statistics web page (https://wwwn.cdc.gov/nndss/data-and-statistics.html). Cases reported by state health departments to CDC for weekly publication are provisional because of the time needed to complete case follow-up. Therefore, numbers presented in later weeks may reflect changes made to these counts as additional information becomes available. The national surveillance case definitions used to define a case are available on the NNDSS web site at https://wwwn.cdc.gov/nndss/. Information about the weekly provisional data and guides to interpreting data are available at: https://wwwn.cdc.gov/nndss/infectious-tables.html. Data are finalized 10 months after the end of the year.  
#
The data is collected from the CDC.   The data file location is: https://data.cdc.gov/NNDSS/NNDSS-TABLE-1M-Gonorrhea-to-Haemophilus-influenzae/h4wb-nae4 and the file names is as follows: 

“NNDSS__TABLE_1M._Gonorrhea_to_Haemophilus_influenzae_invasive_disease_age_5_years_Serotype_b. “

Step 1: Import Data 
The data files are read into ‘pandas’ dataframe using pandas ‘read_csv’ method.

Step 2: Replace Header
The headers were already having proper understandable format to understand. In order to tweak them, the headers there were some symbols and other punctuations in them after importing which were removed
Step 3: Outliers
I was able to find from the five-point summary of the variables by using describe function of pandas. Then, a 98th percentile was used to seal the numeric variables to treat the outliers.

Step 4: Finding and Handling Duplicate Rows
Since there were no duplicates in the dataset, there was not so much we could do in this section.  
.
Step 5: Fuzzy Matching
Challenge lied in identifying the variable to conduct fuzzy matching. There are no two 'logically making sense variables' in the dataset on which fuzzy matching could be done. However, I then considered to do a cross join of location variable in the dataset and find out the fuzzy scores with other locations in the same variable. Then, it was a straightforward thing to have it printed for fuzzy scores>50.
#
