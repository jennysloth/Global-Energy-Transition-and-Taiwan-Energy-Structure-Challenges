# Key Results

## Data Check

- Dataset: `World Energy Consumption.csv`
- Rows: 22,012
- Columns: 129
- Year range: 1900-2022
- Countries and regions: 306
- Selected research columns: 14

## Field Availability

- All requested research columns exist in the CSV; no substitute fields were used.

## Selected Column Types

| Column | Type |
|---|---|
| country | str |
| year | int64 |
| population | float64 |
| gdp | float64 |
| primary_energy_consumption | float64 |
| energy_per_capita | float64 |
| fossil_share_energy | float64 |
| renewables_share_energy | float64 |
| low_carbon_share_energy | float64 |
| coal_share_energy | float64 |
| oil_share_energy | float64 |
| gas_share_energy | float64 |
| greenhouse_gas_emissions | float64 |
| carbon_intensity_elec | float64 |

## Missing Value Ratio in Selected Columns

| Column | Missing % |
|---|---:|
| gas_share_energy | 78.25% |
| oil_share_energy | 78.25% |
| coal_share_energy | 78.25% |
| low_carbon_share_energy | 78.25% |
| renewables_share_energy | 78.25% |
| fossil_share_energy | 78.25% |
| carbon_intensity_elec | 76.54% |
| greenhouse_gas_emissions | 75.89% |
| energy_per_capita | 51.84% |
| gdp | 49.51% |
| primary_energy_consumption | 42.81% |
| population | 17.67% |
| country | 0.00% |
| year | 0.00% |

## Clean Analysis Datasets

- Global long-term trend: World, 1900-2022, 123 rows.
- Country comparison: World, Taiwan, Germany, China, Japan, United States, India, 2000-2022, 161 rows.
- 2022 cross-section: all countries and regions in 2022, 146 rows.
- Taiwan trend extrapolation: Taiwan, 2000-2022, 23 rows.
- K-means: removed missing values before clustering; 60 complete 2022 rows used. Variables were standardized with `StandardScaler`. K = 4.

## Required Numerical Results

| Item | Value |
|---|---:|
| World 2000 renewables_share_energy | 7.817% |
| World 2022 renewables_share_energy | 14.214% |
| Taiwan 2000 renewables_share_energy | 1.651% |
| Taiwan 2022 renewables_share_energy | 4.411% |
| Taiwan 2022 fossil_share_energy | 91.116% |
| World 2022 fossil_share_energy | 81.792% |
| Taiwan 2022 carbon_intensity_elec | 561.000 gCO2/kWh |
| World 2022 carbon_intensity_elec | 436.336 gCO2/kWh |
| Taiwan K-means cluster | 3 |
| Taiwan 2030 renewables_share_energy trend extrapolation | 3.583% |

## 2022 Renewables Share by Main Comparison Group

| Country/Region | renewables_share_energy |
|---|---:|
| Germany | 21.258% |
| China | 16.019% |
| World | 14.214% |
| Japan | 12.514% |
| United States | 11.317% |
| India | 10.402% |
| Taiwan | 4.411% |

## Notes for Interpretation

- The 2030 value is a simple linear trend extrapolation based on Taiwan's 2000-2022 renewables share. It should be interpreted as a trend reference, not a precise forecast.
- K-means cluster labels are numeric model labels. The meaning should be interpreted through the variables and relative positions in the PCA plot.
- Missing values were not imputed. Each analysis excludes rows with missing values only for the variables needed in that analysis.