# US_foreign_debt
This analysis looks at how total foreign holdings of U.S. Treasury securities have changed over time and which countries hold the most American debt, using data from the U.S. Department of the Treasury's [Treasury International Capital (TIC) system](https://home.treasury.gov/data/treasury-international-capital-tic-system).

# Who Owns America's Debt?

This is a project for [Data Studio](https://journalism.columbia.edu/ms-data-journalism), Spring 2026.

This analysis looks at how total foreign holdings of U.S. Treasury securities have changed over time and which countries hold the most American debt, using data from the U.S. Department of the Treasury's [Treasury International Capital (TIC) system](https://home.treasury.gov/data/treasury-international-capital-tic-system).

This dataset, reports monthly country-level holdings in billions of dollars from March 2000 to December 2025, based on U.S. custodian reports on the country of the foreign entity holding the securities. It does not include multilateral holders such as the IMF, World Bank, or ECB.

**Project page:** [AI-energy-usage](https://dimuthuattanayake.github.io/US-creditors/)

## Methodology

Find in [Analysis](https://github.com/DimuthuAttanayake/AI-energy-usage/blob/main/who_powers_ai.ipynb)

### Data collection and cleaning

* Downloaded the data from the U.S. Department of the Treasury's [Treasury International Capital (TIC) system](https://home.treasury.gov/data/treasury-international-capital-tic-system).
* Data was downloaded as a txt file and then converted to a csv. There are multiple tables in the saved csv sheet arranged by year, so I combined all of these to a single table for analysis. ChatGPT helped with this part of the code. 
*  Table was cluttered and was not ordered in a way that I could analyze the monthly debt flows for each year, so I to cleaned and reorganized the table first.
*  There were duplicate columns for some months, and in some years, there were extra spacing for countries etc.This was cleaned up.
*  Because I compiled a number of tables into one table the individual grand totals no longer made sence and would have introduced errors to the analysis, so removed that.
*  Some of the countries were double counted because they were in different groups such as 'oil exporters', 'carribean bankers' until February 2016. So removing these too.
*  United Kingdom included Channel island Isle of Man until February 2026, it was named with "United Kingdom/2". Cleaned this to make "United Kingdom" one continous line throughout. No separate Channel Islands or Isle of Man entries exist in the data so it is not possible to combine the data together throughout, which would have been more accurate.
*  'Belgium-Luxembourg' was a single row in 2000–2001, then split into separate rows from 2002 onward with a "Belgium  5/" in 2002. This was made consistant for the analysis,by cleaning to make one continous line throughout (Similar to United Kingdom).
*  Belgium and Luxembourg was grouped together from 2001 until February 2016, and the row was named different names over time. Making it one name ('Belgium-Luxembourg') and then added up the two countries until 2025, for consistancy. 

### Analysis

* I wanted to understand the top US creditors in 2025, and how this trend changed over time. For this, I am calculating the country averages from 2000 to 2015, and then looked at how the major creditors changed over time.
* I looked at which country held the most amount of debt in 2025, by filtering up countries that held over USD 0.3 trillion. 'All Other' category was dropped because I was more interested in individual countries or special groups (tav havens).
* Sinece Belgium, Luxemberg, Cayman Islnds and Ireland are 'tax havens' I looked at how they have performed as agroup over time.


### Visualisations

* I built a scrolly using scrollama.js. It is responsive on mobile, tab and laptop, with four charts showing how the top US creditors changed over time,
* The charts were made with Data Wrapper and then converted with ai2html before building into a webpage using css, html and github actions.
* These are the individual charts:
  -Total Debt: Single line showing total foreign-held U.S. Treasury securities from 2000 to 2025.                  
  -China: China's rise as America's biggest creditor, peaking at $1.28T in 2013, then declining to $0.72T by 2025.                     -Japan: Shows Japan and China lines in one chart,highlighting the crossover in 2019 when Japan overtook China as the top creditor.
  -Tax Havens: Financial centers (Belgium-Luxembourg + Cayman Islands + Ireland combined) rising to $1.6T by 2025, surpassing Japan.    
## New Skills

* Creating scrollys's with multiple charts
* Using scrollama.js
* Narrative storytelling with data vizualisations

## What Inspired My Design

* Reuters US-N. Korea relations](https://www.reuters.com/graphics/TEST-TEST/010070HX15H/)
* [Washington Post US energy production](https://www.washingtonpost.com/graphics/national/power-plants/)  

## What more would I like to do?

* Analyze a dataset with multilateral creditors and the countries to understand the full picture
* Learn to make the transition between Vizualisations smoother and, cleaner
* Build multiple charts that are of same dimensions
* Use After Effects to animate this and use the video to build the scrolly so that transitions are clearer and smoother

## Contact

Dimuthu Attanayake, [dca2140@columbia.edu](mailto:dca2140@columbia.edu)

