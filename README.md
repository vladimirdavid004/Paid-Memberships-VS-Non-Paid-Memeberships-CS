# Cyclistic Bikes Share Case Study

## Business question
How do annual members and casual riders use Cyclistic bikes differently?

## Data
Divvy public trip data, April 2020 to March 2021

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

1. Offer a weekend or summer membership.
Casual riders already ride on weekends and in summer: 42% of their rides fall on Saturday and Sunday, and 66% fall in June–September. A lower-commitment plan that matches that pattern is an easier first step than a full annual membership. Build in an upgrade path to annual.

2. Market where casual riders already start.
Put signage, QR codes and in-app offers at the top 10 casual stations, led by Streeter Dr & Grand Ave, Lake Shore Dr & Monroe St and Millennium Park. Those 10 stations alone account for 11% of all casual rides. Target weekend afternoons, since casual riding builds through the day and peaks around 5 PM.

3. Launch in spring and sell the savings on long rides.
Start the campaign in March–April, before casual riding takes off (it grows about 8× from March to August). Pitch the cost: the average casual ride is 35.9 minutes, and casual riders log roughly 62% of all minutes ridden, so they're the riders paying the most per trip without a membership.
