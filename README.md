# Russia-Ukraine Conflict: Data Pipeline Project

This project demonstrates a complete ETL (Extract Transform and Load) pipeline build using Kobo toolbox(Data collection and validation), Python , PostgreSQL.
This is a full-stack data engineering + analytics project that mirrors real-world scenarios(War between Russia and Ukraine).
it extracts real-time data about the Russia-Ukraine conflict, cleans and transforms it using Python, and loads it into a PostgreSQL database for further analysis.

**Poject Overview:**
The pipeline performs the following:

1. **Extract** data from KoboToolbox (CSV endpoint)
2. **Transform** the data  using pandas :
    - Rename columns for consistency.
    - Calculate total casualties.
    - Parse and convert data formats.
3. **Load** the cleaned data into a Postgre database.
4. (Optional) use **Power Bi or Tableau** for reporting and visualization.

**Project Structure**

bash
Russia-Ukraine-Conflict/
|--.env        #Stores environment variables
|--.gitignore  # Git exclusions
|--pipeline.py #Python Script for the ETL pipeline
|--README.md   #Project Overview and setup guide 
|--requirements.txt Python Libraries 

**Technologies Used**

- **Python 3.10**
- **Pandas** - data cleaning
- **Requests** - data fetching
- **psycopg2** - PostgreSQL connection
- **PostgreSQL** - database
- **KoboToolbox** - data source
- **dotenv** - for environment variable management 

**Environment Variables**

Create an .env file in the root directory with the following structure:

--ini
KOBO_USERNAME= your _kobo_username
KOBO_PASSWORD= your _kobo_password
PG_HOST= your _postgres_host
PG_DATABASE=your _database_name
PG_USER=your postgres_user
PG_PASSWORD= your _postgres_password
PG_PORT=5432

**How to run the pipeline**
1) Install dependencies 
pip install -r requirements.txt

2) Add your .env file with credentials as shown above 

3) Run the Script:
python pipeline.py

Key Metrics Calculated
Total Casualties = Casualties + Injured + Captured
Dates converted for time based analysis
Cleaned and standardized column names

**Dashboard (Optional)**
You can connect the PostgreSQL database to Power BI, Tableau, or any BI tool to build an interactive dashboard showing:

- Total Casualties over time 
- Casualties by region
- occupied territories distribution

**Contributing** 
If you would like to suggest improvements or contributions, feel free to fork the repo and open a pull request. 

**License** 
This project is open source and available under the MIT License 

**Acknowledgements**
Kobo toolbox : for making humanitarian data collection simple 

All open source developers whose tools made this project possible 

Project By MakhouTech

