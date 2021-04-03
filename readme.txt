My Project - G3-Genes Genomes Genetics

SUBMISSIONS
===========
PROJECT.RAR file -- Contains all the HTML pages for all Articles for all Years and Months along with the extracted Information for each one them written to a csv file
Two Python scripts written
	1) Crawl Script - MidTerm_Project_Genomes_Crawl.ipynb
	2) Read Script - MidTerm_Project_Genomes_ReadMe.ipynb

The Scripts have comments describing what is being done


SCRIPT 1
=========
The function Genes_Genomes_Genetics extracts information from the Journal - G3-Genes Genomes Genetics

The Columns being extracted for each Article are
'ID', 'AUTHORS', 'PUBLISH DATE', 'TITLE', 'ABSTRACT', 'FULL PAPER','AFFILIATIONS', 'CORRESPONDENCE AUTHOR', 'KEYWORDS', 'CORRESPONDENCE AUTHOR'S E-MAIL

The Function takes a year as parameter, all articles for that Year and subsequent years are extracted into CSV file as well as the HTML pages saved into a folder structure by Year and Month

The Function loops through Year, Month and Articles in a Month, then from each Article, it extracts the Above column header values as well as HTML pages. 
I have used Regex and Replace functions too to strip some unwanted characters or extract substrings from the extracted tags/text
Each of the crawled information is written into a dictionary and the result is all put into a List which is used to prepare the csv file at the end
For Crawling and Extraction I have used modules requests and BeautifulSoup. For actual HTML pages I have used urllib
For writing to csv file I have used DictWriter


SCRIPT 2
========

This reads the csv file created from SCRIPT 1
Actually I tried using DictReader first to read the file as through research I found it is most time efficient to read large files but I think because of my local set-up issues I am seeing
IOPub data rate exceeded. error in the Jupyter notebook, even though I can read the file

So I went ahead and read the file using Pandas read_csv too and can get the results in a dataframe