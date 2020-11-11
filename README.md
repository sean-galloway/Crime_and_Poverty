# Crime_and_Poverty
## Questions
1. List the Poverty Rates versus Crime Rates for years 2014-2019.
2. List the Property Values versus Crime Rates for year 2014-2019.
3. Which Sacramento zip codes have the highest median home price?
4. Which Sacramento zip codes have the lowest median home price?
5. Is there a correlation between home price and crime rate?
6. Is crime increasing in either the lowest or highest property value areas?
7. Analyze the crime data by "bucket." Make a bar char of the crimes per bucket per year to see the changes over time.
8. Make a heat map of all of the crimes for the area for the "Crimes against the person *" (Title 8 and Title 9)
9. Make a heat map of all of the high poverty areas.
10. Analyse the crime rates versus the high poverty areas.
11. Analyse the crime rates versus the low poverty areas.

## To Do List:
1. Sean: 
* Add the raw Crime.csv file to the Resources file 
* Clean the crime data, store in Resources/Crime_clean.csv
* Create the zip code to city csv file and store 
2. Cora:
* 

## Data Sets
1. https://data.saccounty.net/datasets/9a7f2df25a584ff9b55db274704ad7c9_0/geoservice
2. http://www.ciclt.net/sn/clt/capitolimpact/gw_ziplist.aspx?FIPS=06067
3. https://leginfo.legislature.ca.gov/faces/codedisplayexpand.xhtml?tocCode=PEN
4. Need a data source for median home values per zip code.

## Niche Beatuiful Soup Example
import requests
from bs4 import BeautifulSoup
import pandas as pd
import os

nicheprefix = "https://www.niche.com/places-to-live/n/"
nichesuffix = "-atlanta-ga/"

def get_link(url):
    ret_value = 0
    from urllib.request import Request, urlopen
    from bs4 import BeautifulSoup as soup
    print(url)
    try:
        req = Request(url, headers={'User-Agent': 'Mozilla/5.0'})
        webpage=urlopen(req).read()
        page_soup = soup(webpage, "html.parser")

        mydivs = page_soup.findAll("div", {"class": "scalar__value"})
        
        #print (len(mydivs))
        #print (mydivs[1])
        ret_value = (mydivs[1].find("span").get_text())

    except:
        print ("Could Not Find")
        
    return ret_value

niche_price = []

niche_url = neighborhoods['Niche URL'].tolist()

for niche in niche_url:
    niche_price.append(get_link(niche))
    
