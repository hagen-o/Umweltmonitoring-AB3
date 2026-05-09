
CCGG Flask CO2 Data Tutorial  
Getting Started with Jupyter Notebooks and Real Atmospheric Data

This tutorial is designed for beginners, especially those who are working with environmental data in Python for the first time. It will help you get set up to work with CCGG flask CO2 mole fraction data using Python and Jupyter Notebooks.

---

STEP 1: Download the CO2 Flask Data and Example Notebook

1. Go to the NOAA GML data site (https://gml.noaa.gov/data/dataset.php?item=mlo-co2-flask) and download the CO2 flask measurements for Mauna Loa, Hawaii.

2. Choose a data format:
   - netCDF (.nc) — more complex, good for automated processing
   - ASCII text (.txt) — easier to open and view manually

   This tutorial shows how to work with both formats.

3. Download the example Jupyter Notebook file:
   - ccgg_co2_flask_example.ipynb

4. Save all files (data + notebook) in a folder where you can easily find them later, such as your Desktop or Documents folder.

---

STEP 2: Install Anaconda to Use Python and Jupyter Notebooks

Anaconda is a free software package that includes Python, Jupyter Notebook, and other useful tools. It’s a simple way for beginners to get started with coding and data analysis.

2a. Download Anaconda:
   - Visit the Anaconda download website (https://www.anaconda.com/download).
   - Skip the registration step - it is unnecessary for our purpose. 
   - Download the Distribution Graphical Installer for your system (Windows, macOS, or Linux).

2b. Install Anaconda:
   - Follow the installation instructions for your operating system (https://www.anaconda.com/docs/getting-started/anaconda/install).
   
   - If you don’t have permission to install software (e.g., on a work or school computer), ask your IT department for help.

2c. Launch Jupyter Notebook using Anaconda Navigator:
   - Open the Anaconda Navigator application.
   - Click "Launch" under the "Jupyter Notebook" tile.
   - This will open a new tab in your default web browser showing your computer’s files.

---

STEP 3: Open the Example Notebook

- Use the file browser in Jupyter to find the folder where you saved the notebook file.
- Click on the file "ccgg_co2_flask_example.ipynb" to open it.
- The notebook will open in a new browser tab.

---

STEP 4: Select the Python Kernel

- Look in the upper-right corner of the notebook window.
- Make sure the selected kernel is a Python environment (e.g., "Python 3").
- The kernel is what runs your code and displays the results in the notebook.

---

STEP 5: Download NOAA GML Curve Fitting Tools 

This tutorial uses two Python files developed by NOAA GML to perform atmospheric data filtering and curve fitting, based on methods from Thoning et al. (1989). 
These tools must be downloaded manually.

5a. Go to the NOAA FTP site for the CCGCRV Python tools:
   https://gml.noaa.gov/aftp/user/thoning/ccgcrv/

5b. Download the zip file: "ccg_filter.zip" and unpack it. We will need these two Python files:
   - ccg_filter.py
   - ccg_dates.py
   Note: You do *not* need to use the file `ccgcrv.py` — that one is only needed for command-line use, not in Jupyter notebooks.

5c. Move both files to the same directory as your Jupyter Notebook (.ipynb) file.

These files are standalone Python modules and do not require installation. Once saved in the correct location, you can import them in your notebook using:

    import ccg_filter
    import ccg_dates

---

Now you're set up to work with real atmospheric CO2 data. In the notebook, you'll:

* Load and read CO2 flask data
* Work with both ASCII and netCDF file formats
* Filter and manipulate datasets
* Create simple graphs to visualize CO2 trends
* Apply NOAA GML's curve-fitting methods to separate seasonal signals from long-term trends