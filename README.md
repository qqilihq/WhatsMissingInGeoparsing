# What's Missing In Geoparsing?

***
**FORKED REPOSITORY 2022-05-21** – This is a fork of the original repository which adds evaluation output which was created using Palladian’s Location Extractor. Also, it fixes the Python code to work with Python 3.

For more information about the Palladian Location Extractor please refer to the original paper: <a href="http://philippkatz.de/AusDM-Location-Extraction.pdf">To Learn or to Rule: Two Approaches for Extracting Geographical Information from Unstructured Text</a>; Philipp Katz and Alexander Schill; Proc. of the 11th Australasian Data Mining & Analytics Conference (AusDM 2013).

Despite its age, the Palladian Location Extractor can be considered state-of-the-art and outperforms most of the other systems (GeoTxt, Edinburgh, Yahoo, CLAVIN, Topocluster).

See class `ws.palladian.extraction.location.evaluation.DatasetProducer` in Palladian for how to produce the data.

Thank you to Milan Gritta for making this available!
***

***
**NEWS UPDATE 31.9.2019** - We have a **LONG FOLLOW-UP PAPER OUT NOW** that greatly expands on this topic. The title is **["A Pragmatic Guide to Geoparsing Evaluation."](https://link.springer.com/article/10.1007/s10579-019-09475-3)** It's now been published at Springer LREV Journal. For the project/paper repository, **[follow this link](https://github.com/milangritta/Pragmatic-Guide-to-Geoparsing-Evaluation)**.
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
* Also install numpy and matplotlib
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
