# 🧪 JMeter Performance Testing

This repository contains a JMeter performance test plan and a GitHub Actions CI/CD pipeline to automate load testing.

## 📁 Project Structure

JMeter-Performance-Testing/
├── .github/
│ └── workflows/
│ └── jmeter.yml # GitHub Actions workflow for automated test execution
├── Coop Interview Preparation Test Plan.jmx # JMeter test plan file
├── README.md # Project documentation


## 🚀 How It Works

This project uses **Apache JMeter** to execute a performance test defined in the `.jmx` file. The test is automatically run using **GitHub Actions** whenever changes are pushed to the `main` branch or a pull request is created.

## 📄 Test Plan

- **File:** `JMeter-Performance-Testing- Test -Plan.jmx`
- Designed to simulate user activity for Coop system performance evaluation.
- Can be edited or enhanced using the [Apache JMeter GUI](https://jmeter.apache.org/).

## ⚙️ CI/CD Pipeline

- **File:** `.github/workflows/jmeter.yml`
- **Runner:** `ubuntu-latest`
- **Steps:**
  - Checkout the code
  - Install Apache JMeter
  - Run the `.jmx` test in non-GUI mode
  - Save results as `.jtl` and generate an HTML report
  - Upload the HTML report as a downloadable artifact

## 🧪 How to Run Locally

1. **Install JMeter:** [Download JMeter](https://jmeter.apache.org/download_jmeter.cgi)
2. **Run from CLI:**
   ```bash
   jmeter -n -t "JMeter-Performance-Testing- Test -Plan.jmx" -l results.jtl -e -o results

3. View the Report:

    Open results/index.html in your browser.
