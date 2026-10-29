# Airline Dashboard Analysis

A data visualization portfolio project using **Tableau** and **Power BI** to explore passenger demographics, airport traffic, geographic distribution, and flight status.

The project uses the [Airline Dataset by I Am Sourav Banerjee on Kaggle](https://www.kaggle.com/datasets/iamsouravbanerjee/airline-dataset). The dashboards organize related questions into focused pages so readers can move from an overview to passenger, airport, and operational detail.

## Project objectives

- Understand the passenger mix by gender, age, and nationality.
- Compare passenger records across airports, countries, and continents.
- Explore the distribution of on-time, delayed, and cancelled statuses.
- Examine departure-date patterns and arrival-airport activity.
- Compare flight-status counts across demographic groups.

## Tools used

| Tool | Purpose |
|---|---|
| Tableau | Dashboard creation, calculated fields, and visual exploration |
| Power BI Desktop | Data modeling, DAX measures, and report creation |
| CSV dataset | Source data for both dashboard implementations |

## Dataset

The supplied CSV contains **98,619 records and 15 columns**, with 98,619 distinct passenger IDs.

| Category | Fields |
|---|---|
| Passenger | Passenger ID, First Name, Last Name, Gender, Age, Nationality |
| Airport and geography | Airport Name, Airport Country Code, Country Name, Airport Continent, Continents, Arrival Airport |
| Operations | Departure Date, Pilot Name, Flight Status |

**Source:** [Kaggle — Airline Dataset](https://www.kaggle.com/datasets/iamsouravbanerjee/airline-dataset)  
**Dataset credit:** I Am Sourav Banerjee

Refer to the original dataset page for its description and applicable usage terms.

## Dashboard coverage

### Tableau

| Page | Main focus | Questions explored |
|---|---|---|
| Executive Overview | Summary KPIs | What is the overall passenger, airport, country, pilot, age, and status profile? |
| Passenger Analysis | Gender, age groups, nationalities, and top nationalities | Which passenger groups account for the most records? |
| Airport Analysis | Airport traffic, countries, continents, and airport country codes | Where is passenger activity concentrated? |
| Flight Operations | Status distribution and daily, monthly, and weekday patterns | How do recorded travel activity and statuses vary over time? |

### Power BI

| Page | Main focus | Questions explored |
|---|---|---|
| Route Analysis | Arrival-airport rankings and airport–arrival combinations | Which arrival airports and combinations have the most passenger records? |
| Geographical Analysis | Country-level passenger distribution and airport locations | How is passenger activity distributed geographically? |
| Demographic Insights | Flight status by age group and gender | How do status counts compare across demographic groups? |

The repository currently presents these **four Tableau pages and three Power BI pages**. The broader nine-section outline is a planning framework, rather than a claim that nine dashboards have been implemented.

## Dashboard previews

### Tableau — Executive Overview

![Tableau Executive Overview](<screenshots/tableau/01.Executive Overview.png>)

<details>
<summary>View the other Tableau dashboards</summary>

### Passenger Analysis

![Tableau Passenger Analysis](<screenshots/tableau/02.Passenger Analysis.png>)

### Airport Analysis

![Tableau Airport Analysis](<screenshots/tableau/03.Airport Analysis.png>)

### Flight Operations

![Tableau Flight Operations](<screenshots/tableau/04.Flight Operations.png>)

</details>

### Power BI — Route Analysis

![Power BI Route Analysis](<screenshots/power-bi/01.Route Analysis.png>)

<details>
<summary>View the other Power BI pages</summary>

### Geographical Analysis

![Power BI Geographical Analysis](<screenshots/power-bi/02.Geographical Analysis.png>)

### Demographic Insights

![Power BI Demographic Insights](<screenshots/power-bi/03.Demographic Insights.png>)

</details>

## Dataset status summary

The following figures were calculated from the supplied CSV, before applying dashboard filters:

| Recorded status | Passenger records | Share of records |
|---|---:|---:|
| On Time | 32,846 | 33.31% |
| Delayed | 32,831 | 33.29% |
| Cancelled | 32,942 | 33.40% |
| **Total** | **98,619** | **100.00%** |

The three status categories are almost evenly represented. These are descriptive results for this dataset, rather than estimates of real-world airline performance.

## Metric definitions and interpretation

- **Passenger count:** count of passenger records; passenger IDs are unique in the supplied CSV.
- **Airport, country, and pilot totals:** distinct values in their respective fields, subject to data cleaning and dashboard filters.
- **Average passenger age:** average of the Age field within the active selection.
- **Status percentage:** records in a status category divided by all records in the relevant selection.
- **Time trends:** passenger-record counts grouped by Departure Date, month, or weekday.

**Flight-count limitation:** the dataset does not provide a flight ID. Counting Passenger ID or Flight Status does not establish the number of distinct flights. Existing dashboard labels such as “Total Flights” should therefore be interpreted as record counts unless a separate flight-level definition is validated.

**Geographic and route interpretation:** passenger nationality and airport country describe different attributes. Confirm that Airport Name represents the departure airport before treating its combination with Arrival Airport as an origin–destination route.

**Pilot interpretation:** passenger-record counts grouped by Pilot Name do not establish the number of flights operated or support a causal assessment of pilot performance.

## Repository contents

| Location | Contents |
|---|---|
| [data/](data/) | Source CSV |
| [power-bi/](power-bi/) | Power BI report and PDF export |
| [tableau/](tableau/) | Tableau packaged workbook and PDF export |
| [screenshots/power-bi/](screenshots/power-bi/) | Screenshots of the three Power BI pages |
| [screenshots/tableau/](screenshots/tableau/) | Screenshots of the four Tableau dashboards |

### Open the dashboards

| Format | File |
|---|---|
| Power BI report | [Download PBIX](<power-bi/power bi dashboard.pbix>) |
| Power BI PDF | [View PDF](<power-bi/dashboard pdf.pdf>) |
| Tableau workbook | [Download TWBX](<tableau/tableau dashboard.twbx>) |
| Tableau PDF | [View PDF](<tableau/dashboard pdf.pdf>) |
| Source dataset | [View CSV](<data/Airline Dataset.csv>) |

## How to use this project

1. Review the screenshots above or open the PDF exports for a quick walkthrough.
2. Download the repository to explore the editable dashboard files.
3. Open the PBIX file in Power BI Desktop.
4. Open the TWBX file in a compatible Tableau application.
5. If refreshing requires a source connection, update the CSV path to your local copy of `data/Airline Dataset.csv`.
6. Use the available filters and tooltips to inspect particular groups. Filtered results may differ from the full-dataset totals above.

GitHub provides static previews and downloads; interactive exploration requires opening the dashboard files in the appropriate application.
