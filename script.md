Before I demo the automation , I would like to give a quick insight on what actually the store procedure does  

For automation , as you all suggested we picked up one simple store procedure which is person_main_555_logic. the main intent of this store procedure is

As a first step, Increamental data is loaded into work table 1 based on some criteria

as a second step, work table 2 is created by referring incremental and historical data , filter the data with condition which is created by not equal to -555

as a next step, Update created by id column in work table 1 referring to data in work table 2 

and finally loaded into semantic tabl



This store procedure has insert , select , update and merge update.  I will take another 1 min to share the automation flow and how all these operations have been handled.

For insert query -  we parse the insert statements to identify target table, source table and create corresponding JSON transformation

For update, we parse update statement to idenify source and target table parameters , rename the source column, set the value and drop the column which is not required

for merge update - Creating TD config files with required parameters.

Let me show the demo of where to provide the input and what to be executed to get the output



