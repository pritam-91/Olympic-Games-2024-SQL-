# Olympic-Games-2024-SQL-
Using MySQL DBMS find some reports from Olympic Games 2024 data set.

*1)Names of all of the country get 1st position in this Olympics 2024.*


SELECT NOC, Ranks

FROM Olympic. olympics2024

WHERE Ranks = 1

GROUP BY NOC

ORDER BY Ranks ASC;

![Screenshot 2024-08-17 184133](https://github.com/user-attachments/assets/e3404b69-c0db-4b70-8968-1ddcc2e6f999)


*2)Top 10 Country’s name and their total number of medals*


SELECT NOC, MAX(Total) AS TOTAL FROM

Olympic. olympics2024

GROUP BY NOC

ORDER BY TOTAL DESC;

![2P](https://github.com/user-attachments/assets/dabdae11-90cf-4b66-ad23-bbd8c860aabc)


*3)Rank wise total numbers of medals collected by each country*


SELECT Ranks, NOC, SUM(Total) AS Total_madels

FROM Olympic. olympics2024

GROUP BY Ranks, NOC

ORDER BY Ranks, Total_madels DESC;


*4)Total number of countries for each competition*


SELECT Competitions, COUNT(NOC) AS Total_Country_Apper

FROM olympic. olympics2024

GROUP BY Competitions

ORDER BY Total_Country_Apper DESC;

![4P](https://github.com/user-attachments/assets/5fae58cc-6ac5-415d-a6ff-ebb93336c31b)


*5)Medals distributions by each country*


SELECT NOC, SUM(Gold) AS GOLD,

SUM(Silver) AS SILVER,

SUM(Bronze) AS BRONZE,

SUM(Total) AS TOTAL

FROM Olympic. olympics2024

GROUP BY NOC

ORDER BY TOTAL DESC;

![5P](https://github.com/user-attachments/assets/a0ec6684-f349-4fbf-9239-d26880a3bc92)



