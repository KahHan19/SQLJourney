# SQLJourney

Here, I include the journey and resources I used to self-learn HTML and CSS.

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


7. **LIKE** - Set a soft boundary
  - "%": Soft
  - "_": Strict

```sql
SELECT first_name, salary
FROM parks_and_recreation.employee_salary
....

WHERE first_name LIKE jer%
#output: Jerry

WHERE first_name LIKE %er%
#output: Jerry

WHERE first_name LIKE er%
#output: None

```







