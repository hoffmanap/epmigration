# Desert Drift: Who Is Remaking El Paso — and Where?

**[→ Read the full interactive story](https://hoffmanap.github.io/epmigration/)**

A data-driven scrollytelling investigation into the migration patterns reshaping one of America's fastest-growing border cities. Built with D3.js and Leaflet.js. Ten chapters. Sixteen visualizations.

---

## Key Findings

### 1. The Vacancy Chain Is Real — and the Income Gap Is $33,000
El Paso's housing market shows textbook filtering in action. Households arriving in the city's newest northeastern zip codes (79934, 79938, 79928) earn an average of **$76,000** annually. Those settling in the older core neighborhoods near Downtown and the Lower Valley earn closer to **$43,000** — a 77% income gap separating who gets new housing from who inherits old. Downtown El Paso's arriving households earn just $23,000 on average, less than a third of what's moving into the northeast suburbs.

### 2. New Construction Is Hyper-Concentrated — and Mostly Bought by Texans
Of 9,541 tracked moves, 61 households moved into brand-new construction. Nearly all of that activity — **96%** — sits in three zip codes: 79934, 79928, and 79938 along the northeastern and eastern fringe. New-home buyers earn $83,000 on average and are **87% Texas-origin**, meaning the new home boom is driven primarily by local upward mobility rather than out-of-state arrivals importing wealth.

### 3. New Homes Cost More Per Square Foot and Deliver Less Space
Buyers of new construction pay **$177 per square foot** for an average of 1,786 sq ft. Resale buyers get 2,048 sq ft for just **$157 per square foot** — 262 more square feet at a 13% lower cost per foot. The premium being paid for new construction is a premium for *newness*, not size. For households seeking maximum space per dollar, the city's older neighborhoods are often the better deal.

### 4. Californians Are Coming — but They're Not the Primary Driver of Housing Pressure
California is the single largest out-of-state origin at **296 households**, ahead of New Mexico (250) and Georgia (140). But that represents just **3.1% of all tracked moves**, and California arrivals earn only modestly more than the overall average ($65k vs. $63k). While California movers do disproportionately land in the city's highest-value zip codes (79922, 79932), they are too few in number to be driving citywide price appreciation. A notable share of "California movers" originate from San Diego and Los Angeles — cities adjacent to Marine Corps and Navy installations — suggesting the military pipeline may account for much of this flow.

### 5. The Military Is El Paso's Single Most Consistent Force in Housing
**294 households** in the dataset show clear military origins, tracing from installations across the country — Fort Carson (Colorado Springs), Fort Campbell (Clarksville), Fort Cavazos (Killeen), Fort Bragg (Fayetteville), and Schofield Barracks (Wahiawa, Hawaii) among the top feeders. Fort Bliss, the second-largest military installation in the U.S. by land area, anchors zip codes 79908 and 79906 as primary destination points. Military families' steady rotation creates a structural floor of housing demand that persists regardless of broader economic conditions.

### 6. VA Loans Are the Most Common Financing Instrument in the Market
Among tracked loan transactions, **VA loans account for 332 purchases** — more than conventional mortgages (257) and FHA loans (184) combined. VA borrowers purchase homes averaging **2,078 sq ft** at **$326,000**, nearly identical to conventional buyers, but without the down payment requirement. VA and FHA loans together account for roughly two-thirds of tracked loan activity, underscoring how deeply government-backed lending underwrites El Paso's housing market.

### 7. El Paso Is Being Remade by Movers in Their 50s and 60s
The two largest mover cohorts are the **55–59 age group** (2,113 households) and **60–64** (1,699) — together nearly 40% of all tracked moves. The 30–34 cohort, prime first-time homebuyer age, accounts for just **237 households**. A plausible explanation: military retirees choosing to remain near Fort Bliss after separating from service, a pattern common in major installation cities.

### 8. New Fringe Buyers Are Stretching Their Finances the Most
The ratio of purchasing power to stated income is highest in newer fringe zip codes (**1.06**), meaning buyers there routinely spend slightly beyond what income alone would support. In older core neighborhoods, buyers spend *below* their purchasing power (**0.96**). The new suburbs attract aspirational purchasing — a modest but real financial stretch that could matter if rates or incomes shift.

### 9. El Paso Transforms on a Predictable Annual Rhythm
Moves peak in **May** (1,004 households) and **August** (985), with a quiet winter trough in February (583). The dual-peak structure reflects two overlapping forces: spring civilian real estate seasonality and the military's PCS (Permanent Change of Station) window running June–August. El Paso's transformation is as seasonal as the monsoon — and the Fort Bliss PCS cycle is its most reliable engine.

---

## Methodology

### Data Sources
This project merges two primary datasets:

- **Mover records (n = 9,541):** Proprietary mover database capturing households that relocated to El Paso during the study period. Each record includes origin address, destination address, estimated household income (FIND — Family Income Detector variable, range $1,000–$500,000), purchasing power indicator (PPI), demographic attributes (age, gender), distance of move, deed transaction type, mortgage loan type, and geographic identifiers. Records also include former and current lat/lon coordinates.

- **MLS sales data:** El Paso-area Multiple Listing Service records for the same period, including sold price, list price, square footage, bedrooms, bathrooms, price per square foot, and transaction date. Merged to mover records via address matching. Of 9,541 mover records, 4,448 had complete MLS housing size data.

### Neighborhood Era Classification
Zip codes were classified into three development-era tiers based on the predominant period of residential construction:

| Era | Zip Codes | Description |
|-----|-----------|-------------|
| **Older Core** | 79901, 79902, 79903, 79904, 79905, 79907, 79915, 79925, 79930 | Pre-1950s to early 1960s urban grid; Downtown, Kern Place, Five Points, Lower Valley corridor |
| **Middle Ring** | 79908, 79912, 79922, 79924, 79932, 79935, 79936 | 1960s–1990s suburban expansion; Westside, Northeast mid-city, Fort Bliss adjacent |
| **New Fringe** | 79911, 79927, 79928, 79934, 79938 | 2000s–present greenfield development; Far Northeast, Far East, Northwest Hills |

### Military Household Identification
Military-affiliated households were identified by cross-referencing origin city names against a curated list of U.S. cities adjacent to known Army, Air Force, and Marine Corps installations. This method is conservative — many military families rotate through cities not on this list and are not captured. The 294-household count should be treated as a lower bound.

Key installation–city pairings used:

| City | Installation |
|------|-------------|
| Colorado Springs, CO | Fort Carson |
| Clarksville, TN | Fort Campbell |
| Killeen, TX | Fort Cavazos (formerly Hood) |
| Fayetteville, NC | Fort Bragg |
| Columbus, GA | Fort Moore (formerly Benning) |
| Wahiawa, HI | Schofield Barracks |
| Tacoma/Lakewood, WA | Joint Base Lewis-McChord |
| Enterprise, AL | Fort Novosel (formerly Rucker) |
| Lawton, OK | Fort Sill |
| Watertown, NY | Fort Drum |

### Income and Purchasing Power
- **FIND (Family Income Detector):** Modeled household income estimate, range $1,000–$500,000. Used as primary income variable throughout.
- **PPI (Purchasing Power Indicator):** Estimated household purchasing capacity. The PPI/FIND ratio (values > 1.0 indicate spending above income) is used in Chapter 9 to assess financial stretch by neighborhood era.

### Seasonal Analysis
Move acquisition dates were extracted from the `acquisition date` field (YYYYMMDD format). Monthly counts reflect the date the mover record was acquired, which closely approximates the move date.

### Limitations
- The dataset captures *movers in motion* — households that changed address — not the full static El Paso population. It cannot measure net population change by neighborhood.
- Income estimates (FIND) are modeled, not self-reported, and carry inherent uncertainty.
- Housing size data (sq ft, bedrooms, baths) is available only for the subset of movers matched to MLS records (47% of total).
- Zip code centroids are used for all geographic bubble placement. Bubbles represent centroids, not precise addresses.
- The "California mover" analysis cannot distinguish between military PCS moves originating in California and purely civilian migration.

---

## Technical Stack

| Component | Technology |
|-----------|-----------|
| Story structure | Semantic HTML5, CSS custom properties |
| Charts & diagrams | [D3.js v7](https://d3js.org/) |
| Geographic maps | [Leaflet.js 1.9](https://leafletjs.com/) + [CARTO Light tiles](https://carto.com/basemaps/) |
| Typography | Playfair Display, Source Serif 4, DM Mono (Google Fonts) |
| Hosting | GitHub Pages |

The five geographic bubble maps use a D3 SVG overlay layer geo-registered to Leaflet, so bubbles stay spatially accurate as users pan and zoom. The military flow diagram uses a custom D3 split-panel canvas (not Leaflet) since it is a conceptual origin–destination schematic rather than a geographic map.

---

## Selected References

1. Rosenthal, S.S. (2014). "Are Private Markets and Filtering a Viable Source of Low-Income Housing?" *American Economic Review*, 104(2), 687–706.
2. U.S. Census Bureau. *American Community Survey 5-Year Estimates* (2022). El Paso city, Texas — median household income: $46,025. [census.gov](https://www.census.gov/quickfacts/fact/table/elpasocitytexas/INC110223)
3. UTEP Hunt Institute for Global Competitiveness. (2022). *Fort Bliss Economic Impact Report*. Estimates $8.7B annual contribution to El Paso regional economy.
4. Urban Institute Housing Finance Policy Center. (2024). *Housing Finance at a Glance*. VA loan market share data. [urban.org](https://www.urban.org/research/publication/housing-finance-glance-monthly-chartbook)
5. U.S. Census Bureau. (2023). *Characteristics of New Housing.* [census.gov](https://www.census.gov/construction/chars/highlights.html)
6. Molloy, R., Smith, C.L., & Wozniak, A. (2011). "Internal Migration in the United States." *Journal of Economic Perspectives*, 25(3), 173–196.
7. Military OneSource. *Understanding the PCS Move Process.* [militaryonesource.mil](https://www.militaryonesource.mil/moving-housing/moving/planning-your-move/understanding-the-pcs-move-process/)
8. Fort Bliss. *Installation Overview.* [bliss.army.mil](https://www.bliss.army.mil/About/)

---

*Analysis and visualization by [hoffmanap](https://github.com/hoffmanap). Data covers the El Paso metropolitan area. All income figures are modeled estimates.*
