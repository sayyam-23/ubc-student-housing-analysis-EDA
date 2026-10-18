# UBC Vancouver Student Housing: Capacity, Waitlists & Rental Costs

## Project Overview

As a UBC student, I wanted to better understand student housing pressures at UBC Vancouver. Has residence capacity kept pace with enrolment, and what do published waitlist milestones and nearby rental-market data reveal about the issue?

In this project, I used Python to explore public data from UBC and the Canada Mortgage and Housing Corporation (CMHC). I compared enrolment with reported residence capacity, examined published waitlist milestones, analyzed rental costs and vacancy rates near campus, and assessed planned housing expansion.

The goal was to understand what the data shows, where uncertainty remains, and what additional information would help explain student housing pressure.

## Key Findings

**1. Residence capacity increased relative to enrolment.**

Using published bed totals, reported capacity increased from approximately 205 beds per 1,000 students in 2020/21 to 228 in 2024/25. An alternative calculation using a different 2024 bed total gives approximately 221 beds per 1,000 students. Both indicate an increase, although these figures measure capacity rather than actual occupancy.

**2. Published waitlist milestones indicate continued housing pressure.**

Public statements reported over 8,000 students on the waitlist in 2022 and more than 7,000 in 2025. These are threshold-based figures rather than exact counts, so they cannot establish a precise annual trend.

**3. The nearby rental market was expensive, with limited vacancies.**

In October 2025, the University Endowment Lands zone, which includes UBC, had an average purpose-built rental price of $2,805 per month and a vacancy rate of 1.3%. Across the Vancouver Census Metropolitan Area (CMA), the average rent was $1,970 and the vacancy rate was 3.7%.

**4. Planned expansion is substantial, but does not predict when waitlist pressure will ease.**

UBC's Housing Action Plan includes 3,300 new Vancouver beds and 1,000 replacement beds. The number of planned new beds is less than 47.2% of the published 2025 waitlist threshold of more than 7,000 students. This comparison illustrates scale; it does not predict how the waitlist will change.

## Recommendations

- Continue publishing consistent annual data on residence capacity, waitlist size, applications, allocations, and occupancy.
- Track housing capacity relative to enrolment while clearly distinguishing capacity from actual occupancy.
- Monitor rent and vacancy trends in nearby rental zones to understand the broader off-campus housing context.
- Evaluate planned housing expansion against future demand, eligibility, and allocation outcomes.

## Methodology

1. Collected public enrolment, residence-bed, waitlist, rental-market, and residence-fee data.
2. Cleaned and combined the data using Pandas and NumPy.
3. Compared reported residence capacity with enrolment.
4. Visualized published waitlist milestones and rental-market indicators.
5. Compared residence fees with a studio-rent benchmark.
6. Examined planned expansion while documenting important data limitations.

## Tools Used

- **Python:** Pandas, NumPy
- **Visualization:** Matplotlib
- **Environment:** Jupyter Notebook
- **Research and documentation:** UBC public reports and CMHC rental-market data

## Repository Contents

- `01_housing_eda_FINAL.ipynb` — exploratory analysis, charts, and conclusions
- `SOURCES.md` — source links, definitions, and known data gaps
- `data/raw/` — supporting aggregate CSV files
- `figures/` — exported charts
- `requirements.txt` — Python dependencies

## How to Run

1. Clone or download the repository.
2. Install the required packages with `pip install -r requirements.txt`.
3. Ensure the supporting CSV files are available beside the notebook or in `data/raw/`.
4. Open `01_housing_eda_FINAL.ipynb` in Jupyter and run the cells in order.

The notebook uses six CSV files: `ubc_enrolment_vancouver.csv`, `ubc_housing_beds.csv`, `ubc_waitlist.csv`, `cmhc_vancouver_cma_avg_rent.csv`, `cmhc_zone_2025.csv`, and `ubc_residence_fees_2026_27.csv`.

## Limitations

Bed counts and waitlist figures are dated public statements, not continuous annual series. UBC's published bed totals contain an unresolved 396-bed discrepancy. CMHC rental figures describe purpose-built rental housing and exclude secondary-market options such as rented condos and basement suites. Residence fees and rental prices cover different periods and include different services.

The analysis identifies patterns in aggregate public data. It does not establish causation or determine individual students' housing needs, waitlist outcomes, or future housing availability.

## Sources and Acknowledgments

Source details, definitions, and known data gaps are documented in [`SOURCES.md`](SOURCES.md). Public sources include UBC Planning, Analytics & Institutional Research, UBC Housing, UBC Housing Action Plan materials, and CMHC.

This is an independent student portfolio analysis using public aggregate data.
