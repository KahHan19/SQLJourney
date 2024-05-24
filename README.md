# SQLJourney

Here, I include the journey and resources I used to self-learn SQL.

## Resources Used
1. MySQL
2. GitHub Desktop (For code upload)

---

## Beginner Notes

- Most commands such as `SELECT`, `DISTINCT`, and others are not case sensitive.

### Basic SQL Commands
1. **SELECT** - Allows you to select the specific column of interest (`*` selects all columns).
2. **FROM** - Specifies the dataset from which you are extracting information.
3. **";"** - Represent end of code.

#### Example:

```sql
SELECT * FROM parks_and_recreation.employee_salary;
SELECT first_name, salary, salary*2 FROM parks_and_recreation.employee_salary;
````

The second line showcases extract specific column such as first_name, salary and the value of salary*2. ( In another words it enables addition column with extract processing. )

4. **Where** - Similar to "IF" in python, it sets addition contraint on what infromation to display.

```sql
SELECT first_name, salary
FROM parks_and_recreation.employee_salary
WHERE salary > 70000;

Output:
1	Leslie	Knope	  Deputy Director of Parks and Recreation	75000	  1
8	Chris	  Traeger	City Manager	                          90000	  3
```

5. **Logic Statements** - Similar to conditional statemetn in Python, "AND, OR and NOT"<br>


6. **LIKE** - Set a Softer condition
  - "%": Soft 
  - "_": Strict

```sql
SELECT first_name, salary
FROM parks_and_recreation.employee_salary
....

WHERE first_name LIKE jer%
#output: Jerry ( Jerry is the only name in the dataset with "jer" - something )

WHERE first_name LIKE %er%
#output: Jerry ( Jerry is the only name in the dataset with "something" - er - "something

WHERE first_name LIKE er%
#output: Error ( No name in the dataset starts with "er" )

WHERE first_name LIKE Jer__
#output: Jerry ( Jerry is the only name in the dataset with "Jer" follow by 2 character )

WHERE first_name LIKE Jer_
#output: Error ( No name in the dataset starts with "Jer" fllow by 1 character )

```


7. **GROUP BY** - Group Distinvt values in a column and compile it
```sql
SELECT gender, avg(age) AS avg_age
FROM parks_and_recreation.employee_demographics
GROUP BY gender

#output:

Gender    ave_age
Female    38.50000
Male      41.2857
````

Firstly dont make stupid mistake like me, where is the ";" !!!
We first group all the rows by gender and we average all the values with gender = male or female


9. **ORDER BY** - Sort the dataset, ASC(ascending) or DESC(descending)

10. **HAVING** - Similar to "WHERE" but comes after "GROUP BY"

11. **LIMIT** - Limit the data shown




