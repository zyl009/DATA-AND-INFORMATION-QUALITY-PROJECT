# DATA-AND-INFORMATION-QUALITY-PROJECT
## Project Overview
This project focuses on data cleaning and preprocessing to improve data quality. The dataset used in this project contains 6094 rows and 22 columns, and various data quality issues such as missing values, redundancy, and inconsistencies were identified and addressed. The data pipeline involves multiple preprocessing steps to standardize, clean, and enhance the dataset for further analysis.

## Authors
- Zhongyou Liang 
- Alessandro Turazza 

## Project Structure
The project is structured as follows:

1. **Setup Choices**
   - Libraries and tools used
2. **Pipeline Implementation**
   - Data exploration
   - Data cleaning
     - Data transformation
     - Error detection & correction (missing values, outliers)
     - Data deduplication
3. **Results**
   - Improvements in data completeness, redundancy reduction, and data consistency

## Tools & Libraries Used
The following Python libraries were utilized:
- `pandas`: Data manipulation and cleaning
- `ydata-profiling`: Data profiling and exploratory analysis
- `spacy`: Text processing and entity extraction
- `recordlinkage`: Data deduplication and record matching
- `sklearn`: Machine learning for predictive imputation of missing values
- `re`: Regular expressions for text pattern matching
- `numpy`: Handling numerical computations

### Execution Environment
- Google Colab for running the scripts
- Google Drive for storing data

## Data Processing Steps
### Data Exploration
- Profiling dataset using `ydata-profiling`
- Identifying issues such as low uniqueness, missing values, redundancy, and inconsistencies

### Data Cleaning
#### Data Transformation
- Standardized date formats
- Removed unnecessary columns (e.g., Case Number.1, Case Number.2)
- Reformatted categorical fields (e.g., Country, Location, Activity)
- Normalized time values to HH:MM format
- Extracted meaningful information from complex fields
  
#### Handling Missing Values
- Forward-filling (`ffill`) for time-series data
- Mode imputation for categorical fields
- Mean imputation for numerical fields
- Replaced unknown values with appropriate placeholders
  
#### Outlier Detection & Correction
- Identified unrealistic date values (e.g., future years) and corrected them
- Adjusted inconsistent year values
  
#### Data Deduplication
- Used `recordlinkage` library for identifying duplicate records based on similarity scores
- Applied threshold-based matching to remove redundant entries

## Results
- **Completeness:** All missing values were handled, ensuring every column has valid data
- **Redundancy Reduction:** Removed unnecessary columns to streamline the dataset
- **Standardized Formats:** Improved consistency in date, time, and categorical values
- **Improved Data Quality:** Enhanced reliability for downstream analysis

## License
This project is open-source under the MIT License.
