
## Project Overview
This project is a DBT (Data Build Tool) analytics pipeline for BigQuery, designed to transform and model NYC taxi trip data. It includes staging, core, and seed models, as well as macros and tests for data quality and business logic.

## Folder Structure
- `models/` — DBT models (SQL files) organized by domain (core, staging)
- `seeds/` — CSV seed files for static reference data
- `macros/` — Custom DBT macros
- `snapshots/` — Snapshot definitions for slowly changing dimensions
- `analyses/` — Ad-hoc analysis SQL files
- `config/` — Service account key files for BigQuery authentication
- `dbt_project.yml` — Main DBT project configuration
- `profiles.yml` — DBT profile for BigQuery connection

## Setup Instructions
1. **Install Python & DBT**
   - Run `bin\windows\install_python_venv.bat` to create a virtual environment.
   - Run `bin\windows\install_python_libraries.bat` to install required Python packages.
   - Run `bin\windows\install_dbt_libraries.bat` to install DBT and dependencies.

2. **Configure BigQuery Access**
   - Place your Google Cloud service account key file in the `config/` folder.
   - Update `profiles.yml` with your project, dataset, and keyfile path.

3. **Install DBT Packages**
   - Run `dbt deps` to install dependencies listed in `packages.yml`.

## Usage
1. **Activate the Python environment**
   - `venv\Scripts\activate` (Windows)
2. **Run DBT commands**
   - `dbt run` — Build models
   - `dbt test` — Run tests
   - `dbt seed` — Load seed data
   - `dbt docs generate && dbt docs serve` — Generate and view documentation

## Configuration
- **BigQuery Project:** Set in `profiles.yml` under `project:`
- **Dataset:** Set in `profiles.yml` under `dataset:`
- **Service Account:** Set in `profiles.yml` under `keyfile:`

## References
- [DBT Documentation](https://docs.getdbt.com/)
- [BigQuery Documentation](https://cloud.google.com/bigquery/docs)