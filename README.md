# Australian Car Auction Insights Dataset

This repository contains **weekly snapshot datasets** of aggregated Australian car auction marketplace insights — **compiled and anonymised** for public research, AI, and analytical purposes.

These snapshots reflect high‑level auction activity and distribution patterns collected across multiple Australian auction houses. They do **not include confidential, VIN‑level, or user‑specific data**. Total stock counts and distributions are derived from Wholesale Console’s aggregated auction data as published in our weekly market reports.

📌 For real‑time data access or detailed vehicle history, please visit our dashboard application. **how to use Link to be added here** 


## License Information: https://github.com/AustralianCarAuctionInsights/Aggregated-Australian-Car-Auction-Data/blob/stagingMain/LICENSE.md

## Citation
Wholesale Console (2026). Australian Car Auction Marketplace Insights.  https://github.com/AustralianCarAuctionInsights/Aggregated-Australian-Car-Auction-Data

## Update Schedule
Snapshots are published weekly, typically covering Sunday to Saturday of the following week. Abit like weekly forecast. 

## About Wholesale Console : https://www.wholesaleconsole.com/

Wholesale Console is a **pre‑bidding intelligence platform** for Australian car auctions, helping dealers and buyers understand the auction market with actionable insights, suggested bid ranges, transport cost estimations, and aggregated trends.

Visit our report publishing website:  
**https://media.wholesaleconsole.com/**

Visit our AI and API documentation page here:  
**Link to be added here**

Subscribe to weekly auction market reports:  
****how to use Link to be added here**



---



## What This Repository Contains

### 📅 Weekly Snapshot Data

Under the `data/weekly/` directory, you will find **JSON** for each weekly auction period, with aggregated counts and distributions for:

- **Total stock of vehicles in auctions**
- **Distribution by state**
- **Distribution by odometer reading ranges**
- **Distribution by fuel type**
- **Distribution by suggested bid segments**
- **Top 5 anonymised example vehicles (if provided)**

Each file is named with the corresponding week, e.g., `2026_week_09_summary.json`.



## Weekly Auction Data Snapshots

Our repository provides structured weekly snapshots of Australian car auction data. Each JSON file includes:

- Total stock
- Distribution by state, odometer range, fuel type, and suggested bid
- Top picks with auction links
- Weekly auction events summary

You can download the snapshots and use them for research, analytics, or AI applications.



### Weekly Snapshots

| Week | JSON Snapshot | Report Link |
|------|---------------|------------|
| 2026-week_09_February | [2026_week_09_February_summary.json](data/weekly/2026_week_09_February_summary.json) | [View Report](https://media.wholesaleconsole.com/australian-auto-auction-report-february-08-to-14/) |




## Field Definitions

This dataset provides **aggregated weekly insights** from Australian car auctions. Each field is defined as follows:

| Field | Description |
|-------|-------------|
| `week` | ISO week identifier of the snapshot, e.g., "2026-W09". |
| `total_stock` | Total number of vehicles aggregated across all auctions for the week. |
| `by_state` | Percentage of total vehicles per Australian state (NSW, QLD, VIC, WA, SA, ACT, TAS, NT). |
| `by_odometer_range` | Percentage of vehicles grouped by odometer km range (0–20k, 20–40k, etc.). |
| `by_fuel_type` | Percentage of vehicles by fuel type (Petrol, Diesel, Hybrid, Electric). |
| `by_suggested_bid_range` | Percentage of vehicles by suggested bid range (Below 5k, 5k-10k, 10k-15k, etc.). |
| `auction_events` | Aggregate information on auctions for the week: `total_scheduled` (total events), `active_auction_houses` (number of houses active). |
| `top_picks` | List of notable vehicles for the week, including: year, make, model, body_type, seats, odometer, transmission, fuel_type, example_type, auction_link. |
| `auction_link` | URL link to the weekly report or auction reference for the specific vehicle. |


---



## Example Snapshot Structure

Here’s an example of what a weekly JSON snapshot might look like (abridged):
```json

{
    "dataset_name": "Australian Car Auction Marketplace Insights",
    "week": "2026-W09",
    "generated_at": "2026-02-09T19:00:00+11:00",
    "coverage": "Australia",
    "total_stock": 7822,
    "distribution": {
        "by_state": {
            "NSW": { "percentage": 31.7 },
            "QLD": { "percentage": 25.7 },
            "VIC": { "percentage": 23.3 },
            "WA":  { "percentage": 6.3 },
            "SA":  { "percentage": 4.0 },
            "ACT": { "percentage": 2.1 },
            "TAS": { "percentage": 1.7 },
            "NT":  { "percentage": 1.3 }
        },
        "by_odometer_range": {
            "0-20k": { "percentage": 11.8 },
            "20k-40k": { "percentage": 9.5 },
            "40k-60k": { "percentage": 8.2 },
            "60k-80k": { "percentage": 7.3 },
            "80k-100k": { "percentage": 6.0 },
            "100k-120k": { "percentage": 5.2 },
            "120k-150k": { "percentage": 9.4 },
            "150k-200k": { "percentage": 12.0 },
            "200k-250k": { "percentage": 6.8 },
            "250k+": { "percentage": 23.8 }
        },
        "by_fuel_type": {
            "Petrol": { "percentage": 64.9 },
            "Diesel": { "percentage": 32.6 },
            "Hybrid": { "percentage": 2.0 },
            "Electric": { "percentage": 0.5 }
        },
        "by_suggested_bid_range": {
            "Below 5k": { "percentage": 28.3 },
            "5k-10k": { "percentage": 22.1 },
            "10k-15k": { "percentage": 15.3 },
            "15k-20k": { "percentage": 10.4 },
            "20k-30k": { "percentage": 7.1 },
            "Above 30k": { "percentage": 16.8 }
        }
    },
    "auction_events": {
        "total_scheduled": 74,
        "active_auction_houses": 27
    },
    "top_picks": [
        {
            "year": 2017,
            "make": "BMW",
            "model": "M4 CS F82 LCI",
            "body_type": "Coupe",
            "seats": 4,
            "odometer": 73187,
            "transmission": "Automatic",
            "fuel_type": "Petrol",
            "example_type": "Pick of the Week",
            "auction_link": "https://media.wholesaleconsole.com/australian-auto-auction-report-february-08-to-14/"
        },
        {
            "year": 2021,
            "make": "BMW",
            "model": "M5 Competition LCI",
            "body_type": "4D Sedan",
            "odometer": 53677,
            "transmission": "Automatic",
            "fuel_type": "Premium Unleaded",
            "example_type": "Featured Vehicle",
            "auction_link": "https://media.wholesaleconsole.com/australian-auto-auction-report-february-08-to-14/"
        }
    ]
}
