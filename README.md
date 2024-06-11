# Fetch_pdf

The script first imports some Python libraries like requests, pymupdf, and PyPDF2.

`requests` is a Python library used for making various types of HTTP requests like GET and POST. In this case, it is used to download the PDF files.

`pymupdf` (fitz) is a Python binding for the PDF processing library MuPDF. It is used in this script to read the PDF content.

`PyPDF2` is a Python library used to read, split, merge, and add metadata to PDF documents.

The script then defines a bunch of helpful functions. These functions:

- Download and store the PDF file given a url Google Drive.
- Extract text from the PDF and clean it.
- Extract phone numbers and emails from the cleaned text using regular expressions.

The script then reads an input CSV file that contains the necessary data (fund names, ISIN, prospectus), and for each prospectus, it calls the above functions to fetch the PDF, extract text, phone numbers, and emails. It then stores this information into lists which are added to the dataframe. Lastly, the script outputs a CSV file containing the extracted phone numbers and emails along with the respective page numbers they were found on in the PDFs.

## Instructions to run

1. Download the ipynb file and upload to Google Drive
2. Open the file in Google Drive
3. Rename the input file to 'input.csv'
4. Open the left column with the 'file' image
5. Upload 'input.csv'
6. Click 'run' subsequently.
7. Download 'output.csv' for the result.

## Output Rules

The output file follows the rules below

1. The phone number and email only output the one with the most appearance times
2. The page list contains all the pages where phone and email appear.
