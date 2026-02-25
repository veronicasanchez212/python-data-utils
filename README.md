# python-data-utils
Practical Python utilities for data processing, validation, and small automation tasks, with clear structure and documentation.
# Python Data Utilities

A collection of practical Python utilities for common data processing, validation, and automation tasks.

This repository focuses on clean, readable code and simple examples that demonstrate real-world usage.

---

## Project Structure

- data_cleaner.py  
  Functions for cleaning and normalizing text-based data.

- file_utils.py  
  Helpers for basic file handling and validation.

- examples/  
  Small scripts showing how the utilities can be used.

---

## Usage

Clone the repository:

git clone https://github.com/veronicasanchez212/python-data-utils.git
cd python-data-utils

Run an example script:

python examples/example_clean.py

---

## Requirements

Python 3.x  
No external dependencies.

---

## License

MIT License
data_cleaner.py
file_utils.py
examples/example_clean.py
examples/example_file_utils.py
requirements.txt
"""
Simple data cleaning utilities.
"""

import re


def normalize_text(text: str) -> str:
    """
    Convert text to lowercase and normalize whitespace.
    """
    return re.sub(r"\s+", " ", text.strip().lower())
"""
Basic file utility functions.
"""

import os


def file_exists(path: str) -> bool:
    """
    Check whether a file exists.
    """
    return os.path.exists(path)


def read_lines(path: str) -> list[str]:
    """
    Read all lines from a text file.
    """
    with open(path, "r", encoding="utf-8") as file:
        return file.read().splitlines()
from data_cleaner import normalize_text

text = "   Sample TEXT for Cleaning   "
print("Original:", text)
print("Cleaned:", normalize_text(text))
from file_utils import file_exists, read_lines

path = "README.md"

print("File exists:", file_exists(path))
if file_exists(path):
    print("Number of lines:", len(read_lines(path)))
# No external dependencies
