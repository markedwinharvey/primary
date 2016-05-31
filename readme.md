Sample matplotlib output data:
![primary sample 1](https://github.com/markedwinharvey/primary/blob/master/media/p_update4.png)
![primary sample 2](https://github.com/markedwinharvey/primary/blob/master/media/jt_update1.png)

`primary.py` uses the requests module to scrape US presidential candidates' names from 
news and politics sites listed in `news_sites.txt`, compared against names in `names.txt`. The 
data is automatically saved in a csv-formatted file as 'dat2_'+current date/time, with optional note
to add per data set. 

The program is currently set to run every four hours. 

All markup data (html invisible to casual user) and script data is removed prior to name parsing. Inclusion of 
markup data artificially inflates the results in terms of words visible/invisible to the user. 
On the other hand, some sites load content dynamically, so the results are only an estimate of the relative
proportion of names in the data. 

But some might say that a picture is worth a thousand trumps. ...So even including the markup/script data 
(which has a noticeable effect on the results)
is arguably something
of an understatement of the percent content devoted to particular candidates
(perhaps pixel count should factor in). 
In any case, the true number of trumps per front page news (total html content) can be calculated
by eliminating/commenting the area in the code where the website data is shrunk (i.e., function `remove_markup` in 
`primary.py`).

`primary2.py` offers to open a selection of the available data and displays the selected data as a 
mini ascii spreadsheet. 

`analyze.py` visualizes the available data (numpy/matplotlib), the average percentage per query (over all journals) and the 
raw totals from all journals. 
A trendline-finding module was added and incorporated into the visualization, such that the program 
also plots the results of linear regression on each data set to show overall trends. 
An additional plotting function looks at the spread of all data points from all media sources assayed. An example is shown. 
