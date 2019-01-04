# What's Missing In Geoparsing?

***
**NEWS UPDATE 1.1.2019** - We have a **LONG FOLLOW-UP PAPER OUT NOW** that greatly expands on this topic. The title is **["A Pragmatic Guide to Geoparsing Evaluation."](https://arxiv.org/abs/1810.12368)** It's on arxiv as a preprint and under review at Springer LREV Journal. **[Download Now](https://arxiv.org/abs/1810.12368)!** For the project/paper repository, **[follow this link](https://github.com/milangritta/Pragmatic-Guide-to-Geoparsing-Evaluation)**.
***

> "Science is a wonderful thing if one does not have to earn one's living at it." -- Albert Einstein

## Summary

Thanks for stopping by! In this repository, you will find the accompanying code and data for the publication "What's missing in geographical parsing?" in the journal [Language Resources and Evaluation]( https://link.springer.com/article/10.1007/s10579-017-9385-8). In the unlikely case of any files missing, please track me down and I'll upload :+1:

## What's included

1. data - This is the output of all systems on both datasets (2 * 5 files) plus the gold standard (2 files) 
2. The dataset WikToR(SciPaper).xml is the original data as described and used in the paper.
3. The LGL dataset, which is also used for evaluation is included as lgl.xml
4. Essential experiment files (plus supporting scripts)

## How to replicate

You should have some basic Python libraries like Numpy, NLTK, Matplotlib (if you want graphics), ... to start with.
* methods.py is the main python script for running the experiments (requires the yahoo.py script)
* Please install [GeoPy](https://pypi.python.org/pypi/geopy/1.11.0) to calculate the distances between coordinates.
* Also install [Wikipedia](https://pypi.python.org/pypi/wikipedia/) for Python, nice API wrapper :+1:
* Scroll down to the end of the file to see example usage, I included all necessary instructions and comments. 
* Enjoy!

## How to (re)create and modify WikToR

The dataset (WikToR) can be created (and unite tested) from scratch, extended, reduced, with more or fewer sentences added, etc. If you wish to do that, great! Here's what you need:
* The wiktor.py file is the python script used to (re)generate and unit test WikToR.
* Download the [allCountries.txt](http://download.geonames.org/export/dump/) data dump from GeoNames and save in the same directory as the script.
* Please sign up for a [GeoNames](http://www.geonames.org/login) account and a USERNAME, which you will need to fill in on line 42 to ensure the API query works.
* The first half of wiktor.py is for CORPUS CREATION, the second half is for CORPUS TESTING.
* Enjoy!

---
> "The science of today is the technology of tomorrow." -- Edward Teller
