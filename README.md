# cigna-python-challenge

# **How To Send** 

Clone down the solution and copy it into your own GitHub repo.
Please include a section in the ReadMe walking through how you solved it and the process you used. 
You will send your Github repo link to your recruiter when finished. 

# **Instructions**

Create an ETL script, which imports, parses, aggregates and outputs the data in 1 required 
format, and for bonus points, several optional formats (more details below).

The source data can be seen below in CSV format.

The data is formatted as such to supply an hourly snapshot of the percentage of free memory. 
Each unique entry (hostname), is stored on each column.  Each row below the column represents 
a snapshot of the collected data, stored via the 'Date / Time' timestamp stored in epoch time.

The format of the column keys are 'node type#hostname#metric', so as an example, the hostname 
for the string 'host#HOST1#% Free Memory avg 1h' could be identified as HOST1.  Columns are 
comma delimited.

Please create a process which will intake the below provided CSV source, and generate 1 line 
of output for the following aggregations:

- The minimum value for each unique hostname.
- The maximum value for each unique hostname.
- The average value for each unique hostname.

Additionally, generate the following aggregated values:

- The minimum value for all results.
- The maximum value for all results.
- The average value for all results.

Data for your results should be stored in a result format which you can utilize to output your 
results to STDOUT. Optionally, we'd like for you also to provide formatted output for some of 
the following options:

- XML
- JSON
- YAML

These results can be written to external files, for extra credit.

You will be allowed full use of the search engine of your choice.

Good luck!

HOW I CAME UP WITH MY SOLUTION

- Imported pandas and sys for data processing and output purposes
- Used pandas 'read_csv' function to grab the csv file holding the required data and store it in a variable as a reference 
- Dropped the Date / Time column because the field is not relevant and removing irrelvant fields/data will save memory
- Declared variables for the maximums, minimums, and means for each Hostname
- Declared variables for the maximums, minimums, and means for all of the results 
- Used the sys library to output the maximums, minimums, and means pandas series for each host name along with each pandas series' maximums, minimums, and means

