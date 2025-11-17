Use GSE59867 as demo to acquire each GSM information and combine to a txt file and a GSM demo to test

GEO GSM Scraper (Playwright + Python)

This repository provides an automated workflow to:
	1.	Fetch all GSM sample IDs from a given GSE accession.
	2.	Retrieve each GSM page from the NCBI GEO website using Playwright.
	3.	Save:
	•	The first GSM page as a test file.
	•	A merged text file containing all GSM pages.

This tool is helpful for bioinformatics workflows that require bulk metadata extraction from GEO.

Features
	•	Automatically retrieves all GSM IDs from a GSE.
	•	Uses Playwright headless browser to fetch full GSM page content.
	•	Produces two output files:
	•	<GSE_ID>_FIRST_GSM.txt
	•	<GSE_ID>_ALL_GSM.txt
	•	Works cross-platform (macOS / Linux / Windows).

  Requirements

Python ≥ 3.8

Install required packages:

```
pip install playwright requests beautifulsoup4
playwright install
```

Usage

Modify the GSE accession at the top of the script:
```
GSE_ID = "GSE59867"
```
Then run:
```
python geo_scraper.py
```

You will get two files on your Desktop:
```
GSE59867_FIRST_GSM.txt
GSE59867_ALL_GSM.txt
```
