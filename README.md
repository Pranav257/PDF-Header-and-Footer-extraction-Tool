This tool is designed to extract and compare headers and footers across multiple pages of a PDF file. It helps identify inconsistencies in headers and footers between the pages. The tool uses PyMuPDF to handle PDF operations and regex for text cleaning.

Features
Extract headers and footers from each page of a PDF document.
Clean text by removing numbers, AM/PM notation, and excessive whitespace.
Compare headers and footers between pages to identify differences.
Display differences and similarities in a clear and concise format.
Installation
This script requires Python 3.6 or higher. Before running the script, you must install the necessary Python package:

bash
Copy code
pip install pymupdf
Usage
To use this tool, follow these steps:

Prepare your PDF file: Ensure your PDF file is accessible by the script, ideally in the same directory as the script or specify the path.
Modify the script: In the script, update the pdf_path variable to the location of your PDF file.
Run the script: Execute the script in your Python environment. The script outputs the headers and footers of the first two pages and then the differences, if any, for subsequent pages.
Example Command
bash
Copy code
python your_script_name.py
Script Functions
clean_text(text): Cleans text by removing numbers, AM/PM markers, and reducing multiple spaces to a single space.
is_similar(header_footer_1, header_footer_2): Compares two strings and returns whether they are similar based on cleaned content.
identify_header_footer(blocks): Identifies and returns the header and footer from a list of text blocks.
extract_text_blocks(pdf_path): Extracts text blocks from each page of the specified PDF file and sorts them vertically.
print_differences_and_update(new, old, page_num, type): Prints and returns the differences between new and old headers/footers.
print_header_footer_first_two_pages_and_differences(pdf_path): Extracts and prints headers and footers for the first two pages and then checks for differences in subsequent pages.
Output
The script prints the header and footer of the first two pages of the PDF and then highlights differences in these sections on subsequent pages.

Notes
Ensure your PDF content is accessible to PyMuPDF for reading and extracting text.
The script currently handles text-based PDFs and might not accurately process image-based or encrypted PDF documents without modifications.
