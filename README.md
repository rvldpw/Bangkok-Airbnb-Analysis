# 📊 Bangkok Airbnb Pricing & Demand Analytics

 

![Python](https://img.shields.io/badge/Python-3.13-blue)

![Status](https://img.shields.io/badge/Status-Completed-green)

![Pandas](https://img.shields.io/badge/Pandas-2.x-lightgrey)

![License](https://img.shields.io/badge/License-MIT-green)

 

**Capstone Project #2 - Data Science & Analytics Program**

**Institution:** Purwadhika Digital School

**Author:** Rivaldi

 

---

 

## 📌 Overview

 

This project is an **exploratory and strategic analysis** of Bangkok Airbnb listings, examining how **price, location, and room type** drive booking performance. The analysis was prepared for Airbnb's **Revenue Management / Pricing Team** to support host acquisition, pricing optimization, and demand mapping across Bangkok.

 

**Business Questions:**

 

- **Q1.** Which price and room type segments should Airbnb prioritize to maximize overall demand?

- **Q2.** Which price, neighbourhood, and room type combinations deliver the most consistent bookings, and how can pricing guide hosts toward them?

 

---

 

## 👥 Stakeholder

 

**Primary:** Revenue Management / Pricing Team, Airbnb Bangkok, Thailand

 

This team focuses on optimizing pricing strategies to maximize booking performance across the platform.

 

---

 

## 🎯 Goals

 

This analysis aims to deliver actionable insight to support smarter pricing decisions:

 

- Identify high-performing price and room type segments

- Provide data-driven pricing recommendations for hosts

- Highlight top-performing neighbourhood and room type combinations

- Enable better in-app suggestions and targeted host outreach

 

**Deliverables from this analysis include:**

- Demand and listing distribution map (Leaflet.js / Folium)

- Top neighbourhood rankings by demand consistency

- Room type performance breakdown

- Market price range analysis

- Pricing insights and strategic recommendations

 

---

 

## 🗂️ Dataset

 

| | |

|---|---|

| **Source** | Inside Airbnb - Bangkok listings |

| **Initial rows** | 15,854 |

| **Final clean rows** | 14,839 (-6.4%) |

| **Columns** | 17 (numeric, text, datetime, categorical) |

 

**Key columns:** `neighbourhood`, `room_type`, `price`, `reviews_per_month`, `availability_365`, `minimum_nights`, `calculated_host_listings_count`

 

**Out of scope:** seasonality, host quality signals (response rate, superhost status), listing amenities.

 

**Cleaning steps:**

- No duplicates found

- Dropped non-analytical columns (`name`, `host_name`, `Unnamed: 0`)

- Imputed `0` for `reviews_per_month` on unbooked listings; added `has_reviews` flag

- Removed 1 listing with `price = 0`

- Capped price at 99th percentile (18,000 THB)

- Dropped listings with `minimum_nights > 365` or `availability = 0`

 

---

 

## 📊 Key Findings

 

### Market Overview

- Median nightly price: **1,422 THB**

- The 500-2,000 THB range is the core competitive segment, with the highest listing volume

- Listings above 5,000 THB are rare luxury outliers with limited demand

 

### Room Type

| Room Type | Supply Share | Avg Reviews/Month | Notes |

|---|---|---|---|

| Entire home/apt | 56.1% | 0.73 | Drives 75.1% of all review activity |

| Private room | 36.7% | 0.29 | Oversupplied, captures only 19.2% of reviews |

| Hotel room | 3.8% | 0.34 | Underserved segment up to 2,500 THB |

| Shared room | 3.4% | 0.11 | Weakest demand signal |

 

### Location

- Premium districts (Pathum Wan, Vadhana, Bang Rak) exceed **1,700 THB/night** due to BTS/MRT access

- Budget districts (Sai Mai, Bangkok Noi, Khan Na Yao) fall below **1,000 THB/night**

- Location drives up to an **8x price gap** across Bangkok

 

### Top Demand Combination

Entire home/apt in **Bang Rak or Khlong Toei**, priced **1,200-2,400 THB**, consistently scores highest on the demand performance index.

 

---

 

## 💡 Strategic Recommendations

 

| Strategy | Room Type | Location Tier | Target Price | Goal |

|---|---|---|---|---|

| **High Volume** | Entire home/apt | Mid-tier, transit-accessible (e.g., Khlong Toei, Bang Rak) | 1,200-1,700 THB | Maximum booking frequency |

| **High Revenue** | Entire home/apt | Premium central (e.g., Pathum Wan, Bang Rak, Phra Nakhon) | 2,000-3,000 THB | Maximum revenue per stay |

| **Balanced** | Entire home/apt | Mid-tier, transit-accessible (e.g., Vadhana, Khlong Toei, Huai Khwang) | 1,500-2,000 THB | Balance volume and margin |

| **Opportunity** | Private room | Mid-tier, transit-accessible (e.g., Vadhana, Khlong Toei) | 500-1,000 THB | Close supply/demand gap |

 
Private rooms show a structural imbalance (36.7% supply vs 19.2% review share), mainly due to weak demand above **2,500 THB**, where booking performance drops unless listings are clearly differentiated. The key driver of improvement is **competitive, transit-based pricing**, especially in mid-tier locations, to better capture demand.

To improve performance, focus on:
- Educating hosts with in-app insights, emails, and seminars on pricing thresholds and demand behavior  
- Optimizing private rooms in transit-accessible areas with a **500–1,000 THB** target range  
- Applying dynamic pricing to adjust for peak vs low seasons and maximize revenue  
- Improving listing quality (photos, descriptions, responsiveness) to increase conversion  
- Shifting supply toward stronger segments like entire homes where demand is more stable and scalable  

---

 

## Libraries  

This program uses the following libraries:

| Library | Purpose |

|---|---|

| `pandas` | Data cleaning and tabular analysis |

| `numpy` | Numerical computation |

| `matplotlib` / `seaborn` | Data visualization |

| `folium` | Interactive map (Leaflet.js) |

| `scipy` | Statistical testing (Kruskal-Wallis, Spearman) |

 

**Environment:** Conda (local) | **Editor:** Visual Studio Code

 

**Additional tools:** Canva (presentation), Tableau (dashboard)

 

---

## 📁 Repository Structure

 

```

├── README.md    # Project documentation

├── bangkok_airbnb_analysis.ipynb   # Main analysis notebook

├── listings.csv    # Raw dataset

```

---

 

## 🔗 Links


- 📊 **Tableau Dashboard:** [Bangkok Airbnb Pricing & Demand Insights](https://public.tableau.com/app/profile/rvld/viz/BangkokAirbnbPricingDemandInsights/Dashboard)

- 🎨 **Canva Presentation:** [Bangkok Airbnb Pricing Analytics](https://bangkok-airbnb-pricing-analystics.my.canva.site/)
