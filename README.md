# Australian Car Auction Insights Dataset

This repository contains **weekly snapshot datasets** of aggregated Australian car auction marketplace insights — **compiled and anonymised** for public research, AI, and analytical purposes.

These snapshots reflect high‑level auction activity and distribution patterns collected across multiple Australian auction houses. They do **not include confidential, VIN‑level, or user‑specific data**. Total stock counts and distributions are derived from Wholesale Console’s aggregated auction data as published in our weekly market reports.

📌 For real‑time data access or detailed vehicle history, please visit our dashboard application. **how to use Link to be added here** 

## About Wholesale Console

Wholesale Console is a **pre‑bidding intelligence platform** for Australian car auctions, helping dealers and buyers understand the auction market with actionable insights, suggested bid ranges, transport cost estimations, and aggregated trends.

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
  "total_stock": 18432,
  "distribution": {
    "by_state": { "NSW": { "count": 6123, "percentage": 33.2 }, "...": {} },
    "by_odometer_range": { "0-50k": { "count": 2540, "percentage": 13.8 }, "...": {} },
    "by_fuel_type": { "Petrol": { "count": 9820, "percentage": 53.3 }, "...": {} },
    "by_suggested_bid_range": { "10k-20k": { "count": 6123, "percentage": 33.2 }, "...": {} }
  }
}
