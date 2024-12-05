# EV Data Analysis and Integration Guide

This guide will walk you through the process of running scripts and updating the CSV data model for EVs in Australia.

## Steps:

### 1. Rerun the following Python script to get a list of EVs in Australia
- **Data Source**: [Fuel Economy Data](https://www.fueleconomy.gov/feg/download.shtml)
- **Script**: Download the provided Python script and run it to fetch the EV data for Australia.
- **Command to run**: 
    ```bash
    python3 get_ev_list_australia.py
    ```

### 2. Find the list of the Most Popular EVs
- Use the sales data (by model, etc.) to find the most popular EVs and add this information to the CSV/Data Model for each vehicle type.
- **Run the following scripts**:

    - **EV Sales Analysis**: Split by AC & DC charging
        - [EV Sales Data (AC & DC)](https://github.com/Chameleon-company/EVAT-Data-Science/blob/main/personal-work/archive/pending/nirmal-antony-mariadoss/EV%20Sales%20in%20Australia%20from%202011%20to%202024.ipynb)
        - [Forecast Future EV Adoption Rates](https://github.com/Chameleon-company/EVAT-Data-Science/blob/main/personal-work/archive/pending/rose-mary-joy/Develop_Models_to_Forecast_Future_EV_Adoption_Rates.ipynb)
        
    - **Sales by type of EV & Charging Infrastructure**:
        - [EV Adoption Trends - Data Analysis](https://github.com/Chameleon-company/EVAT-Data-Science/blob/main/personal-work/archive/pending/shut-keung-chan/DataAnalysis_EV_adoption_trends.ipynb)
        - [EV Adoption Trends](https://github.com/Chameleon-company/EVAT-Data-Science/blob/main/personal-work/archive/pending/shut-keung-chan/EV_adoption_trends.ipynb)

### 3. Find the list of EV Connector types (Plugs)
- Add the connector type (plug type) for each vehicle to the CSV Data Model.
- You may need to use tools like co-pilot or other sources to gather these details into a list.

### 4. Ensure the following fields are contained in the final CSV Data Model
- The final CSV model should include both current fields and new fields for each vehicle type.

**Current fields** (these may need renaming to match the existing schema):
- `_id`, `model_release_year`, `make`, `model`, `variant`, `fuel_type`, `energy_consumption_whkm`, `electric_range_km`
  
**New fields to include**:
- `battery_capacity_kwh`: Total capacity of the vehicle's battery (kWh)
- `charge_rate_acceptance_kw`: Maximum rate at which the vehicle can accept a charge (kW)
- `charger_power_output_kw`: The power output capacity of the charger (kW)
- `charger_type`: Type of charger (AC/DC)
- `efficiency`: Charging efficiency (%)
- `desired_charge_level_kwh`: Target charge level (kWh)

- **Example usage**:
    ```python
    battery_capacity_kwh = 75  # kWh
    current_battery_level_kwh = 20  # kWh
    charge_rate_acceptance_kw = 50  # kW
    charger_power_output_kw = 100  # kW
    charger_type = "DC"  # AC or DC
    efficiency = 90  # %
    desired_charge_level_kwh = 60  # kWh
    ```

- **Fields for vehicle types**:
    - `ac_v2g`: "no"
    - `dc_v2g`: "no"

### 5. Use the New CSV Data Model to Develop PowerBI Dashboards
- Once the CSV Data Model is updated, use it to create PowerBI dashboards.
- This step will need to be done manually using PowerBI's interface.

### 6. Update the Documentation of the CSV Data Model
- After the new fields are added, update the documentation to reflect the changes in the data model and ensure consistency.

---

### Example Output
The final CSV data model should include detailed information about each EV, including its make, model, charging details, and connector type.

---

By following these steps, you'll be able to update the EV data model and develop comprehensive insights for EV adoption trends and infrastructure in Australia.

