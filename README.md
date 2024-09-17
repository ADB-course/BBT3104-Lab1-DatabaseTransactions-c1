[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/r-tQZu0l)
# BBT3104-Lab1of6-DatabaseTransactions


| **Key**                                                               | Value                                                                                                                                                                              |
|---------------|---------------------------------------------------------|
| **Group Name**                                                               | ? |
| **Semester Duration**                                                 | 19<sup>th</sup> August - 25<sup>th</sup> November 2024                                                                                                                       |

## Flowchart

[text](../../../../AppData/Local/Packages/5319275A.WhatsAppDesktop_cv1g1gvanyjgm/TempState/C578B62099F8AC80C1F66028B53F7F07/flowChart4lab1.docx)
## Pseudocode

Start

1.Calculate Latest Order Number
2.Create New Order
3.Create Savepoint 1
4.Insert Product 1
Update Product 1 Quantity in Stock
5.Create Savepoint 2
6.Insert Product 2
Update Product 2 Quantity in Stock
7.Create Savepoint 3
8.Insert Product 3
Update Product 3 Quantity in Stock
9.Receive Payment
10.Commit Transaction
11.Confirm Effects of Committed Transaction
End

## Support for the Sales Departments' Report


To improve the database design for generating a report on unpaid orders and outstanding balances, you could implement the following changes:

1. Add a Payment Table: Create a separate table to record payments. This table should include fields such as payment_id, order_id, payment_date, amount_paid, and payment_method.

2. Modify the Orders Table: Ensure that the orders table includes a field for total_amount and possibly amount_paid or balance_remaining if you need to track the current balance directly.

3. Create a View or Query: Develop a database view or query that joins the orders table with the payments table to calculate the remaining balance for each order. This view can aggregate payments by order and compute the difference between the total_amount and the total payments made.

4. Update Reporting Tools: Adjust reporting tools or scripts to use this view or query to generate reports showing unpaid orders and their outstanding balances.

By structuring the database this way, you can efficiently track and report on payments, ensuring that the sales department has accurate information for follow-ups.
