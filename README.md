# Relational-Algebra

select customers.customerName, offices.city as office_city
from customers, employees, offices
where 
	customers.salesRepEmployeeNumber = employees.employeeNumber and 
	employees.officeCode = offices.officeCode and
    customers.city = offices.city;


π customers.customerName, offices.city  (customers |×| salesRepEmployeeNumber = employeeNumber ( π employeeNumber ( employees |×| officeCode = officeCode ( π officeCode (offices |×| city = city ( π city (customers)))))
