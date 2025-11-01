# Time Zone-Based Sales Performance Analysis

## Overview

This project analyzes sales data from various retailers operating in different time zones (EST, CET, Australia/West) to understand sales patterns and revenue distribution. The analysis handles timezone conversions using the `pytz` module and performs comprehensive data manipulation with pandas.

## Main Objective

Obtain information about product sales across various retailer types in UTC offset and display the average amount of sales that occurred in each time zone.

## Dataset

The analysis uses `Sales-products-tz-mod.csv` containing:
- **RetailerCountry**: Country where the sale occurred
- **RetailerType**: Type of retailer (Outdoors Shop, Sports Store, Department Store, Discount Retailer)
- **Product**: Product name
- **Sales Revenue ($)**: Revenue from the sale
- **DateOfSale**: Date of the transaction
- **TimeOfSale**: Time of the transaction
- **TimeZone**: Time zone of the sale (EST, CET, Australia/West)

## Analysis Workflow

### Task 1: Data Preparation
- Combine date and time values into a single "MOS" (Moment of Sale) column
- Verify that time zone values are valid and compatible with the pytz module
- Convert string timestamps to datetime objects using `pd.to_datetime()`

### Task 2: Data Manipulation
- Calculate UTC offset for each sale
- Store offset values in an "OffsetUTC" column
- Handle timezone-aware datetime conversions using pytz

### Task 3: Data Analysis
- Order all sales by UTC-equivalent timestamps
- Analyze sales patterns across different time zones
- Compare revenue distribution by retailer type and location

### Task 4: Data Visualization
- Generate statistics on sales by time zone
- Create visualizations to illustrate sales patterns
- Display average sales amounts per time zone

## Technologies Used

- **Python 3.x**
- **pandas**: Data manipulation and analysis
- **pytz**: Timezone handling and conversions
- **datetime**: Date and time operations
- **matplotlib**: Data visualization

## Getting Started

### Prerequisites

```bash
pip install pandas pytz matplotlib
```

### Running the Analysis

1. Ensure `Sales-products-tz-mod.csv` is in the same directory
2. Open the Jupyter notebook:
   ```bash
   jupyter notebook "Sales Data Analysis Across Different Time Zone.ipynb"
   ```
3. Run all cells sequentially to perform the complete analysis

## Key Features

- Timezone validation and conversion
- UTC offset calculation
- Cross-timezone sales comparison
- Revenue analysis by retailer type
- Statistical summaries and visualizations

## Results

The analysis provides insights into:
- Sales distribution across different time zones
- Average revenue by retailer type
- Temporal patterns in sales data
- Geographic sales performance

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
