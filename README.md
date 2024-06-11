# Replication kit to ATD SMS Updated

This replication kit is related to update of the paper 'Architectural Technical Debt - A Systematic Mapping Study' accepted in SBES 2023 after doctoral thesis review.

Armando Sousa, Lincoln Rocha, and Ricardo Britto. 2023. Architectural Technical Debt - A Systematic Mapping Study. In XXXVII Brazilian Symposium on Software Engineering (SBES 2023), September 25–29, 2023, Campo Grande, Brazil. ACM, New York, NY, USA, 10 pages. https://doi.org/10.1145/3613372.3613399

The original repository is available on https://github.com/armandossrecife/smsatd

## More details

You can find the following structure: 

```bash
.
├── LICENSE (Simplified BSD License)
├── README.md (Description of the replication kit)
├── csv (this folder contains .csv files)
├── dataset (this folder contains .csv, .xls, and .txt files related to the main dataset of the SMS)
├── images (this folder contains the figures generated by scripts and figures used in the main SMS paper)
├── latex (this folder contains the .tex files related to Latex tables)
├── md (this folder contains markdown files that support this replication kit)
└── python (this folder contains python scripts and .ipynb notebook files)
    ├── analyses (this folder contains .ipynb notebook files related to NLTK - Natural Language Toolkit - analysis)
    ├── auxiliary (this folder contains .ipynb notebook files that support latex files, text files, and generate md tables)
    ├── original (this folder contains the initial prototype of this replication kit - deprecated)
    ├── requirements.txt (this file contains all requirements necessary to run the scripts)
    └── util (this folder contains python scripts to support other functions of the replication kit)
```

You can find the following types of files in this replication kit:

- .csv files containing data to be analyzed in other tools.
- .xls files for general analysis in Excel.
- .txt files with general information in text format.
- .tex files for LaTeX tables.
- .md files containing markdown files published in this replication kit.
- .ipynb files containing Python notebook files to be executed in Jupyter Notebook or Google Colab.

## Requirements

