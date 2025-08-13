# Loan Document OCR Extraction and Eligibility Check

This project processes scanned or digital loan application documents, extracts relevant fields using **OCR (Tesseract)**, and determines loan eligibility based on predefined business rules.

## Features
- **Image Preprocessing** (grayscale conversion, denoising, thresholding)
- **OCR Extraction** using [Tesseract OCR](https://github.com/tesseract-ocr/tesseract)
- **Regex-based Field Parsing** for:
  - Name
  - PAN
  - Salary
  - Loan Amount
- **Eligibility Check** based on salary-to-loan ratio
- **Batch Processing** of all images in a folder
- **Results Export** to CSV and Excel formats

## Example Workflow
1. Preprocesses the document image to improve OCR accuracy.
2. Runs OCR to extract raw text.
3. Uses regex to identify and extract structured fields.
4. Applies an eligibility rule:
   
pip install opencv-python pytesseract pandas
python loan_doc_ocr_extractor.py synthetic_dataset

.
├── loan_doc_ocr_extractor.py
├── synthetic_dataset1/
│   ├── doc_1.png
│   ├── doc_2.png
│   └── ...
├── loan_results.csv
├── loan_results.xlsx
└── README.md

