# Bank-full 


##INTRODUCTION

This project was done with power bi which is a intelligence business tool. Bank term deposit subscription dataset was used to carry out the project.
The dataset was cleaned in excel ,which after it was imported into power bi with csv/text format.The dataset contains 45,000 rows and 18 columns.
I went further to arranging the columns to proper case. 


## PROBLEM STATEMENT

1. Create a measure for 'Average age of depositors'
2. Create a new column named 'Age band' containing the following
 
   a) 'Young' for ages below 30.
   
   b)'Mid-aged' for ages between 30 and 50.
   
   c)'Old' for ages above 50.
   
4. Create a measure calculating the total balance for
   
   a) Job technician
   
   b)Marital: single or married
6. Create a measure to get the number of depositors on loan


## ANALYZING THE DATA

Using the imported bank-full dataset to give solutions to the questions.
For the first task in finding the average age of depositors , i clicked on the new measure button on the report view of power bi and calculate it using the formula.
`Average age of depositors = AVERAGE('bank-full'[age])`
which automatically created the value for the average age of all depositors,which was viewed on the report view with card view .
![Screenshot (1)](https://github.com/Janefranceschisom/Bank-full/assets/140454293/c31a7bcf-9a9a-415e-bd62-8e9df036c7aa)

For the second task , i created a conditional column by transforming the dataset in the power query . i created a syntax that enabled me to input the conditions i want
![Screenshot (2)](https://github.com/Janefranceschisom/Bank-full/assets/140454293/48cfe26c-8eb7-489d-b320-13356d474c11)
which after i closed and applied the formula in the table .
On the table view i can view the added column
![Screenshot (5)](https://github.com/Janefranceschisom/Bank-full/assets/140454293/425674bc-1c60-4ce0-b77b-4d5ea925d81d)

For the third task ,i created a new measure in the report view in which the formula used for finding the balance for job technician was
`technician = CALCULATE(SUM('bank-full'[balance]), FILTER('bank-full','bank-full'[job]="technician"))`
while the formula for calculating single or married was
`single & married balance = CALCULATE(SUM('bank-full'[balance]),'bank-full'[marital] IN {"single","married"})`
This was viewed with a card view
![Screenshot (7)](https://github.com/Janefranceschisom/Bank-full/assets/140454293/63a50eb1-f719-45ac-b0f7-1574571454f8)
![Screenshot (6)](https://github.com/Janefranceschisom/Bank-full/assets/140454293/45f1aa6b-5bbe-47ec-bf55-b10273115efd)

For the fourth task, in getting the number of depositors on loan, i calculated the number of 'yes' in the loan column using this formula
`loan depositors = CALCULATE(COUNTA('bank-full'[loan]),FILTER('bank-full','bank-full'[loan]="yes"))`
![Screenshot (8)](https://github.com/Janefranceschisom/Bank-full/assets/140454293/e926eb3d-0bcc-4a09-ba57-27c8f2ab3882)


##CONCLUSION

The purpose of this visualization was to know the actual number of individuals representing a particular niche.
This will help the company make valuable insights from the solutions. using power bi makes data manipulation and visualization easy to use and can be 
comprehended fast in a 5secs look by anyone while viewing the result.



