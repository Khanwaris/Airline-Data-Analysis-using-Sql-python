# ✈️ Airline Data Analysis

> **Tools Used:** SQL · Python  
> **Type:** Fresher Data Analyst Project  
> **Focus:** Flight Occupancy · Route Revenue · Pricing Strategy · Operational Efficiency

---

## What Is This Project About?

The airline operates flights across a wide network of routes and serves thousands of passengers every day. On paper, it looks like a functioning operation. But when you dig into the numbers, a clear problem shows up — the business is struggling to stay consistently profitable.

The reasons are not hard to spot. Operational costs are rising, some routes are planned poorly, and passenger demand keeps fluctuating. But the biggest issue I kept coming back to was this — a large number of flights are taking off with way too many empty seats.

Every empty seat is lost revenue the airline can never recover.

At the same time, certain routes are completely packed. The demand is there, but the airline is not doing enough to act on it. So you end up with two problems happening at once — too much capacity where it is not needed, and not enough where it actually is.

That imbalance became the central question of this project.

---

## The Problem in Plain Terms

- Many flights are operating with low occupancy — seats are going empty on every trip, which means the cost of running that flight is not being recovered
- Some routes are running at full or near-full capacity, but the airline is not capitalizing on that demand
- Revenue is driven by a small group of high-performing flights, while a large portion of the network is underperforming
- There is no clear data-driven system for deciding which routes to grow, which to cut back, and how to price tickets based on actual demand

---

## What I Analyzed

| Area | What I Was Looking For |
|---|---|
| Occupancy Rate Distribution | How full are flights on average across the network |
| Top 10 Flights by Occupancy | Which flights are consistently running at full capacity |
| Bottom 10 Flights by Occupancy | Which flights are nearly empty and costing more than they earn |
| Top 10 Flights by Revenue | Which individual flights are driving the most money |
| Top 10 Routes by Revenue | Which city-to-city routes are the strongest performers |
| Lowest 10 Routes by Revenue | Which routes are barely generating enough to justify operating |

---

## Key Numbers at a Glance

| Metric | Finding |
|---|---|
| Occupancy Range | Wide spread — from near 0% to 100% across the network |
| Top Performing Flights | Operating at or very close to 100% occupancy |
| Bottom Performing Flights | Occupancy below 1% — nearly empty on every trip |
| Top Revenue Route | DME → KHV and KHV → DME lead by a clear margin |
| Revenue Distribution | Heavily concentrated in a small group of flights and routes |

---

## What the Data Showed

**The occupancy gap is the core problem.**
When I plotted occupancy across all flights, the spread was striking. A noticeable chunk of flights are sitting in the low-to-mid occupancy range. These are not cancelled flights — they are running regularly, burning fuel, paying crew, but filling only a fraction of their seats.

**Some flights are doing everything right.**
The top 10 flights by occupancy are all operating at or near 100%. Passengers want these routes and they are booking them out consistently. These are not lucky outliers — they are proof that strong demand exists on certain corridors.

**The bottom 10 flights are a serious problem.**
These flights have occupancy rates below 1%. For every 100 seats, fewer than 1 is filled. They are technically operating, but almost certainly losing money on every single trip. Something needs to change — whether that is cutting frequency, switching to smaller aircraft, or introducing promotional pricing to test whether demand can be built.

**Revenue is concentrated in a few routes.**
The top revenue-generating flights all perform at a similar level, which tells you consistent demand and decent pricing are working together on those routes. But the gap between the top routes and the bottom routes is enormous — and the lowest performing routes are generating a fraction of what the best ones earn.

**DME → KHV is the standout route.**
This corridor and its reverse (KHV → DME) top the revenue charts. When both directions of the same route appear at the top, it confirms this is a genuinely high-demand, high-value corridor that deserves more investment.

---

## Project Structure

```
airline-data-analysis/
│
├── data/
│   └── airline_data.db              # Source database
│
├── sql/
│   └── queries.sql                  # All SQL queries used in analysis
│
├── python/
│   ├── analysis.py                  # Main analysis script
│   ├── visualizations.py            # Chart generation
│   └── requirements.txt             # Python dependencies
│
├── charts/
│   ├── occupancy_distribution.png   # Figure 1
│   ├── top10_occupancy.png          # Figure 2
│   ├── bottom10_occupancy.png       # Figure 3
│   ├── top10_revenue_flights.png    # Figure 4
│   ├── top10_revenue_routes.png     # Figure 5
│   └── bottom10_revenue_routes.png  # Figure 6
│
├── report/
│   └── Airline_Analysis_Report.pdf  # Full written report
│
└── README.md
```

---

## Analysis Breakdown

### Occupancy Analysis
The first thing I looked at was how occupancy is distributed across the entire network. Rather than just looking at averages, I plotted the full distribution to understand the shape of the problem — and it showed a clear imbalance between high-demand and low-demand flights.

### Revenue Analysis
I then looked at which flights and routes are actually generating money. The goal was to identify the backbone of the business — the routes that are doing the heavy lifting — and separate them from the routes that are dragging performance down.

### Route-Level Performance
By combining occupancy and revenue data at the route level, I could identify not just which routes earn the most, but which ones are worth growing versus which ones need to be reconsidered entirely.

---

## What I Would Recommend

**Fix the low-occupancy flights first.**
These are the most immediate drain on profitability. Options worth considering: reduce how often they run, switch to smaller aircraft to cut costs, or try promotional pricing to see if demand can be created. Running a near-empty large aircraft is one of the most expensive things an airline can do.

**Double down on the high-demand routes.**
Flights running at 100% occupancy are leaving money on the table if the airline is not adding capacity or adjusting pricing to reflect that demand. More flights, larger aircraft, or dynamic pricing on these routes would directly improve revenue.

**Protect and grow the top revenue routes.**
DME → KHV and the other top-performing corridors are the backbone of the business right now. Investment here — more frequency, better service, optimized pricing — would generate the clearest return.

**Re-evaluate the weakest routes seriously.**
Some of these routes may never be profitable at the current scale. The question is not just how to improve them — it is whether the airline should continue operating them at all. Data should drive that decision, not habit.

**Build a dynamic pricing system.**
Right now pricing does not appear to be responding to real-time demand patterns. Flights that are nearly full should cost more. Flights that are struggling to fill seats should be tested with lower prices earlier in the booking window — not just before departure when it is too late.

---

## Tools & Skills Used

- **SQL** — Data extraction, filtering, aggregation, route-level joins, ranking queries
- **Python** — Data cleaning, occupancy calculations, revenue analysis, chart generation
- **Libraries** — Pandas, Matplotlib, Seaborn
- **Data Analysis** — Occupancy rate analysis, revenue benchmarking, route performance comparison, demand pattern identification

---

## How to Run This Project

1. Clone the repository
2. Install dependencies:
   ```bash
   pip install -r python/requirements.txt
   ```
3. Run the SQL queries in `sql/queries.sql` against the database to extract the core datasets
4. Run the Python analysis:
   ```bash
   python python/analysis.py
   ```
5. Charts will be saved to the `charts/` folder
6. Read `report/Airline_Analysis_Report.pdf` for the full written analysis

---

## About This Project

This is a personal data analysis project built as part of my fresher portfolio. The goal was to take a real airline operations dataset, ask meaningful business questions, and use SQL and Python to find answers that are actually useful.

The part that surprised me most was the occupancy data. I expected to find some underperforming flights — but flights running at below 1% occupancy while still being scheduled regularly was harder to explain. It tells you that operational decisions are not being driven by performance data, and that is exactly the kind of gap that data analysis is supposed to close.

---

*Built with SQL & Python · Fresher Data Analyst Project*
