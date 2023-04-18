This script is designed to:
  1. **Extract** specific information from the /etc/passwd file
  2. **Transform** it into CSV format, and then 
  3. **Load** it into a table called 'users' in a PostgreSQL database.

The script first extracts the user name, user id, and home directory path of each user account defined in the /etc/passwd file using the 'cut' command. The extracted data is saved to a text file named "extracted-data.txt".

Next, the script transforms the extracted data into CSV format by replacing the ':' delimiter with a ',' delimiter using the 'tr' command. The transformed data is then saved to a CSV file named "transformed-data.csv".

Finally, the script loads the transformed data from the CSV file into a table called 'users' in the PostgreSQL database. This is done using the 'psql' command and the COPY command to copy the data from the CSV file into the table.


There's an article about the same on my medium page, [here](https://medium.com/@anwangari/a-begginers-guide-to-etl-using-shell-scripts-bb488029463d).
