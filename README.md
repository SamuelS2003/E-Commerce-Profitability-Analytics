# E-Commerce Performance & Profitability Analysis

A four-page Power BI dashboard that shows where an e-commerce business makes money and where it loses it. It covers 2024 and 2025, about €640K in net sales and 5,873 orders.

I built it to answer one question: sales are growing, so why does the margin feel fragile? The short answer is that three things eat into it. Deep discounts, returns, and stock-outs.

## Headline numbers

| Metric | Value |
|---|---|
| Net sales | €640.42K |
| Contribution margin | €127.65K (19.42%) |
| Orders | 5,873 |
| Average order value | €109.05 |
| Return rate | 10.04% (1,099 units) |
| Return loss | €102.90K |
| On-time delivery | 92.75% |
| Unfulfilled units | 498 of 11,449 ordered |
| Lost sales value | €36.71K |

## What's in the dashboard

**1. Executive Performance.** The overall picture: net sales and margin % by quarter, sales by department, margin by category, and sales by region. This is the page a CEO or CFO would open first.

**2. Product & Customer.** Margin broken down by campaign and by product, with year and department slicers. It exists to show which promotions and products actually earn money once discounts are taken off.

**3. Returns & Operations.** Return reasons, returned units and return loss by category, sales by channel, and on-time delivery by fulfilment model (owned network, marketplace, 3PL).

**4. Inventory.** Ordered versus fulfilled units by quarter, lost sales by category, unfulfilled units by region, and a product table showing which backordered items cost the most.

## What I found

- **Margin depends heavily on category.** Beauty earns 46.34%. Electronics earns 2.83%.
- **Deep discounts lose money.** Clearance 35% runs at -11.57% margin and Weekend Flash 25% at 1.39%. Loyalty 10% earns 26.19% and VIP Private Sale 12% earns 22.30%, so the biggest discounts are not the best performers.
- **Two Smart Home products are loss-making.** Smart Home Elite (-0.93%) and Smart Home Plus (-2.91%). Elite also has a 12.24% return rate, above the 10.04% average.
- **Returns are mostly preventable.** "Changed mind" is the biggest reason (292), but size/fit (271), not as described (183), defective (134) and damaged in transit (130) are all things the business can fix.
- **Fashion has the most returned units. Electronics has a high loss per unit.** (Read from the chart, so treat as approximate.)
- **3PL is the weakest fulfilment model** at 88% on-time, against 96% for the owned network.
- **Electronics accounts for about half of lost sales** (€18.69K of €36.71K). Worth noting that at a 2.83% margin, the profit behind that revenue is small, so restocking Electronics is a revenue story more than a profit story.
- **Western Europe and the Baltics hold 264 of the 498 unfulfilled units.**

## Who it's for

| Page | Main audience | Decisions it supports |
|---|---|---|
| Executive Performance | CEO, CFO, regional heads | Where to invest, which categories and markets to grow |
| Product & Customer | Marketing, merchandising, pricing | Which campaigns and products to keep, reprice or drop |
| Returns & Operations | Operations, customer experience, channel managers | How to cut return loss, which fulfilment model to lean on |
| Inventory | Inventory planners, procurement, category managers | What to restock first |

## Caveats

- Figures marked approximate in the report (margin by region, return loss by category, quarterly gaps) were read off chart positions, not pulled from the data model. Check them in Power BI before quoting them.
- 2025 Q4 shows a sales dip. I haven't confirmed whether that quarter is complete.
- I'd want to confirm how Return Loss is defined relative to Net Sales, so nothing is counted twice.
- The campaign and product tables scroll, and I only had the visible rows. There may be more campaigns than the six I discuss.
- The Page 1 KPI card reads "Average Oder Value". It should say "Order".

## Tools

Power BI and DAX.

## Files

- `Ecommerce_Performance_Analysis_Report.pptx`: a 14-slide report covering each page, the business question behind each chart, stakeholder scenarios, and recommended actions.

## What I'd do next

- Add a drill-through from campaign to category, to see whether Clearance loses money everywhere or only in certain categories.
- Show return rate by product and reason in one view.
- Add days of cover or a stock-out reason to the Inventory page.
- Put margin thresholds on the campaign table with conditional formatting, so a campaign below target stands out.

