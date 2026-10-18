# Data Sources

---

## PAIR-AER-2024-25-T4

**UBC Annual Enrolment Report 2024/25**, Table 4: Overall Student Headcount, by Year, by Campus (p. 34). Domestic figures from Table 5 (p. 35), international from Table 7 (p. 38).
Publisher: UBC Planning, Analytics & Institutional Research Office (PAIR).
URL: https://pair.ubc.ca/wp-content/uploads/sites/145/2025/03/UBC-Annual-Enrolment-Report-2024-25.pdf

Covers 2020/21 through 2024/25.

Note: the Vancouver total includes the Residents category (Dentistry, Medicine, Pharmaceutical Sciences residents), so `total_headcount` is not exactly `domestic + international`. The report states not all residents have student status. This is left uncorrected rather than silently reconciled.

---

## PAIR-AER-2019-20-T4

**UBC Annual Enrolment Report 2019/20**, Table 4: Overall Student Headcount, by Year, by Campus (p. 30). Domestic from Table 5 (p. 31), international from Table 7 (p. 34).
Publisher: UBC Planning, Analytics & Institutional Research Office (PAIR).
URL: https://pair.ubc.ca/wp-content/uploads/sites/145/2020/11/2019-20-Enrolment-Report.pdf

Covers 2015/16 through 2019/20. Combined with the 2024/25 edition this gives a continuous ten-year Vancouver series.

Note: the 2019/20 edition flags that from 2017/18 onward, Diploma & Certificate counts moved into the Undergraduate category. This affects category breakdowns but not the campus totals used here.

---

## CMHC-HMIP-ZONE-2025

**Vancouver, Rental Market Statistics Summary by Zone**, CMHC Rental Market Survey, October 2025 reference period. Vacancy rate, average rent, median rent and rental universe by RMS survey zone.
Publisher: Canada Mortgage and Housing Corporation, Housing Market Information Portal.
URL: https://www03.cmhc-schl.gc.ca/hmip-pimh/en/TableMapChart/Table?DisplayAs=Table&GeograghyName=Vancouver&GeographyId=2410&GeographyTypeId=3&TableId=2.1.31.3

Reliability codes are captured in the CSV (a excellent, b very good, c good, d poor). Figures used in the analysis carry a or b.

Zone reference: Zone 5 is Kitsilano/Point Grey, Zone 11 is University Endowment Lands (including UBC), Zone 3 is Downtown.

CMHC states the Rental Market Survey does not include student housing, so these zones measure the off-campus market a student competes in, not UBC residences. Purpose-built rental only; the secondary market (rented condos, basement suites) is excluded.

---

## CMHC-HMIP-HIST-AVGRENT

**Vancouver, Historical Average Rents by Bedroom Type**, CMHC Rental Market Survey, October reference periods.
Publisher: Canada Mortgage and Housing Corporation, Housing Market Information Portal.
URL: https://www03.cmhc-schl.gc.ca/hmip-pimh/en/TableMapChart/TableMatchingCriteria?GeographyType=MetropolitanMajorArea&GeographyId=2410&CategoryLevel1=Primary+Rental+Market&CategoryLevel2=Average+Rent+%28%24%29&ColumnField=2&RowField=TIMESERIES

Geography is the Vancouver CMA, not a sub-zone. Purpose-built rental only; the survey excludes the secondary market (rented condos, basement suites) where many students actually live.

Reliability codes (a/b/c/d) published alongside each figure are not captured in the CSV. All CMA-level figures used here carry code `a`.

---

## UEL-ZONE-2025 (SUPERSEDED)

Previously a secondary source for endowment-lands rents. Replaced by CMHC-HMIP-ZONE-2025, pulled directly from the CMHC portal. No longer used.


---

## Bed capacity

Assembled from dated UBC statements rather than a single published table. No annual series exists publicly.

| source_id | Figure | Origin |
|---|---|---|
| BCGOV-2019-SKEENA | 11,800 Vancouver | Province of BC news release, 2019: https://news.gov.bc.ca/releases/2019AEST0081-001252 |
| DH-2020-OCCUPANCY | ~12,000 Vancouver | Daily Hive, Oct 2020: https://dailyhive.com/vancouver/ubc-vancouver-enrolment-student-housing-coronavirus |
| DH-2023-EXPANSION | 13,205 Vancouver after Brock Commons North | Daily Hive, 2023: https://dailyhive.com/vancouver/ubc-student-housing-residence-expansion-strategy |
| UBCNEWS-2024-BROCKSOUTH | 13,883 Vancouver (16,003 system-wide) after Brock Commons South | UBC News, Aug 2024: https://news.ubc.ca/2024/08/ubc-new-student-residence-brock-south/ |

**Known inconsistency.** 13,205 plus Brock South's 282 beds gives 13,487, but UBC reports 13,883 for the same point. The 396-bed difference is unexplained in the public statements. It is carried into the analysis as-is and flagged, not smoothed.

---

## Waitlist

No published annual series. Every figure below is a point-in-time public statement, most of them rounded by the speaker. Treated as milestones, never interpolated.

| source_id | Figure | Origin |
|---|---|---|
| CBC-2019-NANO | 6,000 (2019) | CBC News, Sept 2019: https://www.cbc.ca/lite/story/1.5267186 |
| DH-2020-OCCUPANCY | in excess of 6,000 (2020) | Daily Hive, Oct 2020 (link above) |
| DH-2023-EXPANSION | 3,200 peak in 2010; over 6,000 in 2019; over 8,000 in 2022 | Daily Hive, 2023 (link above), citing UBC |
| UA-2025-CRUNCH | more than 7,000 | University Affairs, 2025: https://universityaffairs.ca/news/student-housing-crunch-eases/ |

---

## UBC-FEES-TOTEM / UBC-FEES-ORCHARD

2026/27 Winter Session residence fees, UBC Vancouver Student Housing.
- Totem Park: https://vancouver.housing.ubc.ca/applications/fees-payments/totem-park/
- Orchard Commons: https://vancouver.housing.ubc.ca/applications/fees-payments/orchard-commons/

Winter Session contract runs 5 Sep 2026 to 28 Apr 2027, treated as 8 months. Fees are subject to Board of Governors approval. Only the current year is captured; a fee time series would require archived fee pages.

---

## UBC-HAP-2023

**UBC Housing Action Plan 10-Year Update (2023), Vancouver Campus.** Policy 14 commits to increasing on-campus student housing to at least 17,300 beds from nearly 14,000; the plan commits to at least 3,300 new beds plus 1,000 replacement beds by the mid-2030s.
URL: https://planning.ubc.ca/sites/default/files/2024-04/2023-10-11_CV2050_HAP_Appendix_1_HAP_Report.pdf

---

## Gaps and what would close them

1. Zone-level rent and vacancy as a time series. Currently a single 2025 cross-section. Fix: export the Zone 5 and Zone 11 historical tables from the HMIP portal.
2. Residence fee history. Fix: archived UBC fee pages, or a request to Student Housing.
3. A continuous bed-count series. Fix: UBC Board of Governors materials or a direct request to Student Housing and Community Services.
4. Applicant-level demand, eligibility and allocation outcomes. Not public and not obtainable. This is a permanent limit on what this analysis can claim.
