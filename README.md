# 🌏 Bangkok Airbnb Pricing & Demand Analytics

![Python](https://img.shields.io/badge/Python-3.13-blue)  
![Status](https://img.shields.io/badge/Status-Completed-green)  
![Pandas](https://img.shields.io/badge/Pandas-2.x-lightgrey)  
![License](https://img.shields.io/badge/License-MIT-green)  

**Capstone Project #2 – Data Science & Machine Learning Program**  
**Institution:** Purwadhika Digital School  
**Creator:** Rivaldi  

---

## Project Overview  

This project is an **exploratory and strategic analysis of Bangkok Airbnb listings**, focusing on how **price, location, and room type** influence booking performance.

Developed as part of a **Data Science & Analytics program at Purwadhika Digital School**, this project simulates real-world pricing and revenue management decision-making for Airbnb’s marketplace.

It is designed to support **Revenue Management / Pricing teams** by identifying demand patterns, optimizing host pricing behavior, and improving supply allocation across Bangkok.

--- 

## Context, Problem, and Users  

**1. Context**  
The Bangkok Airbnb market varies significantly across price levels, neighbourhoods, and room types. Central and transit-connected areas generally show stronger demand, while peripheral zones and private rooms tend to underperform. This creates a fragmented market where performance depends heavily on correct price–location–room type alignment.

**2. Problem**  
Without clear segmentation, it is difficult to identify which combinations of price, neighbourhood, and room type drive consistent bookings. This leads to mispricing, with some listings overpricing in weak-demand segments and others underpricing in strong-demand areas. As a result, demand is unevenly distributed and revenue potential is not fully captured.

**3. Users**  
Revenue Management/Pricing teams responsible for optimizing marketplace performance. They need insights to prioritize high-performing segments and guide host pricing decisions to improve booking consistency and demand allocation.

---

## Business Questions  

- Which price and room type segments should be prioritized to maximize demand?  
- Which combinations of price, neighbourhood, and room type generate the most consistent bookings, and how should pricing guide host behavior?  

---

## Goals  

- Identify high-performing price and room type segments  
- Provide data-driven pricing recommendations for hosts  
- Highlight top-performing neighbourhood and demand combinations  
- Enable smarter in-app recommendations and host targeting  

---

## Deliverables  

- Demand & listing distribution map (Folium / Leaflet.js)  
- Neighbourhood performance ranking  
- Room type performance breakdown  
- Market price range analysis  
- Strategic pricing recommendations  

---

## Dataset  

| Metric | Value |
|---|---|
| Source | Airbnb Bangkok listings |
| Initial rows | 15,854 |
| Final rows | 14,839 (-6.4%) |
| Columns | 17 |

**Key features:** `neighbourhood`, `room_type`, `price`, `reviews_per_month`, `availability_365`, `minimum_nights`, `calculated_host_listings_count`  

**Out of scope:** seasonality, host quality signals, amenities  

### Data Cleaning Process  
- Removed duplicates (none found)  
- Dropped non-analytical columns (`name`, `host_name`, `Unnamed: 0`)  
- Imputed missing `reviews_per_month` with 0 + created `has_reviews` flag  
- Removed invalid listings (`price = 0`)  
- Capped extreme prices at 99th percentile (18,000 THB)  
- Filtered unrealistic listings (`minimum_nights > 365`, `availability = 0`)  

---

## Key Findings  

### Market Overview  
- Median nightly price: **1,422 THB**  
- Core market: **500–2,000 THB range**  
- Luxury segment (>5,000 THB): low volume, niche demand  

---

### Room Type Performance  

| Room Type | Supply Share | Avg Reviews/Month | Insight |
|---|---|---|---|
| Entire home/apt | 56.1% | 0.73 | Drives 75.1% of demand |
| Private room | 36.7% | 0.29 | Oversupplied, underperforming |
| Hotel room | 3.8% | 0.34 | Underserved mid-range opportunity |
| Shared room | 3.4% | 0.11 | Weakest segment |

---

### Location Insight  
- Premium districts (Pathum Wan, Vadhana, Bang Rak) exceed **1,700 THB/night**  
- Budget districts (Sai Mai, Bangkok Noi, Khan Na Yao) fall below **1,000 THB/night**  
- Location creates up to **8x price variation across Bangkok**  

---

### Top Demand Segment  
Entire homes in **Bang Rak / Khlong Toei**, priced **1,200–2,400 THB**, show the strongest and most consistent demand performance.

---

## Strategic Recommendations  

| Strategy | Room Type | Location | Target Price | Goal |
|---|---|---|---|---|
| High Volume | Entire home/apt | Mid-tier transit zones (Khlong Toei, Bang Rak) | 1,200–1,700 THB | Max booking frequency |
| High Revenue | Entire home/apt | Premium central (Pathum Wan, Bang Rak, Phra Nakhon) | 2,000–3,000 THB | Max revenue per stay |
| Balanced | Entire home/apt | Mid-tier transit zones (Vadhana, Khlong Toei, Huai Khwang) | 1,500–2,000 THB | Balance volume and margin |
| Opportunity | Private room | Mid-tier transit zones (Vadhana, Khlong Toei) | 500–1,000 THB | Close supply/demand gap |

Private rooms show structural underperformance due to oversupply and weak demand above **2,500 THB**, requiring stronger pricing discipline and better positioning.

---

## Focus Areas  

- Educate hosts through in-app insights, emails, and seminars  
- Optimize private rooms near transit-accessible areas  
- Apply dynamic pricing for seasonal demand shifts  
- Improve listing quality (photos, descriptions, responsiveness)  
- Shift supply toward entire homes where demand is more stable  

---

## 🔗 Links
 
- 📊 **Tableau Dashboard:** [Bangkok Airbnb Pricing & Demand Insights](https://public.tableau.com/app/profile/rvld/viz/BangkokAirbnbPricingDemandInsights/Dashboard)
- 🎨 **Canva Presentation:** [Bangkok Airbnb Pricing Analytics](https://bangkok-airbnb-pricing-analystics.my.canva.site/)

---

## Libraries  

- **pandas**: Data manipulation, cleaning, and tabular data analysis  
- **numpy**: Numerical computing and array operations  
- **matplotlib / seaborn**: Visualization for trends, patterns, and distributions  
- **folium**: Interactive mapping for geospatial analysis  
- **scipy**: Statistical testing (Kruskal-Wallis, Spearman)  

---

## Repository Structure

```text
 ├── README.md
 ├── airbnb_bangkok_listings.csv
 ├── bangkok_airbnb_analysis.ipynb
```

---

## Environment & Tools  

- Programming Language: Python  
- Environment: Conda (local machine)  
- Editor: Jupyter Notebook  
- Visualization & Reporting: Tableau, Canva  
