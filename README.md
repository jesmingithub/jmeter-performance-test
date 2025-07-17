# JMeter Load Test Example

## Overview
This repository contains a simple JMeter load test plan targeting the public API [jsonplaceholder.typicode.com](https://jsonplaceholder.typicode.com/).

The test plan sends GET requests to the `/posts` endpoint with different `userId` query parameters sourced from a CSV file.

## Included Files
- `load_test.jmx` — JMeter test plan file
- `user_data.csv` — CSV file with `userId` values for parameterization
- `README.md` — This documentation file
- Blazemeter Reports

## Prerequisites
- [Apache JMeter](https://jmeter.apache.org/) installed on your machine.
- BlazeMeter account
- Basic familiarity with running JMeter test plans.

## How to Run Locally
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

---

## How to Run This Test on BlazeMeter

### 1. Log in to BlazeMeter
Visit [https://a.blazemeter.com](https://a.blazemeter.com) and sign in with your account.

### 2. Create a New Test
Click **Create Test** → **Performance Test**.

### 3. Upload Test Files
Upload the following files in the **Test Script** section:
- `load_test.jmx`
- `user_data.csv`

Make sure they are both selected and uploaded before proceeding.

### 4. Configure Test Parameters
Adjust the following based on your test goals:
- Number of Virtual Users
- Ramp-Up Time
- Test Duration
- Geo-locations (optional)

### 5. Start the Test
Click the **Run Test** button to execute your test plan in the cloud.

### 6. Monitor and Analyze Results
Use the built-in BlazeMeter dashboard to analyze:
- Response times
- Throughput
- Error rates
- Percentile distributions

You can view detailed reports via the **Summary**, **Timeline**, and **Errors** tabs.

### 7. Export Reports
After the test:
- Click **Download Report**
- Export in **PDF**, **CSV**, or **JSON** format for documentation


