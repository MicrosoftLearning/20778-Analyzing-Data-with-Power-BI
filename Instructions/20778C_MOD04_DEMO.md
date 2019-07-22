# Module 4: Shaping and Combining Data

- [Module 4: Shaping and Combining Data](#module-4-shaping-and-combining-data)
  - [Lesson 1: Power BI Desktop Queries](#lesson-1-power-bi-desktop-queries)
    - [Demo 1: Using APPLIED STEPS](#demo-1-using-applied-steps)
  - [Lesson 2: Shaping Data](#lesson-2-shaping-data)
    - [Demo 1: Transforming Data with the Power Query Editor](#demo-1-transforming-data-with-the-power-query-editor)
  - [Lesson 3: Combining Data](#lesson-3-combining-data)
    - [Demo 1: Adding and Shaping Data from the Internet](#demo-1-adding-and-shaping-data-from-the-internet)


## Lesson 1: Power BI Desktop Queries

### Demo 1: Using APPLIED STEPS

1. If it is not already running, start the **MT17B-WS2016-NAT**, **20778C-MIA-DC** and **20778C-MIA-SQL** virtual machines, log on to **20778C-MIA-SQL** as **ADVENTUREWORKS\\Student** with the password **Pa55w.rd**.

2. On the taskbar, click **Power BI Desktop**.

3. In the **Welcome to Power BI Desktop** window, click **Already have a Power BI account? Sign in**.

4. In the **Sign in** dialog box, enter your account credentials, and then click **Sign in**.

5. In the **Sign in to your account** dialog box, enter your password credentials, and then click **Sign in**.

6. In the **Power BI Desktop** window, click **Get data**.

7. In the **Get Data** dialog box, click **Azure SQL database**, and then click **Connect**.

8. In the **SQL Server database** window, in the **Server** box, type the URL of the Azure server **\<*Server Name*\>.database.windows.net** (where **\<*Server Name*\>** is the name of the server you created).

9. In the **Database (optional)** box, type **AdventureWorksLT**, and then click **OK**.

10. If the **SQL Server database** dialog box appears, click **Database**. In the **Username** box, type **Student**, in the **Password** box, type **Pa55w.rd**, and then click **Connect**.

11. In the **Navigator** window, select the **SalesLT.SalesOrderDetail** check box, and then click **Edit**.

12. On the Ribbon, in the **Query** group, click **Advanced Editor**. The window opens to display the query code. Note that no transformations have been applied yet. Click **Cancel**.

13. Right-click the **SalesOrderDetailID** column, and then click **Remove**.

14. In the **APPLIED STEPS** list, right-click **Removed Columns**, click **Rename**, type **Removed SalesOrderDetailID**, and then press Enter.

15. In the center pane, right-click the **OrderQty** column, click **Rename**, type **OrderQuantity**, and then press Enter.

16. In the **APPLIED STEPS** list, right-click **Renamed Columns**, click **Rename**, type **Renamed OrderQty**, and then press Enter.

17. In the center pane, click the **rowguid** column, and with the Ctrl key held down, click **ModifiedDate**.

18. Right-click either of the column headings, and then click **Remove Columns**.

19. In the **APPLIED STEPS** list, right-click **Removed Columns**, click **Rename**, type **Removed rowguid and ModifiedDate**, and then press Enter.

20. On the Ribbon, in the **Query** group, click **Advanced Editor**. The window opens to display the query code. Note that the transformations have been added, and they are in the same order as the list of **APPLIED STEPS**, and then click **Cancel**.

21. In the **APPLIED STEPS** list, right-click **Removed rowguid and ModifiedDate**, and then click **Move Up**.

22. In the **APPLIED STEPS** list, next to **Removed SalesOrderDetailID**, click the **delete** icon.

23. In the **Delete Step** dialog box, click **Delete**. The **SalesOrderDetailID** column reappears in the table.

24. In the **APPLIED STEPS** list, next to **Navigation**, click the **gear** icon.

25. In the **Navigation** window, click **SalesLT.SalesOrderHeader**, and then click **OK**. Note that the data preview has been updated with the **SalesLT.SalesOrderHeader** data. Also note the warning icon under **Queries [1]**.

26. In the **APPLIED STEPS** list, next to **Removed rowguid and ModifiedDate**, click the **delete** icon.

27. In the **Delete Step** dialog box, click **Delete**.

28. In the **APPLIED STEPS** list, next to **Renamed OrderQty**, click the **delete** icon.

29. Note that the warning is no longer displayed.

30. On the Ribbon, in the **Query** group, click **Advanced Editor**. The window opens to display the query code. Note that the transformations have been removed, and the source table has been changed, and then click **Cancel**.

31. On the Ribbon, click **Close & Apply** to return to Power BI Desktop.

32. Leave Power BI Desktop open for the next demonstration.

---

## Lesson 2: Shaping Data

### Demo 1: Transforming Data with the Power Query Editor

1. In Power BI Desktop, click **Get Data**.

2. In the **Get Data** dialog box, click **Excel**, and then click **Connect**.

3. In the **Open** dialog box, browse to the **D:\\Demofiles\\Mod04\\Demo** folder, click **Sales Matrix.xlsx**, and then click **Open**.

4. In the **Navigator** dialog box, select the **Sales** check box, and then click **Edit**.

5. In the **Untitled - Power Query Editor** dialog box, in the **Queries** pane, click **Sales**.

6. In the **APPLIED STEPS** list, next to **Changed Type**, click the **delete** icon.

7. In the **APPLIED STEPS** list, next to **Promoted Headers**, click the **delete** icon.

8. On the **Transform** tab, click **Transpose**.

9. Note that the columns are now rows.

10. In the top left-hand corner of the table, click the **table** icon, and then click **Use First Row as Headers**.

11. Right-click the **Column1** column, click **Rename**, type **Country**, and then press Enter.

12. Right-click the **Column2** column, click **Rename**, type **Category**, and then press Enter.

13. Click the **Country** column, and on the Ribbon, in the **Any Column** group, click **Fill**, and then click **Down**. The null values are replaced.

14. Click the **2005** column, hold down the Ctrl key and click the **2006**, **2007**, and **2008** columns.

15. Right-click any of the selected column headers, and then click **Unpivot Columns**.

16. Note that the names of the columns are **Attribute** and **Value** for the attribute-value pairing.

17. Right-click the **Attribute** column, click **Rename**, type **Year**, and then press Enter.

18. Right-click the **Value** column, click **Rename**, type **Sales**, and then press Enter.

19. On the **File** menu, click **Close & Apply**.

20. In the **FIELDS** pane, expand **Sales**, and then click **Country** to select the field.

21. On the **Modeling** tab, click **Data Category: Uncategorized**, and then click **Country/Region**.

22. In the **FIELDS** pane, note the map icon next to **Country**.

23. In the **FIELDS** pane, under **Sales**, click **Sales** to select the field.

24. In the **Formatting** group, click **Data type: Decimal Number**, and click **Fixed decimal number**.

25. In the **Data type change** dialog box, click **Yes**.

26. Click **Format: General**, point to **Currency**, and then click **$ English (United States)**.

27. In the **FIELDS** pane, note the sum symbol next to **Sales**.

28. Drag the **Country** field onto the report. Note that Power BI automatically chooses the map chart.

29. Drag the **Sales** field onto the map, and note that the bubble sizes now represent the Sales figure.

30. Click the report canvas.

31. In the **VISUALIZATIONS** pane, click **Clustered column chart**.

32. Drag **Category** onto the **Axis** property.

33. Drag **Year** onto the **Axis** property.

34. Drag **Country** onto the **Legend** property.

35. Drag **Sales** onto the **Value** property.

36. Grab the corner edge of the chart to expand the width and height.

37. Click the **Click to turn on Drill Down** arrow icon in the top right-hand corner of the chart.

38. Click the tallest column in the **Bikes** group. This now breaks down the sales by year.

39. Save the file report as **AdventureWorks Sales 4.pbix** to **D:\\Demofiles\\Mod04\\Demo**, as this will be used for the next demonstration.

40. Leave Power BI Desktop open for the next demonstration.

---

## Lesson 3: Combining Data

### Demo 1: Adding and Shaping Data from the Internet

1. In Power BI Desktop, on the **Home** tab, click the **Get Data** arrow, and then click **Web**.

2. In the **From Web** dialog box, in the **URL** box, type **https://www.imdb.com/chart/top**, and then click **OK**.

3. In the **Navigator** window, select the **Table 0** check box, and then click **Edit**.

4. In Power Query Editor, right-click the left-most column, and click **Remove**.

5. Right-click the right-most column, and click **Remove**.

6. Right-click the **Your Rating** column, and click **Remove**.

7. Note that these steps have been grouped together in the **APPLIED STEPS** list as **Removed Columns**.

8. Click the **Rank & Title** column, and then on the **Home** tab, in the **Transform** group, click **Split Column**, and then click **By Delimiter**.

9.  In the **Split Column by Delimiter** dialog box, in the **Select or enter delimiter** list, click **--Custom--**, and in the box, type a period followed by a space **". "**.

10. In the **Split at** section, click **Left-most delimiter**, and then click **OK**.

11. The Rank data now shows in its own column. Right-click the **Rank & Title.1** column, click **Rename**, type **Rank**, and then press Enter.

12. Click the **Rank & Title.2** column, and on the **Transform** tab, in the **Any Column** group, click **Replace Values**.

13. In the **Replace Values** dialog box, in the **Value to Find** box, type a space followeb by an opening parenthesis **" ("**, and then click **OK**.

14. With focus on the **Rank & Title.2** column, from the **Any Column** group, click **Replace Values**.

15. In the **Replace Values** dialog box, in the **Value to Find** box, type a closing parenthesis **")"**, and then click **OK**.

16. With focus on the **Rank & Title.2** column, in the **Text Column** group, click **Split Column**, and then click **By Number of Characters**.

17. In the **Split Column by Number of Characters** dialog box, in the **Number of characters** box, type **4**.

18. In the **Split** section, click **Once, as far right as possible**, and then click **OK**.

19. The Year data has been moved to a separate column.

20. Right-click the **Rank & Title.2.1** column, click **Rename**, type **Title**, and then press Enter.

21. In the **Text Column** group, click **Format**, and then click **Trim**. The white space around the titles is removed.

22. Right-click the **Rank & Title.2.2** column, click **Rename**, type **Year**, and then press Enter.

23. In the **QUERY SETTINGS** pane, under **Properties**, in the **Name** box, type **IMDB Top 250 Movies**, and then press Enter.

24. On the **File** menu, click **Close & Apply**.

25. In Power BI Desktop, on the **File** menu, click **Exit**.

26. If the **Microsoft Power BI Desktop** dialog box appears, click **Save**.
