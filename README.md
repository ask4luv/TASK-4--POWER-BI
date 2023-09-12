### TASK-4--POWER-BI
Below are the steps to solving the Task 4
###### 1. Create a measure for the ‘Average age of depositors’
         AVERAGE AGE OF DEPOSITOR = AVERAGE('bank-full'[AGE])

###### 2.Create a new column named ‘Age band’ containing the following;
        •	‘Young’ for ages below 30
        •	‘Mid-aged’ for ages between 30 and 50
        •	‘Old’ for ages above 50

      AGE BAND = SWITCH( TRUE(),'bank-full'[AGE]<30, "YOUNG",'bank-full'[AGE]>=30 && 'bank-full'[AGE]<=50, "MID-AGE",'bank-full'[AGE]>50, "OLD")
	
###### 3. Create a measure calculating the total balance for:
        •	Job: Technician
        TOTAL BALANCE FOR TECHNICIAN = SUMX(FILTER('bank-full', 'bank-full'[JOB]= "TECHNICIAN"),'bank-full'[BALANCE])

        •	Marital: Single and Married
        TOTAL BALANCE FOR MARRIED = SUMX(FILTER('bank-full','bank-full'[MARITAL]="MARRIED"),'bank-full'[BALANCE])

         TOTAL BALACE FOR SINGLE = SUMX(FILTER('bank-full','bank-full'[MARITAL]="SINGLE"),'bank-    full'[BALANCE])

 ###### 4. Create a measure to get the number of depositors on Loan
            DEPOSITORS ON LOAN = COUNTROWS(FILTER('bank-full','bank-full'[LOAN]="YES"))
            
            
             
             
 <img width="957" alt="6" src="https://github.com/ask4luv/TASK-4--POWER-BI/assets/138107435/e96f3563-816a-4eb6-b8a0-65b5473b4243">

