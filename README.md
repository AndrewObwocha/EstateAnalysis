# Real Estate Data Analysis Notebook

## Overview

This Jupyter Notebook (`estate.ipynb`) demonstrates basic data loading, processing, and analysis for a simplified real estate dataset spread across multiple text files. It reads information about property ownership, regional price indexes, and individual property details, then calculates and presents a summary report showing average area, average price, and the number of available properties per locality.

The primary goal is to showcase reading data from files, manipulating basic data structures (dictionaries and lists), performing simple calculations, and formatting output in Python within a notebook environment.

## Input Data Files (Required)

This notebook **requires** the following text files to be present in the **same directory** as `estate.ipynb`:

1.  **`ownership.txt`**: Expected format (comma-separated, with header):
    ```
    OwnerID,CompanyName,YearEstablished
    1,Example Corp,2005
    ...
    ```
2.  **`price_index.txt`**: Expected format (comma-separated, with header):
    ```
    Locality,AvgPricePerSqft
    Downtown,408.3
    ...
    ```
3.  **`properties.txt`**: Expected format (comma-separated, with header):
    ```
    Locality,Rooms,Area,OwnerID
    Downtown,3,1200.5,1
    Downtown,2,950.0,0 # OwnerID 0 signifies 'available'
    ...
    ```

*Failure to provide these files in the correct format and location will result in errors.*

## Features

*   Reads and parses data from three separate comma-separated text files.
*   Stores data efficiently using Python dictionaries and lists.
*   Calculates the average property area for each locality.
*   Calculates the estimated average property price for each locality based on area and price index.
*   Counts the number of "available" properties (defined as OwnerID=0) for each locality.
*   Sorts the results primarily by the number of available properties (descending) and secondarily by locality name (ascending).
*   Prints a formatted summary table of the calculated statistics directly in the notebook output.

## Requirements

*   Python 3.x
*   A Jupyter Notebook environment (like Jupyter Lab, Jupyter Notebook, Google Colab, or VS Code with the Jupyter extension) capable of running `.ipynb` files.
*   The required input data files (`ownership.txt`, `price_index.txt`, `properties.txt`).

## How to Use

1.  **Place Files:** Ensure `estate.ipynb`, `ownership.txt`, `price_index.txt`, and `properties.txt` are all in the same directory.
2.  **Open Notebook:** Launch your Jupyter environment and open `estate.ipynb`.
3.  **Run Cells:** Execute the cells in the notebook sequentially (e.g., using "Run All" or running them one by one from top to bottom).
4.  **View Output:** The final cell will execute the `main()` function and print the formatted summary table as its output.

## Output Example

The notebook generates a text-based table

## Code Structure

The notebook is organized into Python functions within code cells:

*   `ownershipFileReader()`: Reads `ownership.txt`.
*   `priceIndexFileReader()`: Reads `price_index.txt`.
*   `propertyFileReader()`: Reads `properties.txt`.
*   `averageArea()`: Calculates average area per locality.
*   `averagePrice()`: Calculates average price per locality.
*   `numOfAvailableProperties()`: Counts available properties per locality.
*   `main()`: Orchestrates the reading, calculation, sorting, and printing steps.

## License

MIT License

## Author

Andrew Obwocha
