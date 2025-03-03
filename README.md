# VeriGenTool
To Build an AI-powered tool using NLP or Python to validate verification criterion

Verification Criteria Validation Process
Overview
This process validates verification criteria extracted from an Excel file by checking for required Pattern and suggesting patttern when needed. The application is built using Python, NLTK, Pandas, and Streamlit to provide an interactive dashboard for validation and analysis.

Process Workflow:

1. Data Input
The user uploads an Excel (.xlsx) file that contains a column named "DA_Verification_Criteria".
The program reads this column and processes the text to check for required verification headings.

2. Data Cleaning & Processing
The text is tokenized into sentences using the NLTK library.
Each sentence is analyzed, and the function clean_heading() extracts key pattern(using defined Headings).
Headings are checked against a predefined list:
Pre-Condition
Acceptance Criteria
Input
Output

3. Verification & Validation
The check_headings() function determines whether all required headings are present in the text.
If a heading is missing:
The validation status is marked as "Not Matched with RuleBook".
A suggested structure is provided to guide corrections.
If all required headings are found:
The validation status is "Matched with RuleBook".

4. Output File Generation
A new Excel file is generated with additional columns:
 . Verification Criteria Validation Status (Matched / Not Matched)
 . Missing Rule Patterns (Lists missing headings)
 . Suggested Rule Book Pattern (Provides a corrected structure)
The file is formatted using OpenPyXL, where:
Matched rows are highlighted in Green.
Not Matched rows are highlighted in Red.
Text wrapping is applied for better readability.

5. Visualization
A pie chart is displayed on the Streamlit Dashboard to show:
The percentage of Matched vs Not Matched criteria.
Counts for each category.

6. User Interaction
Users can upload an Excel file.
After validation, they can download the processed output with the corrected details.
A graphical summary provides a quick overview of validation results.

Libraries Used
Pandas - For handling Excel data.
NLTK - For sentence tokenization.
OpenPyXL - For formatting Excel output.
Streamlit - For building an interactive dashboard.
Matplotlib & Seaborn - For visualization.
