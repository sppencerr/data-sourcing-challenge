# data-sourcing-challenge
# Space Weather Prediction – Data Sourcing Challenge

This project was built to help improve predictions around space weather... specifically geomagnetic storms that are triggered by massive solar events called Coronal Mass Ejections (CMEs). These storms can affect satellites, GPS systems, and even parts of our power grid, so being able to predict them earlier is a pretty big deal.

The whole point was to pull CME and GST data from NASA's public API, clean it up, connect the dots between the events, and prep it for use.

---

## What this project does

- Pulled real CME and GST data from NASA's DONKI API (from 2013 through 2024)
- Cleaned the raw JSON data and kept the parts that matter
- Matched CMEs to their related GSTs
- Calculated the time it usually takes between a CME and the resulting GST
- Exported a clean dataset to CSV for future analysis or modeling

---

## Tools used

- Python + Jupyter Notebook
- pandas
- requests
- dotenv (for securely loading the API key)

---

## Why it matters

Geomagnetic storms aren’t just cool science — they have real-world impacts. Better data helps with:

- Avoiding signal outages
- Protecting satellite operations
- Making power grids more resilient

Getting this data cleaned and connected is a first step toward training smarter models that can make earlier, more accurate predictions.

---

## Project structure

- `retrieve_data.ipynb`: The main notebook that does all the data pulling, cleaning, and merging
- `cme_gst_merged_data.csv`: Final dataset (clean and ready for ML use)
- `.env`: Your personal API key lives here (not included in the repo)

---

## How to run this

1. Clone the repo
2. Create a `.env` file and add your NASA API key like this:  
   `NASA_API_KEY=your_key_here`
3. Open the notebook and run through the steps
4. Final output will be saved as a CSV