1) Rerun the following (attached) python script to get a list of EV's in Australia. ( Details within the file).
Data Source : https://www.fueleconomy.gov/feg/download.shtml
 
2) Find the list of the Most popular EV's ( from sales data by model etc). Add this to the CSV/Data Model for each vehicle type.
Can re-run the following scripts. Split into AC & DC
EV Sales
https://github.com/Chameleon-company/EVAT-Data-Science/blob/main/personal-work/archive/pending/nirmal-antony-mariadoss/EV%20Sales%20in%20Australia%20from%202011%20to%202024.ipynb
https://github.com/Chameleon-company/EVAT-Data-Science/blob/main/personal-work/archive/pending/rose-mary-joy/Develop_Models_to_Forecast_Future_EV_Adoption_Rates.ipynb
 
Sales by type of EV & Charging infrastructure
https://github.com/Chameleon-company/EVAT-Data-Science/blob/main/personal-work/archive/pending/shut-keung-chan/DataAnalysis_EV_adoption_trends.ipynb
https://github.com/Chameleon-company/EVAT-Data-Science/blob/main/personal-work/archive/pending/shut-keung-chan/EV_adoption_trends.ipynb
 
3) Find the list of the EV Connector type (plug) for each vehicle. Add this to the CSV Data Model for each vehicle type.
You may need to use co-pilot or other to gather these details into a list.
 
4) Ensure the following fields are contained in the Final CSV data model . Fields from Current Data Schema Current ( you make need to rename to existing fields to these) + new fields.
 
"_id": {
    "$oid": "66d7e0f5cdf87e8b5d63de6c"
  },
  "model_release_year": 2023,
  "make": "MG",
  "model": "MG4",
  "variant": "64kWh EV RWD ",
  "fuel_type": "Pure Electric",
  "energy_consumption_whkm": 130,
  "electric_range_km": 535,
 
*https://github.com/Chameleon-company/EVAT-Data-Science/blob/main/personal-work/archive/pending/harold-parappillil-sunny/Estimated_time.ipynb
    Parameters:
    - battery_capacity_kwh: Total capacity of the vehicle's battery (kWh)
    - charge_rate_acceptance_kw: Maximum rate at which the vehicle can accept a charge (kW)
    - charger_power_output_kw: The power output capacity of the charger (kW)
    - charger_type: Type of charger (AC/DC)
    - efficiency: Charging efficiency (%)
    - desired_charge_level_kwh: The target charge level you want to reach (kWh)
# Example usage:
battery_capacity_kwh = 75  # kWh
current_battery_level_kwh = 20  # kWh
charge_rate_acceptance_kw = 50  # kW
charger_power_output_kw = 100  # kW
charger_type = "DC"  # AC or DC
efficiency = 90  # %
desired_charge_level_kwh = 60  # kWh
 
"ac_v2g": "no",
"dc_v2g": "no",
 
5) Use New CSV Data Model to develop PowerBI Dashboards
 
6)Update the Documentation of the CSV Data Model