- [pandas](https://pandas.pydata.org): pandas is a powerful data manipulation and analysis library that provides data structures like DataFrames and Series, making it easy to work with structured data.
- [numpy](https://numpy.org): is a fundamental package for scientific computing with Python, providing support for large, multi-dimensional arrays and matrices, along with an extensive collection of high-level mathematical functions.
- [xlrd](https://pypi.org/project/xlrd): is a library to read data and formatting information from Excel files (.xls). It allows you to extract data from Excel spreadsheets into Python data structures.
- [nltk](https://www.nltk.org): Natural Language Toolkit - nltk is a leading platform for building Python programs to work with human language data. It provides tools for text processing, tokenization, stemming, tagging, and more.
- [pillow](https://python-pillow.org): is a friendly fork of the Python Imaging Library (PIL), which provides support for opening, manipulating, and saving many different image file formats.
- [matplotlib](https://matplotlib.org): is a comprehensive library for creating static, animated, and interactive visualizations in Python. It provides a wide range of 2D plotting functionalities.
- [seaborn](https://seaborn.pydata.org): is a data visualization library based on matplotlib that provides a high-level interface for creating attractive and informative statistical graphics.
- [sklearn](https://scikit-learn.org/stable): scikit-learn is a versatile machine learning library that provides simple and efficient tools for data mining and data analysis. It includes various algorithms for classification, regression, clustering, and more.
- [tabulate](https://pypi.org/project/tabulate) is a library for tabular data formatting, providing a convenient way to display data in a structured and readable format, especially when working with lists, dictionaries, or DataFrames.

## Install dependecies

```bash
pip install -r python/requirements.txt
```

### Install [word cloud](https://github.com/amueller/word_cloud.git)

A little word cloud generator in Python.

```bash
git clone https://github.com/amueller/word_cloud.git
cd word_cloud && pip install .
```

Return to the main replication kit path (smsatd)
```bash
cd ..
```

### Install [Jupyter Notebook](https://jupyter.org/)

```bash
pip install jupyter
```

## Executing scripts

If you use jupyter notebook:

```bash
jupyter notebook
```

Open scripts in python folder that you want to run

If you use [Google Colab](https://colab.research.google.com/), you can simply open the Python script directly from Google Colab and install dependencies before running the selected Python script.

# Dataset

The dataset organize all studies used in this case. We created a spreadsheet to group the selected papers with all critical characteristics evaluated in this SMS.

The spreadsheet is available on [Extraction_form](https://github.com/armandossrecife/smsatd/blob/main/dataset/Extraction_form_basic2022.xlsx)

# Systematic Mapping Process

The main activities of this SMS follow five main phases: 

 - Define research questions 
 - Search process 
 - Selection process 
 - Extraction process 
 - Analysis process

![SMS Process](https://github.com/armandossrecife/smsatd/blob/main/images/sms-process.png) 

Figure 1 - show the flow used in this SMS

![Main Process](https://github.com/armandossrecife/smsatd/blob/main/images/searchprocess.png)

Figure 2 - summary of the literature study

We used the following [Form](https://github.com/armandossrecife/smsatd/tree/main/md/mytable_extract_data_eg.md) | [Script](https://github.com/armandossrecife/smsatd/tree/main/python/auxiliary/Convert_tables_to_latex_form.ipynb) to extract and analyze the data from the spreadsheet. 

# Scripts used to analyse the dataset

## Publications and Venue Types

[Selected Papers](https://github.com/armandossrecife/smsatd/tree/main/md/mytable_papers.md) | [Venues](https://github.com/armandossrecife/smsatd/tree/main/md/mytable_venues.md)

The following scripts [Selected papers](https://github.com/armandossrecife/smsatd/tree/main/python/auxiliary/Convert_tables_to_latex_sps.ipynb) and [sms_extraction](https://github.com/armandossrecife/smsatd/tree/main/python/analyses/sms_extraction.ipynb) is used to generate results about publications and venue types. 

## Research type of publication - according to Wieringa et al. (2006)

[Research types](https://github.com/armandossrecife/smsatd/tree/main/md/mytable_q7_distribution_detailed.md)

The following script  [Research type](https://github.com/armandossrecife/smsatd/tree/main/python/auxiliary/Convert_tables_to_latex_rs_type.ipynb) is used to generate results about research type classification. 

## RQ1 - Type of Architectural Technical Debt

[ATD Types](https://github.com/armandossrecife/smsatd/tree/main/md/mytable_q1_updated.md) | [ATD Types before findings](https://github.com/armandossrecife/smsatd/tree/main/md/mytable_q1.md)

The following script [ATD types](https://github.com/armandossrecife/smsatd/tree/main/python/auxiliary/Convert_tables_to_latex_q1.ipynb) is used to generate results about ATD's type classification. 

## RQ2 - Measurement of ATD

[Measurement](https://github.com/armandossrecife/smsatd/tree/main/md/mytable_q2_distribution_detailed.md) 

The following script [Measurement](https://github.com/armandossrecife/smsatd/tree/main/python/auxiliary/Convert_tables_to_latex_q2.ipynb)  is used to generate results about ATD's measurement classification. 

## RQ3 - Monitoring of ATD

[Monitoring](https://github.com/armandossrecife/smsatd/tree/main/md/mytable_q3_distribution_detailed.md) 

The following script [Monitoring](https://github.com/armandossrecife/smsatd/tree/main/python/auxiliary/Convert_tables_to_latex_q3.ipynb)  is used to generate results about ATD's monitoring classification. 

## RQ4 - Tools and Methods to Identify ATD

[Tools](https://github.com/armandossrecife/smsatd/tree/main/md/mytable_q4_tools_and_other_distribution_detailed.md) | [Tools with more features](https://github.com/armandossrecife/smsatd/tree/main/md/mytable_q4_tools_and_other_distribution_detailed_new_features.md) | [Methods](https://github.com/armandossrecife/smsatd/tree/main/md/mytable_q4_methods_detailed.md) | [Methods and SPs](https://github.com/armandossrecife/smsatd/tree/main/md/mytable_q4_methods_detailed_with_sp.md)

The following scripts [Tools and Methods](https://github.com/armandossrecife/smsatd/tree/main/python/auxiliary/Convert_tables_to_latex_q4.ipynb) are used to generate ATD's tools and ATD's method classification results. 

WordCloud of methods [methods](https://github.com/armandossrecife/smsatd/blob/main/images/atdmethods.png)

## RQ5 - Calculate the Cost of ATD item

[Calculate cost of ATD](https://github.com/armandossrecife/smsatd/tree/main/md/mytable_q5_distribution_detailed.md) 

The following script [Cost of ATD](https://github.com/armandossrecife/smsatd/tree/main/python/auxiliary/Convert_tables_to_latex_q5.ipynb) is used to generate results about how to calculate ATD item cost
