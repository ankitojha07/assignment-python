# Fetch PubMed Papers

## Overview
This script fetches research papers from the PubMed API based on a user-specified query. It extracts key details such as title, publication date, non-academic authors, company affiliations, and the corresponding author's email. The results are saved to a CSV file for further analysis.

## Features
- Fetches research papers using PubMed API
- Extracts relevant details including non-academic authors and company affiliations
- Saves results in a structured CSV file
- Designed for use in Google Colab

## Installation & Setup (Google Colab)
1. Open Google Colab.
2. Install dependencies (if not already installed):
   ```python
   !pip install requests
   ```
3. Copy and run the provided Python script in a new Colab cell.

## Usage
### Running the Script in Colab
1. Import and run the function with your desired query:
   ```python
   papers = run_colab("cancer research")
   ```
2. The results will be saved in `pubmed_results.csv` and printed in the output.

## Output
The script generates a CSV file with the following columns:
- **PubmedID**: Unique identifier for the paper.
- **Title**: Title of the paper.
- **Publication Date**: Date when the paper was published.
- **Non-academic Author(s)**: Names of authors affiliated with non-academic institutions.
- **Company Affiliation(s)**: Names of pharmaceutical/biotech companies.
- **Corresponding Author Email**: Email address of the corresponding author.

## Example Output (CSV)
```
PubmedID,Title,Publication Date,Non-academic Author(s),Company Affiliation(s),Corresponding Author Email
123456,Study on Cancer Treatments,2023-10-15,John Doe,ABC Pharma,johndoe@abcpharma.com
```

## Notes
- The script limits results to **10 papers** for testing. You can modify this limit in the `fetch_pubmed_papers()` function.
- It uses heuristics to identify non-academic authors based on affiliations (excluding universities, colleges, and institutes).
