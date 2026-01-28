# Weather Data Analysis for Romania

This is an educational project created as part of my learning journey, aimed at applying what I’ve learned about data processing and visualization.  
The project collects weather data for Romania using a public weather API, covering the last 6 days, today, and the forecast for the next two days (9 days in total), based on the free plan.  

After collecting the data, the project cleans, organizes, and analyzes it, then automatically generates a PDF weather bulletin. The bulletin includes charts and short written analyses for weather conditions across Romania and its counties.  
The report contains information about temperature, precipitation, cloud coverage, humidity, snowfall, and wind, presented in a clear and accessible way.  

This project is intended for educational purposes and as a practical exercise in working with real-world data.

---

## Setup

- Python 3.10+
- Installing the required libraries:
    + All the libraries required for this project (pandas, matplotlib, reportlab, geopandas, etc.) are listed in the `requirements.txt` file.
    + In the same folder, there is a `.bat` file that can be run to automatically install all required libraries.
    + Alternatively, you can run: `py -m pip install -r requirements.txt`
    + If you are using Anaconda, these libraries can also be installed directly through Anaconda Navigator.
- Jupyter Notebook is required to run the notebooks:
    + Can be installed from the official website: https://jupyter.org/install
    + Or via Anaconda: https://www.anaconda.com/download
    + Alternatively, you can use VS Code with the recommended extensions (listed in `.vscode/extensions.json`)

---

## Data Sources

- All weather data is downloaded via a public API from https://www.weatherapi.com/
- Geographic data of Romania (county boundaries) is sourced from the OpenStreetMap database: https://osm-boundaries.com/

---

## API Key

Before running the code, you need to obtain an API key from https://www.weatherapi.com/ (free plan available).  
Your API key must be copied into the `.env` file before executing the notebooks.

---

## Running the Project

1. **Fetch Data**  
    - Notebook: `notebooks/01_fetch_data.ipynb`  
    - This notebook downloads weather data from the API and saves it in `data/raw/`.  
    - Must be run first, before any data processing.

2. **Process Data**  
    - Notebook: `notebooks/02_process_data.ipynb`  
    - This notebook reads the files from `data/raw/`, cleans and processes the data, and saves it in `data/processed/`.  
    - Must be run after `01_fetch_data.ipynb`.

3. **Data Analysis & PDF Generation**  
    - Notebook: `notebooks/03_data_analysis.ipynb`  
    - This notebook reads all processed data and generates a PDF weather bulletin containing charts and analyses for weather across Romania.  
    - Must be run after `02_process_data.ipynb`.

---

