# Datathon_HealthCare-Analysis
This project aims to analyze hospital discharge volumes, financial performance, illness severity impacts, and geographic trends to uncover patterns in patient care costs, hospital efficiency, and patient outcomes across New York State from 2009 to 2024.

## Project Objective
Our primary objective is to uncover actionable insights into hospital performance across New York State by:
1. Analyzing hospital discharge volume trends
2. Examining the relationship between illness severity and healthcare costs
3. Identifying hospitals with exceptional financial performance (both profitable and unprofitable)
4. Mapping geographic differences in patient care and financial metrics
5. Ranking hospitals based on custom metrics such as profitability and complexity handling

## Datathon Submission Presentation
https://pamareel.github.io/hospital_efficiency_analysis
https://colab.research.google.com/drive/155yzAS4qs9O_Id6PWZ-5Gf49pNSo56Q4?usp=sharing#scrollTo=tBS4fIY-muB1

## Analysis Scope
Our analysis is structured into three main sections:

### 1. Overall Hospital Activity & Volume Trends
- Total discharges by hospital and by year
- Trends in discharges over time, broken down by medical vs. surgical cases and illness severity
- Identification of hospitals with unstable discharge patterns (i.e., large fluctuations)
- Geographic mapping of hospitals categorized by discharge volume

### 2. Hospital Charges, Costs, and Profitability
- Trends in mean costs and mean charges over time
- Ranking hospitals by mean charges and costs
- Identifying hospitals operating at a financial loss vs those achieving high profit margins

### 3. Impact of Diagnosis Type and Severity of Illness
- Distribution of discharges by APR DRG Code
- Distribution of discharges by Severity of Illness (Minor, Moderate, Major, Extreme)
- Analyzing whether costs and charges increase with severity
- Visualizing mean charge and cost by severity level
- Mapping hospitals by severity-weighted discharge scores

## Methodology
We followed a structured analysis workflow:

### Data Preparation:
1. Cleaned and standardized hospital facility names
2. Handled missing value by filling the according to the information from data dictionary
3. Aggregated duplicate rows by recalculated mean and median costs and charges
5. Generated calculated fields including:
Profitability = (Mean Charge - Mean Cost) / Mean Charge
Mean Profit = (Mean Charge - Mean Cost)
Severity Weighted Score = (1 × Minor Discharges + 2 × Moderate Discharges + 3 × Major Discharges + 4 × Extreme Discharges) / Total Discharges
6. Merge external facility location data with latitude and lontitude

### Metric Development:
1. Profitability metric used to rank hospitals' financial efficiency
2. Severity Weighted Score metric used to identify hospitals specialized in handling complex patients
3. Discharge metric to detect volume volatility

## Key Findings:
1. Overall hospital discharge volumes have decreased slightly over time, especially for Minor and Moderate cases
2. Higher severity of illness is strongly correlated with higher mean charges and mean costs
3. Several hospitals exhibit unstable year-to-year discharge volumes
4. Profitability varies widely, with a set of hospitals consistently operating at a financial loss

## Tools Used:
1. Python for data preperation
2. Tableau for visualization and dashboard building


