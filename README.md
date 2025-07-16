# JMeter Load Test Example

## Overview
This repository contains a simple JMeter load test plan targeting the public API [jsonplaceholder.typicode.com](https://jsonplaceholder.typicode.com/).

The test plan sends GET requests to the `/posts` endpoint with different `userId` query parameters sourced from a CSV file.

## Included Files
- `load_test.jmx` — JMeter test plan file
- `user_data.csv` — CSV file with `userId` values for parameterization
- `README.md` — This documentation file

## Prerequisites
- [Apache JMeter](https://jmeter.apache.org/) installed on your machine.
- Basic familiarity with running JMeter test plans.

## How to Run
1. Clone this repository or download the files.
2. Open `load_test.jmx` in JMeter GUI.
3. Ensure the CSV file `user_data.csv` is in the same directory as the `.jmx` file or update the path in CSV Data Set Config.
4. Run the test plan.
5. View results using listeners like 'View Results Tree' or 'Aggregate Report'.

## Test Configuration
- **Threads (Users):** 5  
- **Ramp-Up Period:** 2 seconds  
- **Loop Count:** 2 (each user sends 2 requests)  
- **Delay:** 1 second between each request  
- **Assertions:** Checks if response contains `userId`

## Customization
- Modify `user_data.csv` to test with different user IDs or data.
- Adjust the Thread Group settings in `load_test.jmx` for different load profiles.
- Add or modify assertions as needed.

## Notes
- This is a beginner-friendly example for learning JMeter load testing.
- The target API is a public fake API for testing purposes.
