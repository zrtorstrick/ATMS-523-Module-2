# ATMS 523 Weather and Climate Data Analytics - Module 2

**Project 2: Dask & Xarray for Computing Weather and Climate Diagnostics**  
**ERA-5 Precipitation Analysis**

## Overview

This project analyzes ERA-5 reanalysis precipitation data using Dask and Xarray to compute weather and climate diagnostics. The analysis focuses on extreme precipitation events in the Seattle region and their associated patterns across the continental United States.

## Assignment Components

### 1. Regional Precipitation Analysis
- **Location**: Seattle, WA (47.6061°N, 122.3328°W)
- **Spatial Domain**: 5° × 5° grid box around Seattle
- **Temporal Period**: 1991-2020 (30 years)
- **Analysis**: Daily precipitation time series and 95th percentile threshold

### 2. Extreme Event Identification
- **Method**: Cumulative Distribution Function (CDF) analysis
- **Threshold**: 95th percentile of daily regional mean precipitation
- **Result**: 548 extreme days identified (top 5% of precipitation days)
- **Threshold Value**: 18.17 mm/day

### 3. Composite Analysis
- **Spatial Domain**: Continental United States
- **Analysis**: Composite mean precipitation during extreme Seattle events
- **Comparison**: Anomaly from 1981-2020 climatological mean
- **Visualization**: Cartopy maps with geographic features

## Installation and Setup

### Prerequisites
- Python 3.8+
- Conda or Mamba package manager

### Environment Setup

**Option 1: Using Conda/Mamba (Recommended)**
```bash
# Create environment from specification file
mamba env create --prefix $HOME/envs/xarray-climate -f environment.yml
mamba activate $HOME/envs/xarray-climate
```

**Option 2: Using pip**
```bash
# Create virtual environment
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
```

### Required Packages
- `xarray`: Multi-dimensional data arrays
- `dask`: Parallel computing
- `cartopy`: Geographic mapping
- `matplotlib`: Plotting and visualization
- `numpy`: Numerical computing
- `pandas`: Data manipulation
- `netCDF4`: NetCDF file handling

## Usage

### Running the Analysis

1. **Start Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```

2. **Open HW02.ipynb** and run cells sequentially

3. **Dask Dashboard**: Monitor parallel processing at the provided URL

### Data Files

- **Large datasets** are automatically downloaded from cloud sources
- **Processed data** is cached locally as NetCDF files
- **Data files** are excluded from git tracking (see `.gitignore`)

## License

See LICENSE file for details.

## Contact

**Student**: Zachary R. Torstrick  
**Course**: ATMS 523 Weather and Climate Data Analytics  
**Institution**: University of Illinois Urbana Champaign