# EV-Charging-Analysis
 
This code performs an analysis of energy prices based on a dataset containing energy price information. The data is loaded into a DataFrame named df_energyPrice using the Pandas library. The code calculates the utilization of charging points based on the ratio between the number of cars and the number of charging points. It then filters the dataset based on a specific date range, considering only weekdays (Monday to Friday) and the specified charging start and end hours. The code also calculates the charging power, charging volume, and time required to charge all cars. It then computes the charging consumption based on the charging time and the corresponding energy price.

Next, the code defines two functions, calculate_consumption_above1 and calculate_consumption_below1, to calculate the charging consumption based on whether the number of hours is greater than or less than 1. These functions iterate over the rows of the DataFrame and calculate the consumption for the hours within the integer and decimal parts of the charging time.

Next, the code defines the calculate_normal_consumption function to calculate the normal consumption based on the integer and decimal parts of the charging time. It rounds the decimal values, creates the 'normal consumption' column, and fills the values based on conditions.

Finally, the code converts the 'Hour' column to a string data type, creates a new column named 'DateTime' by concatenating the 'Date' and 'Hour' columns, converts the 'DateTime' column to a datetime data type, and redefines the DataFrame index.

Main objectives:

- Create a normal ('dumb') charge profile
- Make the charging profile smart based on Day-Ahead electricity price
- Calculate the cost saving for purchase of energy