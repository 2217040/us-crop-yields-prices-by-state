# US crop yields, prices and production by state (USDA NASS)

State-level USDA NASS statistics for corn, soybeans, wheat, cotton and sorghum, as clean CSV files: yields per acre with the US average and whether the figure is a forecast or final; monthly prices received and marketing-year averages; production with planted and harvested acres.

Maintained by **[GreenMatrix (greenmatrix.digital)](https://greenmatrix.digital/)**. The files are the same numbers the site shows; the site refreshes them from USDA NASS Quick Stats every day, and a GitHub Action copies them here every week.

## Files

### `data/crop-yields.csv` — yields by state, 2020 onward

Live version: <https://greenmatrix.digital/data/crop-yields.csv> · shown on <https://greenmatrix.digital/crop/>

| Column | Meaning |
|---|---|
| `state`, `state_code` | State name and two-letter code |
| `crop` | Corn, Soybeans, Wheat, Cotton or Sorghum |
| `year` | Crop year |
| `yield`, `unit` | Yield per harvested acre (bu/acre; cotton lb/acre) |
| `us_average` | US yield for the same crop and year |
| `usda_period`, `is_forecast` | USDA reference period (`YEAR` = final estimate, `YEAR - <MONTH> FORECAST` = in-season forecast) |
| `page` | Page on greenmatrix.digital for this state and crop |

### `data/crop-prices.csv` — prices received by state, 2020 onward

Live version: <https://greenmatrix.digital/data/crop-prices.csv> · shown on <https://greenmatrix.digital/prices/>

| Column | Meaning |
|---|---|
| `state`, `state_code`, `crop`, `year` | As above |
| `month`, `price_type` | Month 1–12 for `monthly` prices; empty for the `marketing-year average` |
| `price`, `unit` | Price received by farmers ($/bu; cotton $/lb) |
| `us_average` | US price for the same crop and period |
| `page` | Page on greenmatrix.digital for this state and crop |

### `data/crop-production.csv` — production and acres by state, 2007 onward

Live version: <https://greenmatrix.digital/data/crop-production.csv> · shown on <https://greenmatrix.digital/rankings/>

| Column | Meaning |
|---|---|
| `state`, `state_code`, `crop`, `year` | As above |
| `production`, `production_unit` | Total production (bu; cotton 480-lb bales) |
| `area_planted_acres`, `area_harvested_acres` | Acres planted and harvested |
| `yield`, `yield_unit`, `usda_period` | Yield and USDA period, as in the yields file |

## Notes

- Source: [USDA NASS Quick Stats](https://quickstats.nass.usda.gov/), state level. A state appears for a crop only where NASS publishes it.
- The latest year can be an in-season forecast; USDA revises forecasts and earlier estimates, and this copy follows those revisions.
- Not every state has every crop or every month: NASS publishes prices only for major producing states.

## License and attribution

The underlying USDA NASS statistics are in the public domain. This compilation is published under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — free to use, share and adapt, including commercially, with attribution:

> Source: GreenMatrix (greenmatrix.digital), from USDA NASS Quick Stats — https://greenmatrix.digital/crop/

Spotted a wrong value? Open an issue with a link to the USDA source.
