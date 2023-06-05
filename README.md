# staffhierarchy
PowerBI used to draw staff hierarchy for the Human Resource Database obtained from Kaggle (https://www.kaggle.com/datasets/ogbuzurukelechi/human-resource-dataset).

The following steps were followed to clean, transform and analyze data:

Step 1: Data cleaning issues: 

i. Space after names making matching names difficult
ii. Different IDs given to the same manager
iii. Some managers missing in the employee list
iv. Manager's name was formated idfferently than employee's name

N.B: all these issues were addressed before proceeding to the transformation stage

Step 2: Data Transformation

i. While there are managers that are themselves employees, ManagerID and EmployeeID were not linked.
ii. After linking the two IDs using merge function by matching name of managers with employees, EmployeeID for employees that are also managers was assigned as managers ID. Merge function was used to assign employee ID in place of MannagerID for employees who are managers.
iii. Manager ID was maintained if a manager didn't have a boss.
iv. CEO was introduced in the staff list to ensure that all employees have a boss except for the CEO including board of directors.
v. Finally, serial number of employee ID was reset starting 1. Manager's IDs was updated accordingly.

Step 3: Analysis and Visualization
Hierarchy Chart by Akvelon was used to draw staff hierarchy. 

![image](https://github.com/KesetebirhanDelele/staffhierarchy/assets/109861849/2ccbdfd8-e58d-4586-8885-c12a6d01a88c)
