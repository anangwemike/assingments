#### Python Assignment 1 on Sets

**Name:** Michael Anangwe Oluchiri 
**Date:** July 19, 2025  
**Topic:** Introduction to sets lab

## Objective
To demonstrate understanding of python set operations as well as the inclusion exclusion principle

## Files included
"Michael Anangwe sets assignment.ipynb" - python script with all the set operations
"Europe_and_EU.xlsx" – Dataset used for set analysis

## Tasks completed
1. Tackled all questions in the lab
2. Loaded datasets from Excel using "pandas".
3. Cleaned whitespace from country names.
4. Verified if EU countries are a subset of Europe.
5. Identified countries in Europe but not in EU.
6. Used the Inclusion-Exclusion Principle to count total unique countries.

## 🧪 Sample Code

```python
import pandas as pd

# Load data
europe = pd.read_excel("Europe_and_EU.xlsx", sheet_name="Europe")
eu = pd.read_excel("Europe_and_EU.xlsx", sheet_name="EU")

# Clean whitespace
europe["Country"] = europe["Country"].str.strip()
eu["Country"] = eu["Country"].str.strip()

# Check subset
is_subset = set(eu["Country"]).issubset(set(europe["Country"]))
print("EU is subset of Europe:", is_subset)


