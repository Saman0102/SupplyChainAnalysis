# Avocado Toast Supply Chain Analysis

This project performs a supply chain analysis of the key ingredients used in a standard avocado toast recipe. By leveraging the Open Food Facts database, the analysis identifies the primary countries of origin for ingredients sold in the United Kingdom, illustrating the global complexity behind a simple breakfast dish.

# The Recipe

The analysis focuses on three critical components of avocado toast:

    Avocado

    Extra Virgin Olive Oil

    Sourdough Bread

# Dataset Overview

The project utilizes data from Open Food Facts, an open-source database of food products from around the world.
Data Files

    CSV Files: avocado.csv, olive_oil.csv, sourdough.csv — Contains product names, origin tags, and categories.

    TXT Files: relevant_[ingredient]_categories.txt — Contains specific category tags (e.g., "fruits," "vegetables," "fruit-based oils") used to filter the main datasets for relevant entries.

# Methodology

The analysis follows a strict data cleaning and filtering pipeline:

    Geographic Filtering: The data is restricted to products available in the United Kingdom.

    Category Validation: Entries are filtered using ingredient-specific tags to ensure that irrelevant products (e.g., avocado-flavored chips) are excluded.

    Missing Value Handling: Rows missing critical information in origins or categories_tags are dropped to ensure accuracy.

    Mode Analysis: The script identifies the most frequent country of origin for each ingredient by calculating the mode of the origins_tags column.

# Key Findings

Based on the analysis of products sold in the UK, the top origins for the ingredients are:  
| Ingredient | Primary Origin | 
| :--- | :---: | 
| Avocado | Peru |  
| Olive Oil | Greece |  
| Sourdough | United Kingdom |

# Requirements

To run the notebook, you need:

    Python 3.x

    Pandas

# How to Run

    Ensure the data/ folder contains the necessary .csv and .txt files.

    Run the top_origin function within the provided Jupyter Notebook.

    The function returns the most common origin string for each specific ingredient.
