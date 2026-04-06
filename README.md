# Transportation-Dashboard-Analysis-using-Microsoft-Excel-
This is a Transportation Transaction Dashboard built in Microsoft Excel, designed to monitor bus fleet performance, passenger ridership patterns, and route efficiency. It covers a transit operation running 84 total buses across multiple routes, tracking 6,587 total passengers. The dashboard spans at minimum two years of data (2023–2024) and provides operational insights across time-of-day, day-of-week, monthly, and yearly dimensions. A striking year-over-year ridership decline of 83.5% is the most urgent signal in the entire dashboard, making this a critical performance monitoring tool for transit management.


 ## Data Cleaning Steps
1. Timestamp parsing and time-range bucketing — Raw trip timestamps (e.g., "2024-03-15 20:57:32") were parsed to extract the hour of day. These were then grouped into four named time-range buckets (5:00 AM–10:00 AM, 10:00 AM–3:00 PM, 3:00 PM–8:00 PM, 8:00 PM–1:00 AM) using conditional logic. 
2. AM/PM classification — Each trip record was tagged as AM or PM based on its departure or arrival timestamp. This binary classification was then aggregated to produce the 35.4% AM / 64.6% PM split.
3. Route name standardisation — Route identifiers in the raw data were normalised to consistent names (e.g. "East-West Express", "South Line") to remove abbreviations, punctuation differences, or alternate naming conventions that would fragment route-level counts.
4. Bus utilisation classification — Each bus was assigned a utilisation status (Under-Utilised, Well-Utilised, Over-Utilised) based on a passenger load threshold. Buses with consistently low passenger counts were tagged as under-utilised, those within an acceptable band as well-utilised, and those exceeding capacity benchmarks as over-utilised. 
5. Day-of-week extraction — Transaction dates were used to derive a weekday label (Mon–Sun), enabling the weekly distribution bar chart. Date formatting inconsistencies (e.g. different regional date formats) were also carried out.
6. Monthly aggregation — Trip records were grouped by month and year to produce the "Riders Monthly Distribution" line chart. Months with zero trips or incomplete data were reviewed for accuracy or excluded.
7. Null and missing record treatment — Rows with missing passenger counts, undefined routes, or null timestamps were excluded. Given the precision of KPIs like "Avg. Riders per Trip = 33", missing values in the passenger count field would have significantly distorted averages and needed careful handling.


## Key Performance Indicators (KPIs)
i. **Total passengers =** 6,587 all routes combined

ii. **Avg. riders per trip =** 33 per bus journey

iii. **Busiest route =** East-West Express highest ridership

iv. **Least busy route =** South Line lowest ridership

v. **Peak hours of operation =** 08:57 PM

vi. **Off-peak hours of operation =** 07:50 PM

vii. **Total AM riders =** 35.4%

viii. **Total PM riders =** 64.6%

## Obevrsation 

-- Ridership collapsed 83.5% year-over-year: Total riders fell from 5,654 in 2023 to just 933 in 2024 — an 83.5% YoY drop. The dashboard itself flags this as needing urgent intervention.

-- 43% of the fleet is over-utilised: 36 buses are running above optimal capacity. This means passengers on these routes experience overcrowding while 19 buses on other routes sit under-loaded.

-- PM trips dominate at 64.6% of all ridership: Nearly two-thirds of all passengers travel in the PM, with peak time recorded at 08:57 PM. Morning service at 35.4% is significantly underutilised by comparison.

-- Weekends (Sat–Sun) produce the highest daily ridership: Sunday peaks at 1,185 and Saturday at 796, both highlighted in red as above the 941 average. Weekday ridership is more consistent, ranging from 762 (Friday) to 1,085 (Monday).

-- East-West Express vs South Line gap is stark: The gap between the busiest and least busy routes indicates an uneven service demand distribution. Resources may be misallocated, with South Line buses potentially being over-deployed.

-- December is the peak month at 5,654 riders: There is a dramatic rise from January (933) to December (5,654) — over 6 times growth across the year, suggesting strong seasonality or a data period that captures a ramp-up phase.

-- Only 35% of buses are operating optimally: With 29 buses well-utilised, 19 under-used, and 36 over-used, the fleet is polarised. Effective reallocation from under- to over-loaded routes could improve efficiency without adding buses.


## Conclusion
The Transportation Dashboard reveals a transit system under significant operational stress. While the fleet of 84 buses is active and distributed across multiple routes, two critical problems stand out. First, the 83.5% year-over-year ridership decline from 5,654 (2023) to 933 (2024) is a severe warning signal, whether caused by incomplete data, service disruptions, or genuine ridership loss, it demands immediate investigation. Second, the fleet utilisation distribution is highly inefficient: 43% of buses are over-utilised (causing service quality issues) while 23% are under-utilised (wasting operational costs), and only 35% are in the optimal range. On the positive side, the system shows strong seasonal demand in December, consistent weekend ridership that exceeds weekday averages, and clear peak-time patterns centred around evening hours — all of which provide a solid foundation for smarter scheduling and fleet management.


## Recommendations
1. Urgently investigate the 83.5% YoY ridership decline- This is the single most important action item. The dashboard itself flags it as needing improvement. Management must determine whether this reflects incomplete 2024 data entry, a reporting period mismatch, genuine ridership loss due to route cancellations, fare increases, or competition from other transport modes. Without understanding the cause, no effective response can be designed.
2. Reallocate buses from under-utilised to over-utilised routes immediately- Of 84 buses, 19 are under-utilised, and 36 are over-utilised. Redirecting even 10 buses from low-demand routes to over-capacity ones could reduce crowding on busy routes and eliminate wasted fuel and driver costs on empty ones — a quick operational win requiring no new capital expenditure.
3. Review and restructure the South Line- As the least busy route, the South Line should be assessed for whether its current frequency is warranted. Options include reducing trip frequency, converting to a feeder service, or investigating whether low ridership reflects a scheduling or accessibility problem rather than a lack of demand.
4. Capitalise on December and weekend demand peaks. December ridership at 5,654 represents a 6 times increase over January. Management should ensure maximum fleet readiness going into the high season — preventive maintenance, driver scheduling, and contingency buses should all be planned well in advance. Similarly, weekend services, especially Sunday, should be reinforced, given that Sunday peaks at 1,185 riders.
5. Align fleet scheduling with the PM-dominant ridership pattern- With 64.6% of all trips happening in the PM and peak activity at 08:57 PM, current morning schedules may be over-resourced relative to demand. Shifting driver shifts and bus availability toward the evening window could improve service quality during peak hours while reducing unnecessary AM operating costs.
6. Develop a morning ridership growth strategy- The AM window generates only 35.4% of riders despite covering the traditional commuter hours. Promotional fares, partnerships with local employers for commuter programmes, or improved early-morning route coverage could help grow this underperforming segment and reduce the system's over-reliance on evening-only ridership.
7. Set formal utilisation benchmarks and track them monthly- Currently, only 35% of the fleet is well-utilised. The organisation should define a clear target — for example, achieving 60%+ well-utilisation within 12 months — and track progress monthly through the dashboard, with route-level accountability assigned to operations managers.
