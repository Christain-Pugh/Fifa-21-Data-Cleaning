# Fifa-21-Data-Cleaning
The following repository contains a data cleaning project I took on using the Kaggle Fifa 21 messy dataset.
As an aspiring data analyst I took this project on to show my data cleaning skills in Python.

Here are the steps I took to clean the data set.
1. The Club column had newline characters in almost every row. I wrote to replace any instance of "\n" with an empty space to make it more readable

2. The Weight column was divided up between weight measured in both lbs, and kgs. I wrote a loop that removes both "lbs", and "kg" from the rows then wrote a loop that converts all lbs to kg's to help keep the data more consistent. I also changed the data type to integer to make it easier to aggregate in the case of analysis.

3. The Height column had a similar issue with players height in both feet and cm's. As such I wrote code to remove the characters and convert all height to cm. I changed the data type to integer so that the data could be more easily aggregated.

4. The players Values in the Value column had all values shortened down for example one million euro would have been entered as "1M", This makes the numbers harder to aggregate and visualize if the data were to be used for analysis, so I removed the "M"'s and "K"'s and added a multiplication function to the code to bring all numbers to their true values.

5. I divided the Month, Day, and Year from the Joined column. This was more so done as an excercise in Python since the joined column had the dates represented as a mix of string, integer, and characters that would need seperated and removed in order to properly move all the data into seperate columns.

6. I used my convert_to_full_value function written earlier to conver the Wage of each player into an integer with no euro symbol, once again to assist in potential aggregation.

7. I then dropped the 'Weight_Value', 'Height_cm', 'Loan Date End', 'Unit', 'Converted_Weight', and 'Value' since they were no longer needed in my now cleaned data set.

8. Finally I used the dtypes function to insure that I had all my data types as what I wanted them to be, and used FileLink to downloada csv of the data set!
