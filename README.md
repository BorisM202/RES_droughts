# RES_droughts

This repository contains the code and data used for the analysis and figure generation in the paper:

**Reducing RES Droughts through the integration of wind and solar PV** <br>
*Boris Morin, Aina Maimó Far, Damian Flynn, Conor Sweeney* <br>
2025, *Renewable Energy* <br>
DOI: 10.1016/j.renene.2025.123392 <br>
https://www.sciencedirect.com/science/article/pii/S0960148125010547#da1  <br>


## Repository sctructure

### Data

- `cf_analysis_1979-2023.csv`: 

Contains hourly capacity factor (CF) values from 1979-01-01 to 2023-12-31 for wind and solar PV across three datasets: ATL, C3S GRD, and C3S NAT. Also includes combined RES CF, computed as a capacity-weighted average of wind and solar PV using their respective installed capacities for two different scenarios. 

- `cf_verification_2018-2023.csv`

Contains hourly CF values of actual generation for wind and solar PV from 2014 to 2023, as well as modelled values from the three datasets.

- `power_curve.csv`

Contains wind turbine power curve values from 0 to 40 m/s for the Enercon E112-4500 turbine (data from Renewables.ninja) used by ATL and the Vestas V136-3450 turbine (data from thewindpower.net, linearly interpolated at 0.01 m/s intervals) used by C3S.

### Scripts
Each script corresponds to a figure or analysis in the study.

- `01_methodology_identification.ipynb`
Demonstrates method to identification RES drought event.
- `02_verification_violin.ipynb`
Creates violin plots showing the distribution of CF values for wind and solar PV across datasets.
- `03_verification_power_curve.ipynb`
Compares power curves and shows wind generation distributions.
- `04_verification_wind_contour.ipynb`
Generates 2D density contour plots comparing wind CF (datasets vs observation).
- `05_verification_wind_number_events.ipynb`
Plots the average annual number of wind drought events for different durations from 2014–2023.
- `06_verification_solar_contour.ipynb`
Generates 2D contour plots comparing solar PV CF (datasets vs observation)
- `07_verification_solar_number_events.ipynb`
Plots the annual number of solar PV drought events for the year 2023.
- `08_analysis_number_events.ipynb`
Compares the average number of annual RES drought events of different durations for wind, solar PV, and different combinations of the two.
- `09_analysis_return_periods.ipynb`
Calculates and plots return periods of RES drought durations for wind, solar PV, and different combinations of the two.
- `10_analysis_seasonality.ipynb`
Examines the seasonality of RES droughts by showing the monthly share of RES drought occurrence.


## Notes
Drought events are defined based on periods where the CF falls below a fixed threshold of 0.1 for a duration of 24 hours.

The installed capacities used for RES combination scenarios (in GW):
| Source    | W91–PV9 | W57–PV43 |
|-----------|---------|----------|
| Solar PV  |  0.58   |   8.60   |
| Wind      |  5.92   |  11.45   |
