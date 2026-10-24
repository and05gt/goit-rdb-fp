# Final Project

## Description of the Final Project

1. Load the data:

- Create the `pandemic` schema in the database using an SQL command.
- Set it as the default schema using an SQL command.
- Import the data using the Import Wizard, just as you did in Lesson 3.
- Review the data to get a sense of the context.

  ! As you can see, the Entity and Code attributes are repeated throughout the data. Eliminate this redundancy by normalizing the data.

2. Normalize the `infectious_cases` table to third normal form. Save the two tables with the normalized data in the same schema.

! Run the query `SELECT COUNT(*) FROM infectious_cases` so that your mentor can see how many records you loaded into the database from the file.

3. Analyze the data:

- For each unique combination of `Entity` and `Code` or their `id`, calculate the average, minimum, maximum, and sum for the `Number_rabies` attribute.

  ! Note that the `Number_rabies` attribute may contain empty values `""` — you must filter these out first.

- Sort the result by the calculated average in descending order.
- Select only 10 rows to display on the screen.

4. Create a column showing the difference in years.

For the original or normalized table, use built-in SQL functions to create the following for the `Year` column:

- an attribute that creates the date of January 1 of the corresponding year,

  ! For example, if an attribute contains the value '1996', then the value of the new attribute should be '1996-01-01'.

- an attribute equal to the current date,
- an attribute equal to the difference in years between the two columns mentioned above.

  ! You do not need to recalculate any other attributes, such as `Number_malaria`.

  ! To find the necessary built-in functions, you may need to refer to the material for Topic 7.

5. Create your own function.

- Create and use a function that constructs the same attribute as in the previous exercise: the function should take the year as input and return the difference in years between the current date and the date created from the year attribute (1996 → '1996-01-01').
