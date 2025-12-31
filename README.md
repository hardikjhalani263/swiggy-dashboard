HEADER
 ├─ Logo + Title
 ├─ Filters

KPI ROW
 ├─ Total Sales
 ├─ Avg Rating
 ├─ Orders
 ├─ AOV

ANALYSIS
 ├─ Top Restaurants
 ├─ Monthly Trend
 ├─ Veg vs Non-Veg
 ├─ Sales Map

INSIGHTS
 ├─ Key findings

-- Core KPI Cards (Top Section)

1. Total Sales = SUM(Swiggy[Sales])
2. Avg Rating = ROUND(AVERAGE(Swiggy[Rating]), 2)
3. Total Orders = DISTINCTCOUNT(Swiggy[Order_ID])
4. Dish Count = DISTINCTCOUNT(Swiggy[Dish_Name])


-- Parameter we made in this swiggy_data

Parameter = {
    ("Avg order value", NAMEOF('Swiggy_Data'[Avg order value]), 0),
    ("avg rating", NAMEOF('Swiggy_Data'[avg rating]), 1),
    ("Avg rating count", NAMEOF('Swiggy_Data'[Avg rating count]), 2),
    ("total sale", NAMEOF('Swiggy_Data'[total sale]), 3)
}
