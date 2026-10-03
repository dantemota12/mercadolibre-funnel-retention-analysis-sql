# MercadoLibre Conversion Funnel & Retention Analysis with SQL
Analyzed 2025 MercadoLibre funnel conversion and user retention across 10 Latin American countries with SQL.

## Objective
Identify where users drop off in the purchase funnel and how well they are retained over time, overall and by country and sign-up cohort, to guide conversion and retention improvements.

## Business Questions
1. Between 01/01/2025 and 08/31/2025, what is the conversion rate between each key funnel stage, where is the biggest drop, and how does it vary by country?
2. For users who signed up between 01/01/2025 and 06/01/2025, what are the retention rates at D7, D14, D21 and D28, and how do they vary by country?

## Tools
SQL · Spreadsheets · Funnel Analysis · Cohort Analysis

## Dataset
Two tables, `mercadolibre_funnel` (user events by funnel stage) and `mercadolibre_retention` (user return activity after sign-up), covering 10 Latin American countries in 2025.

## Overall Funnel (% of users reaching each stage)
| select_item | add_to_cart | begin_checkout | add_shipping_info | add_payment_info | purchase |
|---|---|---|---|---|---|
| 76.90% | 11.01% | 4.00% | 2.42% | 2.09% | 1.25% |

## Purchase Conversion by Country
| Country | Purchase conversion |
|---|---|
| Uruguay | 4.55% |
| Bolivia | 3.23% |
| Mexico | 2.48% |
| Peru | 1.82% |
| Argentina | 1.25% |
| Chile | 1.03% |
| Brazil | 0.68% |
| Ecuador | 0.00% |
| Colombia | 0.00% |
| Paraguay | 0.00% |

## Retention by Country
| Country | D7 | D14 | D21 | D28 |
|---|---|---|---|---|
| Brazil | 87.2% | 54.4% | 24.4% | 2.5% |
| Mexico | 86.1% | 55.8% | 25.5% | 3.1% |
| Uruguay | 86.1% | 48.8% | 23.0% | 2.5% |
| Argentina | 85.1% | 52.3% | 22.5% | 1.8% |
| Colombia | 84.5% | 52.0% | 21.8% | 1.6% |
| Peru | 84.3% | 51.1% | 22.9% | 3.2% |
| Chile | 83.7% | 51.8% | 22.1% | 1.7% |
| Paraguay | 80.9% | 49.1% | 22.1% | 2.1% |
| Bolivia | 80.8% | 46.8% | 19.2% | 2.5% |
| Ecuador | 79.1% | 50.0% | 20.6% | 2.5% |

## Key Findings
1. **The biggest funnel drop is between viewing a product and adding it to the cart**: of every 100 users who enter, about 11 add something to the cart and only 1.25 complete a purchase.
2. **Uruguay (4.55%), Bolivia (3.23%) and Mexico (2.48%)** lead final conversion. **Paraguay, Colombia and Ecuador** have 0% completed purchases, which points to market-specific issues such as payment methods or delivery coverage.
3. **Retention drops sharply by day 28 in every country.** Brazil leads at D7 (87.2%), Mexico leads at D14 and D21, Peru is best at D28 (3.2%) and Colombia is the lowest (1.6%).
4. **Monthly cohorts from January to July follow the same pattern** (D7 between 85.9% and 87.7%, D28 between 2.0% and 3.0%). The **August 2025 cohort** shows the lowest retention at every checkpoint (70.8% at D7, 0.2% at D28). This should be validated, since users who signed up late in the data window had limited time to reach D28.

## Recommendations
- Run A/B tests on the product page (higher-quality images, more prominent buy buttons) to reduce the drop before add-to-cart.
- Simplify checkout with address autofill and saved payment methods, and incentivize first purchases with discounts.
- Review payment methods and delivery coverage in Paraguay, Colombia and Ecuador before investing more in user acquisition there.
- Replicate what works in Uruguay and Bolivia, and make small improvements at every funnel stage in Mexico, where volume makes the impact significant.
- Launch reactivation campaigns between D14 and D21 (personalized offers, notifications about viewed products, follow-up emails), prioritizing Colombia.
- Audit the August 2025 cohort to confirm whether the drop is real churn or a data-window effect.

## Files
- `sprint_4_-_Proyecto_4__Análisis_de_embudo_y_retención_para_MercadoLibre_-_Resumen_ejecutivo.xlsx`: funnel and retention results, and executive summary.
- `images/`: screenshots of the charts and results.
- [View the Google Sheet](https://docs.google.com/spreadsheets/d/1pDodRnb3y4NKdYor9KCD9TubbbHr2UFo/edit?usp=sharing&ouid=116118350435914609784&rtpof=true&sd=true)
