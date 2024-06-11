# Resume/CV Scanner

## Introduction
Resume/CV Scanner is a Streamlit application that scans resumes and determines the best matching job domain based on the skills listed in the document. This application uses BERT models and Spacy for natural language processing to provide insights into which domain best fits the resume content.

## Hosted App : [Resume/CV Scanner](https://huggingface.co/spaces/liberatoratif/CareerMatcher)

## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Dependencies](#dependencies)
- [Configuration](#configuration)
- [Documentation](#documentation)
- [Examples](#examples)
- [Troubleshooting](#troubleshooting)
- [Contributors](#contributors)
- [License](#license)

## Installation
To run this project locally, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/mo-atiff/resume-cv-scanner.git
    cd resume-cv-scanner
    ```

2. Create a virtual environment and activate it:
    ```bash
    python -m venv env
    source env/bin/activate # On Windows use `env\Scripts\activate`
    ```

3. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

4. Download the Spacy language model:
    ```bash
    python -m spacy download en_core_web_lg
    ```

5. Place the `target_encodings.pkl` and `linkedin_skill.txt` files in the project directory.

## Usage
1. Run the Streamlit application:
    ```bash
    streamlit run app.py
    ```

2. Open your web browser and navigate to `http://localhost:8501`.

3. Upload your resume in `.docx` format and click the 'SCAN 📝' button.

4. The application will display the predicted job domain and the percentage match for various domains.

## Features
- Extracts text from `.docx` resume files.
- Cleans and processes resume text to remove unwanted characters and stop words.
- Matches skills using a pre-defined list of skills.
- Uses a BERT model to predict the most suitable job domain based on the resume content.
- Displays the predicted domain and the probability of matching for each domain.
- Identifies and validates the presence of email, phone number, and links in the resume.

## Dependencies
- streamlit
- plotly
- pandas
- numpy
- pickle
- spacy
- docx2txt
- transformers
- torch
- re

## Configuration
- Ensure that the `target_encodings.pkl` and `linkedin_skill.txt` files are available in the project directory.
- Customize the Streamlit page settings in `app.py`.

## Documentation
Further documentation can be found within the code comments and function docstrings in `app.py`.

## Examples
Upload a sample `.docx` resume file and click 'SCAN 📝' to see the application in action.

## Troubleshooting
- Ensure that you have the necessary files (`target_encodings.pkl` and `linkedin_skill.txt`) in the correct directory.
- Verify that the Spacy language model (`en_core_web_lg`) is installed.
- Check that your resume file is in `.docx` format.

## Contributors
- [Your Name](https://github.com/mo-atiff)

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Hosted Application
You can also use the hosted version of this application on Hugging Face Spaces: [Resume/CV Scanner](https://huggingface.co/spaces/liberatoratif/CareerMatcher)
