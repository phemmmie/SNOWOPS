# ETL Pipeline Project

## Overview
This project creates and populates a `customers` table in Snowflake as part of an ETL pipeline, using Jenkins for CI/CD and storing SQL scripts in GitHub.

## Directory Structure
- **sql/**: Contains SQL scripts for creating tables and inserting data.
- **jenkins/**: Contains Jenkins pipeline configuration.
- **config/**: Holds database and environment configurations.
- **tests/**: SQL scripts for integration and data validation testing.
- **docs/**: Project documentation.
- **logs/**: Runtime logs.

## Usage
1. Place your Snowflake credentials in Jenkins.
2. Trigger the Jenkins pipeline to deploy the SQL scripts.

## Authors
- Maintainer: Sobakin
