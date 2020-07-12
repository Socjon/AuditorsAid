# Auditors Aid - Anomaly Detection in Not-for-Profit Data

## Synopsis
Non-Profit organizations are required to self-identify their area of focus based on the type of work 
the organization does. I created machine learning models to classify these subgroups based on their annual 990 
filings.

The intent of the project was to identify inconsistencies within these subgroups.
This in turn would give the IRS auditors specific organizations to investigate and reduce fraud.

A [slide deck](https://github.com/Socjon/AuditorsAid/blob/master/Another%20tool%20for%20Auditors.pdf) is also available to peruse for highlights.

## Motivation

In efforts to make the government more efficient and better equipping our civil employees
with the effective tools, I strove to see what kind of analysis could be performed with public data.

We need a Government that embraces new technologies, but that is also transparent enough that any
citizen could do analysis and reaches the same conclusion. Data is not objective. 

## Data Source
[Open Data for Nonprofit Research](https://github.com/lecy/Open-Data-for-Nonprofit-Research):

"The IRS maintains several important nonprofit databases to track the current population 
of exempt organizations, their annual 990 filings, and organizations that have closed. 
This data has been released in formats that are not always easy to use - ASCII text files,
json files, and XML queries. In order to make the data accessible to the research 
community, [[Jesse Lecy and a team]](https://lecy.github.io/Open-Data-for-Nonprofit-Research/)
have created scripts to download data from IRS websites, clean and process it, and export into familiar formats (CSV, Stata, SPSS, etc.)."
 

## Conclusion

After running multiple subsets of the data through regression based, tree based, and ensemble
methods, the best model accuracy 36% in predicting the correct non-profit subgroup.

Compared to true random (4%), a predictive model yields promising results if this kind of analysis
were to be incorporated into the auditing framework. 

## Areas of Improvement
Effort has been put in to combat a few fundamental issues with the dataset.

There is a class imbalance problem, e.g. there are more non-profits active in the 
in Education sector than active non-profits involved in the International, Foreign Affairs, and National Security
sector by a factor of 8, etc, etc. Multiple subsets of the source data was used in analysis to counteract this along with
different modeling techniques.

Other areas that could be improved upon; improving the mapping of an older IRS non-profit
classification system to their current standard, as well as incorporating more data into the model from other IRS sources.
