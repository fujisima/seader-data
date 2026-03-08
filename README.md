# seader-data

Versioned municipal datasets for demographic and social analysis in Brazil.

This repository stores the data files used by the **seader** R package.  
Datasets are distributed through GitHub Releases in **Parquet format** for efficient storage and fast access.

The goal of this repository is to keep data files separate from the R package source code, making the package lightweight while providing stable and versioned data access.

## Available datasets

Current datasets focus on **live births in the state of São Paulo**.

- **birth-sex.parquet**  
  Live births by sex and municipality (2019–2025).

- **birth-age.parquet**  
  Live births by mother's age group and municipality (2000, 2010, 2023–2025).

## Data structure

- **Unit of analysis:** Municipality (IBGE code)
- **Geographic coverage:** State of São Paulo, Brazil
- **File format:** Parquet
- **Access pattern:** Lazy access via Apache Arrow

## Accessing the data

The datasets are intended to be accessed through the **seader** R package.

Example:

```r
library(seader)

births <- read_birth_sex(year = 2025)
