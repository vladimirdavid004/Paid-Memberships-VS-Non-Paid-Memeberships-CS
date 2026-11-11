# Cyclistic Bikes Share Case Study

## Business question
How do annual members and casual riders use Cyclistic bikes differently?

## Data
Divvy public trip data, April 2020 to March 2021 (link here)

## Tools
Google Cloud Storage, BigQuery (SQL), Python

## Process
1. Loaded monthly CSVs from a GCS bucket into BigQuery with a Python script
2. Cleaned the data in SQL (see `sql/01_cleaning.sql`): removed negative and 24h+ rides, test stations, and invalid rider types; added ride length, day of week, hour, and month
3. Analyzed patterns by rider type

## Key findings
- (fill in once you have them)

## Recommendations

Offer a weekend or summer membership. Casual riders lean toward weekends and warm months, so give them a lower-commitment plan that fits how they already ride, with an upgrade path to annual.
Market at the top casual stations. Put signage, QR codes, and in-app offers at the lakefront and tourist stations from your Q6 results.
Time campaigns for spring and early summer, and pitch the savings on long rides. Launch before casual riding peaks, and show casual riders how much they’d save on long rides with a membership. Their longer rides are exactly where pay-per-ride gets expensive.

One limitation to include: the data has no rider IDs, so you can’t tell how many people are casual riders or how often each one rides. A survey or rider-level data would make the conversion pitch much stronger. Mentioning that limitation shows good judgment.

Next step: run the six queries in 03_analysis.sql, then screenshot or paste the results here. I’ll write your actual Key Findings and Recommendations sections with your real numbers in them, ready to drop into the README and the deck.
