# Car Sales Analysis Project

## Overview
This Jupyter Notebook analyzes car sales data to identify top-selling brands and clean key metrics for further analysis. The dataset includes details such as price, odometer readings, vehicle type, registration year, and more.

## Key Steps
1. **Data Loading & Encoding Fix**:  
   - Initially encountered a `UnicodeDecodeError` due to non-UTF-8 characters. Resolved by loading the CSV with `encoding="latin-1"`.

2. **Top-Selling Brands Identification**:  
   - Calculated brand distribution and filtered brands with >5% market share:  
     **Volkswagen, Opel, BMW, Mercedes-Benz, Audi, Ford**.

3. **Data Cleaning**:  
   - **Price**: Removed `$` and commas, converted to integer (e.g., `$5,000` → `5000`).  
   - **Odometer**: Removed `km` and commas, converted to integer (e.g., `150,000km` → `150000`).  
   - Renamed columns for clarity: `price` → `price ($)`, `odometer` → `odometer (km)`.

4. **Filtered Dataset**:  
   - Focused on 34,073 entries from the top 6 brands (original dataset: 50,000 entries).

## Key Findings
- **Top Brands**: Volkswagen dominates with ~21.4% market share.
- **Data Structure**: Includes features like `vehicleType`, `fuelType`, `gearbox`, and `yearOfRegistration`, enabling deeper analysis of pricing trends.

## Future Work
- Handle missing values (e.g., `notRepairedDamage`).
- Explore relationships between price, mileage, age, and fuel type.
- Visualize trends (e.g., price distribution by brand, mileage vs. age).

## Usage
1. **Prerequisites**:  
   - Install pandas: `pip install pandas`.
   - Ensure `cars.csv` is in the project directory.

2. **Run the Notebook**:  
   The code is fully documented. Key sections include data loading, cleaning, and brand analysis.

---

**Note**: The dataset (`cars.csv`) is not included in this repository. Ensure you have the file to replicate the analysis.  
For questions or contributions, feel free to open an issue or submit a pull request.