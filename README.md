README – Human Resources ERD

This ERD represents a Human Resources system that manages employees, branches, roles, salaries, and training programs.

Main entities:

- Employee: represents workers in the company. Each employee has an employee_id (primary key), first_name, last_name, email, phone, and date.

- Branch: represents company locations. Each branch has branch_id, branch_name, address, and city.

- Role: defines employee roles in the company. Each role has role_id, role_name, and description.

- Salary: stores salary payments. Each record includes salary_id, amount, and payment_date.

- Training: represents training programs. Each training has training_id, name, cost, and final_date.


Relationships:

- Works_In: connects Employee to Branch (each employee works in a branch).
- Has_Role: connects Employee to Role (each employee has a role).
- Receives: connects Employee to Salary (employees receive salaries).
- Takes_Training: connects Employee to Training (employees can take training programs).


Note about JSON field:

In the database implementation, the Employee entity may include an additional JSON field that stores personal information.

This JSON field contains:
- firstName
- lastName
- dateOfBirth
- email
- phone

Example:

{
  "firstName": "Esther",
  "lastName": "Abergel",
  "dateOfBirth": "2000-05-14",
  "email": "esther@example.com",
  "phone": "0521234567"
}

Since ERDPlus does not support JSON attributes directly, this field is not represented in the diagram and is described here as an implementation detail.
