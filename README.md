# Time series forecasting of energy production based on solar panels in Poland
## Project

Project has two stages:
1. ETL data from public site: https://monitoringpublic.solaredge.com/solaredge-web/p/home/public?locale=en_US - scrapper code is not part of this repository
2. Build a timeseries forecasting model using Temporal Fusion Transformer (https://pytorch-forecasting.readthedocs.io/en/stable/tutorials/stallion.html)

## Data model
Shape: 10_583_968 rows and 16 columns

|    | measure_time        |   panel_id | city             |   tilt |   azimuth |   latitude |   longitude |    altitude | sun_azimuth |   production_w |   temperature |   wind_speed |   surface_solar_radiation |   surface_direct_solar_radiation |   surface_diffuse_solar_radiation |   surface_thermal_radiation |
|---:|:--------------------|-----------:|:-----------------|-------:|----------:|-----------:|------------:|------------:|------------:|---------------:|--------------:|-------------:|--------------------------:|---------------------------------:|----------------------------------:|----------------------------:|
|  0 | 2018-10-09 19:00:00 |    1119730 | Kliniska Wielkie |     30 |       180 |    53.4609 |     14.7739 | -24.3633    |     293.806 |              0 |         12.22 |         2.42 |                         0 |                             0    |                                 0 |                         302 |
|  1 | 2018-11-17 15:00:00 |    1119730 | Kliniska Wielkie |     30 |       180 |    53.4609 |     14.7739 |  -0.0907536 |     237.803 |              0 |          5.26 |         1.92 |                       120 |                            76.18 |                                44 |                         237 |
|  2 | 2018-12-08 15:00:00 |    1119730 | Kliniska Wielkie |     30 |       180 |    53.4609 |     14.7739 |  -2.94042   |     234.476 |              0 |          7.53 |         8.07 |                        35 |                             0.23 |                                36 |                         311 |
|  3 | 2018-12-31 19:00:00 |    1119730 | Kliniska Wielkie |     30 |       180 |    53.4609 |     14.7739 | -35.475     |     278.856 |              0 |          4.62 |         3.86 |                         0 |                             0    |                                 0 |                         331 |
|  4 | 2019-01-25 23:00:00 |    1119730 | Kliniska Wielkie |     30 |       180 |    53.4609 |     14.7739 | -55.2943    |     354.505 |              0 |         -4.34 |         2.86 |                         0 |                             0    |                                 0 |                         263 |

## Tech stack
python, pandas, pytorch-forecasting etc. 