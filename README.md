# 📊 Bangkok Airbnb Pricing & Demand Analytics

![Python](https://img.shields.io/badge/Python-3.13-blue)
![Status](https://img.shields.io/badge/Status-Completed-green)
![Pandas](https://img.shields.io/badge/Pandas-2.x-lightgrey)
![License](https://img.shields.io/badge/License-MIT-green)

**Capstone Project #2 — Data Science & Analytics Program**  
**Institution:** Purwadhika Digital School  
**Author:** Rivaldi  

---

## Overview

This project is an exploratory and strategic analysis of Bangkok Airbnb listings, focusing on how price, location, and room type influence booking performance. It is designed to support Airbnb’s Revenue Management / Pricing Team in improving host acquisition, pricing strategy, and demand allocation.

### Business Questions
- Which price and room type segments should be prioritized to maximize demand?
- Which combinations of price, neighbourhood, and room type generate the most consistent bookings, and how should pricing guide host behavior?

---

## Stakeholder

Primary: Revenue Management / Pricing Team — Airbnb Bangkok, Thailand  
Focus: optimizing pricing strategies to maximize platform-wide booking performance

---

## Goals

- Identify high-performing price and room type segments  
- Provide data-driven pricing recommendations for hosts  
- Highlight top neighbourhood and demand combinations  
- Enable smarter in-app recommendations and host targeting  

### Deliverables
- Demand & listing distribution map (Folium / Leaflet.js)  
- Neighbourhood performance ranking  
- Room type breakdown  
- Market price range analysis  
- Strategic pricing recommendations  

---

## Dataset

| Metric | Value |
|---|---|
| Source | Inside Airbnb — Bangkok listings |
| Initial rows | 15,854 |
| Final rows | 14,839 (-6.4%) |
| Columns | 17 |

Key features: `neighbourhood`, `room_type`, `price`, `reviews_per_month`, `availability_365`, `minimum_nights`, `calculated_host_listings_count`

Out of scope: seasonality, host quality signals, amenities

### Cleaning Steps
- Removed duplicates (none found)  
- Dropped non-analytical columns  
- Imputed missing review values (0 + flag)  
- Removed invalid pricing (price = 0)  
- Capped extreme prices (99th percentile)  
- Filtered unrealistic availability and minimum nights  

---

## Key Findings

### Market Overview
- Median price: 1,422 THB  
- Core market: 500–2,000 THB range  
- Luxury segment (>5,000 THB): low volume, niche demand  

### Room Type Performance

| Room Type | Supply Share | Avg Reviews/Month | Insight |
|---|---|---|---|
| Entire home/apt | 56.1% | 0.73 | Drives 75.1% of demand |
| Private room | 36.7% | 0.29 | Oversupplied, underperforming |
| Hotel room | 3.8% | 0.34 | Underserved mid-range potential |
| Shared room | 3.4% | 0.11 | Weakest segment |

### Location Insight
- Premium districts exceed 1,700 THB/night  
- Budget areas fall below 1,000 THB/night  
- Location creates up to 8x price variation  

### Top Demand Segment
Entire homes in Bang Rak / Khlong Toei, priced 1,200–2,400 THB, show the strongest and most consistent demand.

---

## Strategic Recommendations

| Strategy | Room Type | Location | Target Price | Goal |
|---|---|---|---|---|
| High Volume | Entire home/apt | Mid-tier transit zones | 1,200–1,700 THB | Max bookings |
| High Revenue | Entire home/apt | Premium central | 2,000–3,000 THB | Max revenue |
| Balanced | Entire home/apt | Mid-tier transit zones | 1,500–2,000 THB | Volume + margin |
| Opportunity | Private room | Mid-tier transit zones | 500–1,000 THB | Fix demand gap |

Private rooms show structural underperformance due to oversupply and weak demand above 2,500 THB. Improvement requires pricing alignment, better positioning, and stronger listing quality.

### Focus Areas
- Educate hosts with pricing insights  
- Optimize private rooms near transit zones  
- Apply dynamic pricing for seasonality  
- Improve listing quality (photos, responsiveness)  
- Shift supply toward entire homes  

---

## Libraries

| Library | Purpose |
|---|---|
| pandas | Data analysis |
| numpy | Numerical computation |
| matplotlib / seaborn | Visualization |
| folium | Interactive mapping |
| scipy | Statistical testing |

Environment: Conda  
Editor: VS Code  
Tools: Tableau, Canva  

---

## Repository Structure
├── README.md
├── bangkok_airbnb_analysis.ipynb
├── listings.csv

---

## Links

- Tableau Dashboard: Bangkok Airbnb Pricing & Demand Insights  
- Canva Presentation: Bangkok Airbnb Pricing Analytics
