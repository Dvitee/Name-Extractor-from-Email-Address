project:
  name: "Name Extractor from Email Address"
  file: "extract_name_from_email.py"
  description: >
    A simple NLP-based Python script that extracts and cleans names from email addresses 
    by removing symbols, dots, and extra characters. 
    Example: "john.smith@example.com" → "johnsmith"
  status: "Prototype / Rough NLP Experiment"
  author: "Tanvi Salgaonkar"
  license: "MIT"

features:
  - Extracts local part of email (before '@')
  - Removes dots, plus signs, and special characters
  - Converts the result to lowercase
  - Works on simple and complex email formats

example_input_output:
  - Original Email: "john@example.com"
    Extracted Name: "john"

  - Original Email: "john.smith@example.com"
    Extracted Name: "johnsmith"

  - Original Email: "disposable.style.email.with+symbol@example.com@example.com"
    Extracted Name: "disposablestyleemailwithsymbol"

  - Original Email: "fully-qualified-domain@example.com"
    Extracted Name: "fullyqualifieddomain"

example_usage: |
  from extract_name_from_email import extract_name

  email = "john.smith@example.com"
  name = extract_name(email)
  print(name)  # Output: johnsmith

how_it_works:
  - Splits the email at '@' and uses the first part
  - Removes special characters like '.', '+', and '-'
  - Keeps only alphabets and numbers
  - Returns the cleaned lowercase string as the extracted name

installation:
  - git clone https://github.com/<your-username>/name-extractor.git
  - cd name-extractor
  - python extract_name_from_email.py

future_improvements:
  - Add option to format names (e.g., JohnSmith → John Smith)
  - Handle initials or company emails (e.g., hr@, info@)
  - Extend with regex or NLP tokenization

contact:
  github: "https://github.com/<your-username>"
  linkedin: "https://linkedin.com/in/<your-linkedin>"
