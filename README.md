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

1. Members ride more often, casual riders ride longer. Members took 2,051,510 rides (59%) at 15.1 min on average. Casual riders took 1,424,418 rides (41%) at 35.9 min, about 2.4× longer.
2. Casual riders spend more total time on the bikes. They account for roughly 62% of all minutes ridden (an estimate: rides × average length).
3. Casual riding is a weekend thing. 42% of casual rides happen on Saturday and Sunday, vs 29% for members. Saturday has 2.3× as many casual rides as Tuesday. Member riding is steady all week.
4. Members commute, casual riders don't. Member rides jump from 17K at 5 AM to 103K at 8 AM, then peak at 215K at 5 PM. Casual riders have no morning bump and climb steadily to a 5 PM peak of 140K.
5. Casual riding is much more seasonal. 66% of casual rides fall in June–September, vs 54% for members. Casual rides drop about 29× from August to February, compared with 8× for members.
6. Casual riders cluster at the lakefront and downtown. The top stations are Streeter Dr & Grand Ave (26K), Lake Shore Dr & Monroe St (21K) and Millennium Park (19K). The top 10 stations alone account for 11% of all casual rides.
7. Bike type is a minor difference. Both groups mostly used docked bikes: 78% of casual rides and 70% of member rides.

## Recommendations

1. Offer a weekend or summer membership. Casual riders lean toward weekends and warm months, so give them a lower-commitment plan that fits how they already ride, with an upgrade path to annual.
Market at the top casual stations. Put signage, QR codes, and in-app offers at the lakefront and tourist stations from your Q6 results.
Time campaigns for spring and early summer, and pitch the savings on long rides. Launch before casual riding peaks, and show casual riders how much they’d save on long rides with a membership. Their longer rides are exactly where pay-per-ride gets expensive.

2. One limitation to include: the data has no rider IDs, so you can’t tell how many people are casual riders or how often each one rides. A survey or rider-level data would make the conversion pitch much stronger. Mentioning that limitation shows good judgment.

