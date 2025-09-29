# plsql-window-functions-Tresor-Ngabo
**Name**:Ngabo Tresor
**ID**:27209
**Group C**

**PL/SQL ASSIGNMENT**

**Step 1:PROBLEM IDENTIFICATION**

Business Identification:In the project I have a community library called Urumuri Library operating from all different places in need of centralised management within its decentralised physical operations.
Problems faced: Due to its scattered operations all over the country centralising the business to properly view the operations all out the branches is a big challenge, knowing the consumer’s preferences and viewing the consumption behaviours for all the branches
Expected Outcome: With the appropriate functions the library becomes centralised allowing the manager to manage different branches as easily as one with insight on customer’s prefered genres of books,sale’s behaviours throughout different seasons and highest demanding areas to properly supply enough book copies to the appropriate demand areas.

**Step 2:Achieved goals**

**Rank():** This function helped with 2 main goals from the problems I mentioned earlier being **Best perfoming book category overall** and also **Knowing specific individuals preferences and properly attending to their needs**
**Sum():** This function facilitated the manager in properly **centralising the sales of different branches** by adding up all the lending fees for the season to come up with the Cumumlative total
**LAG():** This function helps to predict the ups and downs of the sales by comparing the rows of lending fees to see if they have increased or decreased 
**NTILE(4):** By analysis of the fees the books generate(lending fees) the function classifies the books in quartiles based on their profitability which serves in **proper definition of demands by the consumers**
**AVG() OVER():** In each 3 months the **AVG()** Function calculates the average fees generated with inclusion of the losses and profits to get the overall picture without sudden ups and downs

**Step 3:Database Schema**

My database consists 3 tables: **Members**,**Books**,**Lendings**

**Table views:**

**Members**
<img width="736" height="463" alt="members table" src="https://github.com/user-attachments/assets/3aeea1c0-9c0c-4ece-be08-52ed470bbf78" />

This is the Members table


**Books**
<img width="833" height="451" alt="books" src="https://github.com/user-attachments/assets/a96ece55-d983-4488-8755-f07a9c80bd96" />

This is the Books table

**Lendings**
<img width="960" height="509" alt="lending" src="https://github.com/user-attachments/assets/450a8a37-3920-4027-86a3-f456a43dd932" />
This is the Lendings table

**ER diagram**
<img width="960" height="504" alt="ERD" src="https://github.com/user-attachments/assets/28c4b4c3-5cc4-4912-92c8-e94f2c76c598" />

The lendings table is in relationship with all the other tables using their attributes as its Foreign keys ie:Book id and Member id in the lendings table

**Step 4:Function Implementations**.


**RANK():** By using partition by b.category I managed to know the best selling Book genres
<img width="960" height="499" alt="rank" src="https://github.com/user-attachments/assets/e4c23358-7a35-40c2-ba6c-b0625b8f16b8" />

**SUM():** The cumulative row is a summation of all the lending fees from all the branches making it easy to centralise all the sales.

The image is of the sql queries for the function
<img width="960" height="314" alt="cumsql" src="https://github.com/user-attachments/assets/96c0ebca-4bd4-4d5a-a189-388bd2dc2bd1" />.

The result of the query is this
<img width="960" height="505" alt="cumulative" src="https://github.com/user-attachments/assets/1ee587c2-78f4-4230-a3f0-724be0d720a1" />

**LAG():** The function compares current monthly sales to previous month sales to see activity by month.It is tied to finding out the profit from the sales of 2 months.

The Queries
<img width="960" height="392" alt="lu" src="https://github.com/user-attachments/assets/50931ada-d3f6-4a2b-babc-713843f61001" />

The Results
<img width="960" height="496" alt="li" src="https://github.com/user-attachments/assets/6eb4fb22-1ad4-4964-a6dd-bef7bd3c6a13" />

**NTILE(4):** The function displays the genres of books and the revenue they raised and assigning them classes from these attributes.

The Result
<img width="960" height="483" alt="ntil" src="https://github.com/user-attachments/assets/bc0bb39d-747f-43e9-97f6-9dac8698f5a8" />


