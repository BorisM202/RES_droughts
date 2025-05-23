# RES_droughts

This repository contains the analysis and generates figures for the paper:
**Reducing RES Droughts through the integration of wind and solar PV**, Boris Morin, Aina Maimó Far, Damian Flynn, Conor Sweeney
2025, *Renewable Energy*, DOI: ...


## Sctructure

### Data

- `cap_solar_2017-2023.csv`: Contains information on solar PV farms in Republic of Ireland and Northern Ireland. The location have been determined by the authors from manual search, the remaining columns can be found on: https://www.eirgrid.ie/grid/system-and-renewable-data-reports 
- `cap_wind_1990-2023.csv`: Contains information on wind farms in Republic of Ireland and Northern Ireland. The location have been determined by the authors from manual search, the remaining columns can be found on: https://www.eirgrid.ie/grid/system-and-renewable-data-reports 
- `cf_combine_1979-2023.csv`: Contains capacity factor values from 1979-01-01 to 2023-12-31 for the three datasets compared in the study (ATL, C3S GRD, C3S NAT) for wind and solar PV. There are also a combination of wind and solar PV which is obtained by doing a weighted average of the the capacity factor for wind and solar PV and using the total installed capacity of the respective source. 
- `cf_solar_2018-2023.csv`: Contains solar PV capacity factor values from 2018-01-01 to 2023-12-31 for the three datasets compared in the study (ATL, C3S GRD, C3S NAT) for wind and solar PV.
- `cf_wind_2014-2023.csv`:
- `gen_solar_2018-2023.csv`:
- `gen_wind_2014-2023.csv`:
- `power_curve.csv`:

### Scripts

- `01_methodology_identification.ipynb`: Plot time series of wind capacity factor to illustrate the identification procedure
- `02_verification_violin.ipynb`:
- `03_verification_power_curve.ipynb`:
- `04_verification_wind_contour.ipynb`:
- `05_verification_wind_number_events.ipynb`:
- `06_verification_solar_contour.ipynb`:
- `07_verification_solar_number_events.ipynb`:
- `08_analysis_number_events.ipynb`:
- `09_analysis_return_periods.ipynb`:
- `10_analysis_seasonality.ipynb`: