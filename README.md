# Welcome to Pokémon PowerRanker
***

## Task
Data Engineer (Python, SQL) – Test Task

Build a data pipeline that:
1. Collects information about Pokémon.
2. Identifies the most effective Pokémon companion across all generations (ranked from best to worst).
3. Exports the ranked data to Google Spreadsheets for dashboard creation in Google Looker Studio.

## Description
This project retrieves and processes Pokémon data from a public CSV source to:

1. Analyze each Pokémon's battle strength using custom logic.
2. Rank all Pokémon from strongest to weakest.
3. Visualize and check for data quality issues (e.g. missing values).
4. Export the final ranked dataset to a Google Spreadsheet for reporting and visualization.

The solution was implemented in Python and includes:
- Data loading and cleaning data with custom `get_data()` method
- Strength calculation and ranking witg custom `strength_rank()` method
- Visualization of null values
- Export to Google Sheets using the Google Sheets API with custom `save_to_gsheets()` method

### File structure
.
├── README.md
├── pokemon_ranker.py
├── your-credentials-file.json
├── requirements.txt

## Installation

1. Clone this repository or download the files.
2. Install required Python libraries:
```pip install pandas gspread google-auth matplotlib seaborn```
3. Place your Google service account credentials JSON file in the project folder.

## Usage
Open `best_pokemon.ipynb­` file with jupyter notebook

### Configuration:
Before running, update the following variables in the script:
- credentials_path: Path to your service account JSON file
- spreadsheet_id: Your target Google Sheets ID
- worksheet_n: Name of the worksheet to store ranked data

### Pokémon Strength Formula
Poke_strength = (ATK - DEF) * 0.8 + (SP_ATK - SP_DEF) * 0.2

### Output Example
Top 5 Ranked Pokémon:
1. Glastrier
2. Deoxys
3. Pheromosa
4. Deoxys (Alt Form)
5. Aegislash

## Visualization

The project generates a heatmap using Seaborn to highlight any missing values before proceeding with calculations.

## Google Sheets Integration

The final ranked data is exported to a Google Spreadsheet for dashboard creation in Google Looker Studio, allowing dynamic filtering and visualization by users.

## Author

Pēteris Veits
