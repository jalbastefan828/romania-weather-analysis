# Weather Data Analysis for Romania

This is an educational project created as part of my learning journey, with the goal of applying what I’ve learned about data processing and visualization.
The application uses a free weather API to collect data for Romania, covering the last 6 days, today, and forecast data for the next two days (9 days in total), based on the available free plan.
After collecting the data, the project cleans, organizes, and analyzes it, then automatically generates a PDF weather bulletin. The bulletin includes charts and short written analyses for weather conditions across Romania and individual counties.
The report contains information about temperature, precipitation, cloud coverage, humidity, snowfall, and wind, presented in a clear and accessible way.
This project is meant for educational purposes and as a practical exercise in working with real-world data.

----------------------------------------------------------------------------------------------------------------------

## Setup

- Python 3.10+
- Librariile din "requirements.txt":
        + se creează un fișier bash în același folder cu requirements.txt
        + in fișier se adaugă comanda: "py -m pip install -r requirements.txt"
        + se rulează fișierul bash pentru a instala librăriile
- Este nevoie de utilizarea programului JupyerNotebook:
        + se poate instala de pe site-ul oficial: https://jupyter.org/install
        + sau prin Anaconda: https://www.anaconda.com/download
        + alternativ, se poate folosi VS Code cu extensiile recomandate (listate în .vscode/extensions.json)

----------------------------------------------------------------------------------------------------------------------

## Sursa datelor

Toate datele despre vreme sunt descărcate prin intermediul unui API public de pe site-ul https://www.weatherapi.com/
Datele geografice ale Romaniei (granitele judetelor) au fost descarcate de pe OpenStreetMap database https://osm-boundaries.com/

----------------------------------------------------------------------------------------------------------------------

## API KEY

Înainte de rularea codului, trebuie să obțineți un API_KEY de pe site-ul https://www.weatherapi.com/ (plan gratuit disponibil)
API_KEY-ul vostru trebuie copiat și pus în fișierul .env

----------------------------------------------------------------------------------------------------------------------

## Rulare proiect
        1.Fetch Data
                - Notebook: notebooks/01_fetch_data.ipynb
                - Acest notebook descarcă datele meteo din API și le salvează în data/raw/.
                - Trebuie rulat primul, înainte de procesare.

        2.Process Data
                - Notebook: notebooks/02_process_data.ipynb
                - Acest notebook citește fișierele din data/raw/, le curăță și le salvează în data/processed/.
                - Trebuie rulat după 01_fetch_data.ipynb.

        3.Data analysis
                - Notebook: notebooks/03_data_analysis.ipynb
                - Acest notebook citeste toate datele procesate si genereaza un buletin meteo (in format PDF) ce contine grafice si analize despre vremea din Romania
                - Trebuie rulat după 02_process_data.ipynb.

----------------------------------------------------------------------------------------------------------------------


