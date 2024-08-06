# CSV to PostgreSQL Data Insertion

This project provides a Python script that reads multiple CSV files and inserts their data into corresponding tables in a PostgreSQL database using SQLAlchemy and pandas. The script is designed to automate the process of data ingestion for Olympic-related datasets.

## Requirements

Make sure you have the following Python packages installed:

- `pandas`
- `sqlalchemy`
- `psycopg2` (or `psycopg2-binary`)

You can install these packages using pip:

```bash
pip install pandas sqlalchemy psycopg2-binary
```

## Setup

### Database Configuration

Update the PostgreSQL connection details in the script:

- `postgres_user`: Your PostgreSQL username
- `postgres_password`: Your PostgreSQL password
- `postgres_host`: The host where your PostgreSQL database is running (default: localhost)
- `postgres_port`: The port number (default: 5432)
- `postgres_db`: The name of your PostgreSQL database

### CSV Files

Place the following CSV files in the same directory as the script (or update the file paths accordingly):

- `Olympic_Athlete_Bio.csv`
- `Olympic_Athlete_Event_Results.csv`
- `Olympic_Games_Medal_Tally.csv`
- `Olympic_Results.csv`
- `Olympics_Country.csv`
- `Olympics_Games.csv`

# Schema Configuration

This script allows you to configure the schema name for your database operations. By default, the schema name is set to `raw`.

## Usage

Run the script using Python:

```bash
python script_name.py

```

Replace script_name.py with the actual name of your script file.

The script will:

- Read each CSV file into a pandas DataFrame.
- Insert the DataFrame into the corresponding PostgreSQL table in the specified schema.
- Print a confirmation message for each file processed.

## Note

The if_exists='replace' parameter in the to_sql method will replace existing tables with the same name. You can change this to 'append' or 'fail' depending on your requirements.

Ensure that your PostgreSQL server is running before executing the script.

## License

This project is licensed under the MIT License. Feel free to modify and use it as per your needs.
