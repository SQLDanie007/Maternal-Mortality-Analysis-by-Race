# Maternal Mortality Analysis by Race

## Project Overview
This project investigates maternal mortality rates during childbirth with a specific focus on racial disparities. The analysis highlights the significantly higher mortality rate among African American mothers compared to other racial groups. The data is analyzed using SQL to create a table, calculate death rates, and identify races with mortality rates above the average.

## Database Schema
The project includes the following table:

### `MaternalMortality`
| Column               | Data Type   | Description                                           |
|----------------------|-------------|-------------------------------------------------------|
| `Race`               | VARCHAR(50) | The race or ethnicity of the mothers                  |
| `Number_of_Deaths`   | INT         | The number of deaths during childbirth                |
| `Total_Births`       | INT         | The total number of births for that racial group      |
| `Death_Rate_per_1000`| FLOAT       | The maternal death rate per 1000 births               |

## SQL Queries
The project involves several key SQL operations:

### 1. **Table Creation and Data Insertion**
This query creates the `MaternalMortality` table and inserts data:

```sql
CREATE TABLE MaternalMortality (
    Race VARCHAR(50),
    Number_of_Deaths INT,
    Total_Births INT,
    Death_Rate_per_1000 FLOAT
);

INSERT INTO MaternalMortality (Race, Number_of_Deaths, Total_Births, Death_Rate_per_1000) VALUES
('African American', 120, 1000, 120.0),
('Caucasian', 50, 1200, 41.67),
('Hispanic', 40, 1100, 36.36),
('Asian', 30, 800, 37.5),
('Other', 20, 600, 33.33);
