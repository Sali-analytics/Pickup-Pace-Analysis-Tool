# Hotel Booking Pace and Pickup Analysis

How far ahead guests book and how demand builds toward arrival, for a City Hotel and a Resort Hotel.

| Stayed bookings | Median booking window | Booked within 7 days | Booked over 180 days ahead |
|---|---|---|---|
| 75,166 | 45 days | 23.7% | 14.1% |

## Overview

This project analyses booking pace and pickup for two hotels in the Hotel Booking Demand dataset, with arrival dates from July 2015 to August 2017. It reconstructs when each stayed booking was made, then shows how demand builds before arrival and how that build differs by hotel, weekday, market segment and rate (ADR), and what drives the ten busiest arrival dates.

## Key findings

- Half of stayed bookings are made within 45 days of arrival (mean 80 days); 7.9% are made on the arrival day.
- Resort books later than City: median lead time 38 days against 50, and 10.6% of Resort bookings are same-day against 6.1%.
- Weekend arrivals (Fri to Sun) book earlier than weekday arrivals (Mon to Thu): median 51 days against 41.
- Median lead time by segment runs from 6 days (Corporate) to 107 days (Groups). Same-day bookings carry the lowest average ADR (EUR 82.8).
- On six of the ten busiest dates, one block booked on a single day makes up 38% to 57% of the date's bookings.

## Repository contents

| File | Description |
|---|---|
| `pickuppaceanalyses.ipynb` | Analysis notebook: data loading, date construction, pace curves, pickup heatmap, booking window, hotel, weekday and segment comparisons, ADR and top-date views. |
| `Hotel_Pickup_Pace_Report.pdf` | 13-page report with the full set of charts, tables, findings and recommendations. |
| `Hotel_Pickup_Pace_Workflow.pdf` | 2-page workflow explaining how the data was handled, how it was analysed and why each method was chosen. |

## Getting started

1. **Get the data.** Download `hotel_bookings.csv` (Kaggle: Hotel booking demand). The dataset is not included in this repository.
2. **Install the requirements.** Python 3 with `pandas`, `numpy`, `matplotlib`, `seaborn` and Jupyter.
3. **Set the path.** In the second code cell of the notebook, set `file_path` to the location of your copy of the CSV.
4. **Run the notebook** from top to bottom. It keeps stayed (Check-Out) bookings only, which gives 75,166 of 119,390 bookings.

## Method in brief

Booking date = arrival date minus lead time. Bookings are grouped by arrival date and lead time to build pace curves and pickup tables. In the report, groups are compared by their own share of bookings so that differences in size do not hide differences in timing.

## Data source and author

**Data source:** Hotel Booking Demand dataset, Antonio, Almeida and Nunes (2019), Data in Brief, volume 22.

**Author:** Hosea Ngo Sali. All rights reserved. This work is not to be duplicated or redistributed.
