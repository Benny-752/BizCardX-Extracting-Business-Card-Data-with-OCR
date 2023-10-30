# BizCardX-Extracting-Business-Card-Data-with-OCR
![BizCardX](![BizCardX](https://github.com/Benny-752/BizCardX-Extracting-Business-Card-Data-with-OCR/assets/81459105/acf4e86e-2b53-4b7a-a48f-12f9698907b9))

## Introduction
Manually inputting business card data into a database can be time-consuming and error-prone. To streamline this process, developers can automate the extraction of information from business cards and store it efficiently using optical character recognition (OCR) in combination with databases. EasyOCR, a robust OCR library, simplifies the task of extracting text from images. This open-source Python package employs deep learning models to accurately identify and extract text in various languages. By integrating EasyOCR with a MySQL database, developers can expedite the capture of business card data and maintain it in an organized structure.

## Tools and Requirements
### Tools to Install
- Visual Studio Code
- Jupyter Notebook
- Python 3.11.0 or higher
- MySQL

### Required Libraries to Install
```bash
pip install pandas easyocr numpy Pillow opencv-python-headless os re sqlalchemy mysql-connector-python streamlit
```

### Import Libraries
```python
# Scanning library
import easyocr  # Optical Character Recognition
import numpy as np
from PIL import Image, ImageDraw
import cv2
import os
import re

# Data frame libraries
import pandas as pd

# Database Library
import sqlalchemy
import mysql.connector
from sqlalchemy import create_engine, inspect

# Dashboard library
import streamlit as st
```

## ETL Process
1. **Extract Data**
   Extract relevant information from business cards using the EasyOCR library.

2. **Process and Transform the Data**
   After the extraction process, process the extracted data based on Company name, Card Holder, Designation, Mobile Number, Email, Website, Area, City, State, and Pincode, converting it into a data frame.

3. **Load Data**
   Following the transformation process, store the data in the MySQL database.
