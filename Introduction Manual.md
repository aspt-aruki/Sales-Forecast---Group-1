![](https://i.imgur.com/mHymGgz.png)
***<center>User Instruction Manual</center>***
*<center>Last Updated April 2020</center>*

[TOC]
******

# **Introduction**

This instruction manual aims to provide a step-by-step guide on the usage of the various data files as well as the process on how to forecast ASPT-Aruki sales in the future using the application.

The following are the deliverables that are presented to you in a folder called **Aruki**:

1. R-Scripts
2. R-Shiny Application
3. Dashboard
4. Instruction Manual

# **Aruki Folder**
In the Aruki Folder that is given to you, it should contain the following docs:
- app.R
- Create_shortcut.R
- `Dashboard` folder
- Dashboard.pbix
- `Data` folder **(Save your 4 data files here)**
- `Prog Files` folder **(Please do not touch this)**
- `www` folder **(Please do not touch this)**
    >![](https://i.imgur.com/tCU1YUN.jpg)


# Setting Up For the First Time
## Downloading the Software
### CRAN R

1. Open an internet browser and go to https://cran.rstudio.com
3. Click on the `Download R for Windows` link.
    > ![](https://i.imgur.com/tyQ9tg0.png)
4. Click on the `install R for the first time` link at the top of the page.
    >![](https://i.imgur.com/S4mWBk6.png)
5. Click `Download R for Windows` and save the executable file somewhere on your computer. Run the .exe file and follow the installation  instructions.
    >![](https://i.imgur.com/ju3Q2CI.jpg)


### RStudio

1. Go to https://rstudio.com/products/rstudio/download/#download.
2. Click on **DOWNLOAD RSTUDIO FOR DESKTOP**.
    >![](https://i.imgur.com/dvg2Lio.jpg)
3. Save the executable file somewhere on your computer. Run the .exe file and follow the installation  instructions.




### PowerBI Dashboard

### Downloading PowerBI Software

1. Go to https://powerbi.microsoft.com/en-us/desktop/
2. Click `Download Free`
    >![](https://i.imgur.com/y7phOvd.png)
3. Click `Open Microsoft Store`
    >![](https://i.imgur.com/euBFhWN.png)
4. Press `Get` to install PowerBI Desktop
    >![](https://i.imgur.com/0e0I9hq.png)

 
## Using the Software for the first time
### Creating App Shortcut
::: info
**Note:** This shortcut is only applicable to **Windows** or **Unix** 
:::
1. In the **Aruki** Folder, open the file called `Create.shortcut.R` in RStudio.
    >![](https://i.imgur.com/ZPHbsjB.jpg)

2. Run the `Create.shortcut.R` in Rstudio

   a. Press **CTRL + A** to highlight all the code in the R script
   b. Then press **CTRL + Enter** to run the codes
    > 
    >![](https://i.imgur.com/Dy3tT1R.png)

3. After running the script , the console at the bottom will show the the following output : 
    - ***Writing .shiny_run/shinyShortcut.cmd***
    - ***Writing shinyShortcut.vbs***
    
    >![](https://i.imgur.com/mP3hRMG.png)


4. In the `Aruki`folder, a new folder called `.shiny_run` will be created
    >![](https://i.imgur.com/epuajHo.jpg)

5. The folder contain the command prompt shortcut called **shinyShortcut.cmd** which you can save it anywhere(e.g. Desktop) 
    >![](https://i.imgur.com/x1IWbYd.jpg)

6. In the future, you would just need to click on `shinyShortcut.cmd` to open the app. 
    ::: info
    **Alternative**: If `shinyShortcut.cmd` does not work for you, Open `App.R` in Aruki folder and Press **Run App** on the right hand side of the screen to open the app.
        
    ![](https://i.imgur.com/eEmCNwC.png)
    :::
    

 
### PowerBI Dashboard
#### Changing Directory Path for PowerBI

1. Open `Dashboard.pbix` that is saved in the Aruki folder
    >![](https://i.imgur.com/1nPKdHl.jpg)

2. Go to **Home > Queries > Transform Data > Data Source Settings**
    >![](https://i.imgur.com/nG3nnpU.png)

3. Click on the filepath that contain `final_powerbi_dashboard.csv`
    > ![](https://i.imgur.com/k7OlmfI.png)

4. Click on **Change Source**
    >![](https://i.imgur.com/xjrve60.png)

5. Click on **Browse** to change the file directory
    > ![](https://i.imgur.com/WxcFkai.png)

6.  In the Aruki folder, there is a subfolder called `Dashboard` which contains all the datafiles needed for the dashboard. Choose `final_powerbi_dashboard` and press open.
    > ![](https://i.imgur.com/7p3u2jh.png)

7. Click **OK**
    > ![](https://i.imgur.com/GpSXiD5.png)

8. Repeat steps 3 to 7 for the remaining csv files -
    >* `Final_PowerBIdashboard_Code.csv`
    >* `Final_PowerBIdashboard_Item_No.csv`
    >* `Final_PowerBIdashboard_Main_Category.csv`
    >* `Final_PowerBIdashboard_Purchase.csv`

9. After that, Click **Close** once you finishing changing the source
    > ![](https://i.imgur.com/lyPaRmV.png)

10. A ribbon error will appear. Click **Apply Changes** to update the data.
    >![](https://i.imgur.com/zwaOyh8.png)

11. An Apply Query Changes screen will appear. Once it finishing loading. The screen will automatically closed.
    > ![](https://i.imgur.com/7Orygj6.png)
12. Please **Save** the the changes by click the save icon on the left side of the screen.
	>![](https://i.imgur.com/pGmfT9V.png)

 




---


# For Subsequent Use

## Loading New Data

### SAP Business One

1. Extract a minimum 5 years of information for the following data from SAP Business One

   1. **Item Listing data**

      1. Save file as: `Item_listing.xlsx`
      2. Column Names of Item Listing :
    
         > - Code
         > - Item No.
         > - Item Description
         > - Name
         > - Main Category

   2. **AR Invoice data**

      1. File Name as: `AR_Invoice.xlsx`
      2. Column Names of AR Invoice:

         > - Document Number
         > - Posting Date
         > - Employee No
         > - First Name
         > - Last Name
         > - Customer/Vendor Code
         > - Item No.
         > - Item/Service Description
         > - Quantity
         > - Price Currency
         > - Price after Discount
         > - Currency Rate
         > - Row Total
         > - Row Total (FC)
         > - Total Discount
         > - Total Discount (FC)
         > - Remarks

   3. **Sales Order data**

      1. File Name as: `Sales_order.xlsx`
      2. Column Names of Sales Order:

         > - Document Number
         > - Posting Date
         > - Employee No
         > - Customer/Vendor Code
         > - Item No.
         > - Item/Service Description
         > - Quantity

   4. **AP Invoice data**

      1. File Name as: `AP_invoice.xlsx`
      2. Column Names of AP Invoice :

         > - Document Number
         > - Posting Date
         > - Employee No
         > - First Name
         > - Last Name
         > - Customer/Vendor Code
         > - Item No.
         > - Item/Service Description
         > - Quantity
         > - Price Currency
         > - Price after Discount
         > - Currency Rate
         > - Row Total

2. Ensure that these Excel Files are saved in the **Data folder** in **Aruki** folder. 


## R Shiny Application

### Update and Run the App

1. Ensure that steps in [**Loading New Data Section**](#Loading-New-Data) have been done before running the app
    :::info
    **Note**: In the future, please repeat [**Loading     New Data Section**](#Loading-New-Data) when you         have new data. 
    ::: 


2. Run the forecast application using one the following methods:

    (A). Double Click  on `shinyShortcut.cmd` Or 
    
    The command prompt would pop up when the shortcut is being executed  and you just need to wait for it load.
    > ![](https://i.imgur.com/RCOF6Ru.jpg)
    
    (B) Open `App.R` in Aruki folder and **Press Run App** on the right hand side of the screen
    >![](https://i.imgur.com/vdFaaWB.png)

    

3. After running the app, a pop up screen will appear 
    >![](https://i.imgur.com/24q2HAZ.jpg)

    :::info
    **Note:** If the command prompt fails (step 2A),         check the `Missing Product Category.csv` in `Aruki`     Folder. 
         ![](https://i.imgur.com/o6dXTog.jpg)

    > 
    Please fill in the missing values **NA** and update     the `Item_listing.xlsx`. 
     ![](https://i.imgur.com/WyWJtj0.jpg)
    :::


### Functions of the App

When the App starts, there will be an **introduction tour**. You may navigate the tour using the `next` and `previous` buttons. 
>![](https://i.imgur.com/uiR22qb.png)

> You can also skip the tour by clicking `skip` or anywhere outside the introduction boxes.
>![](https://i.imgur.com/sU3dHYt.png)


#### Sales Forecast Tab

In the Sales Forecast tab, you are able to  perform the following functions:
> ![](https://i.imgur.com/QX7T20U.png)
> 1. Download a Forecast Input template 
> 2. Click  [**Model Tab**](#Model-Tab) to see model performance
> 3. Click  [**Variable Tab**](#Variable-Tab) to see suggested input value for variables
> 4. Upload your forecast inputs and click submit
> 5. Select your preferable model to forecast the sale quantity 
> 6. View Predicted Sales Quantity and Download result in any of the following format (csv or xlsx)


#### Variable Tab
In the Variable tab, you are able to  perform the following functions:
> 1. Browse the 5 plots (Per Main category, Code, Country) that shows historical data of the variables used for prediction
> 2. Use the plots to make an estimated value for your inputs in Forecast Input template.
> ![](https://i.imgur.com/8bLmkBd.png)

#### Model Tab
In the Model tab, you are able to  perform the following functions:
> ![](https://i.imgur.com/A5nr0VZ.png)
> 1. Check the model performance of 7 models trained based on historical data given.
> 2. Learn more about the models that are being used.

In general, the model with the **lowest RMSE** has the **least errors** and would be the **best model** to use for prediction.

### How to Use the App

1. Download the `forecast_input_template.xlsx` template In the **Sales Forecast** tab if you have  not done so. 
    > ![](https://i.imgur.com/id741g5.png)


2. Open the `forecast_input_template.xlsx` file to input details that you wish to predict. For example, to predict :

   > (1) **June 2020** sales quantity for 
   >
   > (2) Product Code **R04** whose
   >
   > (3)Main Category is **REFRIGERATOR** and
   >
   > (4) Country is **BN**
   >
   >   fill up excel as shown below,![](https://i.imgur.com/BKN5rq7.png)

3. To input the other values in the `sales_forecast_input.xlxs`, click the **See Variables** Button on the left to navigate to the **Variable Tab**. 
    > ![](https://i.imgur.com/1LL6YGC.png)

4. Use the filters to enter `Main Category` ,`Code `and `Country`. 
The plots will update according to the filters selected.
For the example above, to find what to input for monthly_qty_lag,  
    >![](https://i.imgur.com/tv51cfU.png)
 ::: info
 The filters must be entered according to this particular order: `Category` ,`Code` ,`Country`.
 Otherwise, the filters will reset, i.e If you filter `Code`, then `Category`, `Code` will reset.
 :::
 5. Hover above the chart to find the value for previous year monthly quantity (eg. to predict June 2020, you would find **June 2019**)
    >![](https://i.imgur.com/lZRwFkU.png)

6. You can input the actual values or any values within the 95% confidence interval (between ymin and ymax) in `forecast_input_template.xlsx`.
    >![](https://i.imgur.com/BvWZ4i4.png)

 7. Repeat **step 5 & 6** for the remaining four variables by navigating to `Average Production Days` ,`Average Transaction Day`,`Number of Invoice`,`Monthly Growth` tabs respective. Below is example's input:
   >![](https://i.imgur.com/MWfSDeA.png)

8. After filling up `forecast_input_template.xlsx`, click on the  **Back to Forecast** button to upload the file.
   >![](https://i.imgur.com/W7mW2X6.png)

9. In the  Sales Forecast Tab, upload the filled up excel file on the right, under `Upload Forecast Inputs`.
    >![](https://i.imgur.com/gtHdMvE.png)
    >
    >
    >![](https://i.imgur.com/4V6TKEg.png)


10. Once the upload is complete, click the **submit** button to generate the predicted sales quantity.

    >![](https://i.imgur.com/c3P8A5j.png)
 
     ::: info
    If the app **gray out** , 
        ![](https://i.imgur.com/Oo3OHGl.png)
    1. Please check your `forecast_input.xlsx` files that was uploaded to ensure that there are no typo errors.
    **Note**: Our models can only predict Sales quanitity that have past transaction.
    
    2. To reupload the new input,**refresh** your browser.
    :::
11. To decide which model to use, click on the **See Model Performance** button. 

    > ![](https://i.imgur.com/8ORuXhM.png)

12. In the model tab, seven models' performance based on the historical data are shown. It is advisable to choose the model with the **lowest RMSE**.
    > Toggle the arrows in the **RMSE** column to get the lowest/highest at the top of the table
    > ![](https://i.imgur.com/uDy76h9.png)
   

13. After that,  click **Back to Forecast** button and  select your preferable model to use.

    >![](https://i.imgur.com/5YESTDp.png)


14. The results will be shown in a table where you choose to download in either of the following format: CSV or Excel. 
    * You also have an option to download the predictions from all models through the **All model predictions** button.
        >![](https://i.imgur.com/nh4CD9B.png)

---

## PowerBI Dashboard - Sales Analysis

### Updating the data

1. Run the steps in [**Loading New Data Section**](#Loading-New-Data) before opening the PowerBI dashboard
2.  After that, run the app once using the `shinyshortcut.cmd` or `app.r` so that new data is being generated for the dashboard. 

2. You will see that the data has already been loaded as `Final_PowerBI_dashboard` in **Fields** on the right
 	>![](https://i.imgur.com/aB7XpaW.png)

3. Click **Home Tab → Under Queries** section, Click **Refresh** to update the data!
 	>[](https://i.imgur.com/Z2jSh4d.png)
    :::info
    If there is the following error , Perform the steps     in [**Changing Directory Path for PowerBI**](#Changing-Directory-Path-for-PowerBI)
     > ![](https://i.imgur.com/59n6LFA.jpg)
    :::




### Navigating around the Sales Dashboard

1. To clear all filters in each of the boards, press **CTRL + Click** on the `Clear all filters` button.
	>![](https://i.imgur.com/d0Rj1EY.png)

2. On the right hand side of the each board, it contains  filters such as `Date`, `Main Category`, `Product Code` , `Item No.` and `Country`. This is where you can click to select or search desired inputs from drop down filter.
 
	>![](https://i.imgur.com/ILaUOCa.png)

3. To navigate between the pages, just click the tabs at the bottom.
	>![](https://i.imgur.com/nqZgrUE.png)

#### A. Main Board
The Main section contains key figures and is intended to provide an overview of sales at ASPT-Aruki.

1. The top of the dashboard contains some key figures at glance.
	>![](https://i.imgur.com/PPvf91g.png)
	>
	> **Interpretation of KPI** :
	>
	>| **KPI** | **Rationale** | 
	>| -------- | -------- | 
	>| Year to Date Current Year's Sales| Shows how much sales have been made in the current year | 
	>| Past Year Sales| Shows how much sales have been in the past year | 
	>| Current Year Sales as % of Past Year Sales| Shows progress made in sales compared to past year sales| 

2. The top left visual of the dashboard contains the Actual Sales throughout the years. Hover over the line chart to see the actual sales amount.
	> ![](https://i.imgur.com/P5BiivX.png)

3.  The right side of the dashboard contains `Sales By country`
	> Hover over to see: 
	>  (1) Country
	>  (2) Total Sales
	>  (3) Current year sales as % of Past Year
	>  
	> ![](https://i.imgur.com/nTMB6Uy.png)


4.  At the bottom of the dashboard it contain Product Codes Ranked By Sales 
	> Hover over to see:
	>  (1) total sales,
	>  (2) total quantity sold, and 
	>  (3)the main category it belongs to.
	> 
	> ![](https://i.imgur.com/YLeR35V.png)

5. All visuals in the dashboard also act as **cross filters** for the remaining visuals by **clicking/ctrl-clicking on other graphs**
	> Eg. Selecting a country in the Sales by Country graph will filter the rest of graphs to show sales by that particular country
	> 
	> ![](https://i.imgur.com/sW3HMte.png)
:::info 
**Note**  : To clear filter , **CTRL + Click** on the `Clear all filters` Button
:::

#### B. TOP 10 Analysis
In this page, it will show all the Top 10 products and Bottom 10 products by 
* 	Main Categories
* 	Product Codes
* 	Item Numbers

![](https://i.imgur.com/GT854jU.png)

1. The left-most section contains the top 10 Main Categories by Sales
	>![](https://i.imgur.com/YCkdiNg.png)
	>
* **Hover** over the graph to show tooltip
	>
	> ![](https://i.imgur.com/fONPhIb.png)
	> * The tooltip will show dollar amount of sales (Darker blue) compared to dollar amount of purchases (Lighter Blue) in the last 5 years
	> * It will also provides a short explanation as to how to interpret this graph

2.  The middle of the dashboard contains bar charts of the top 10 and bottom 10 Product Codes based on Sales.
	>![](https://i.imgur.com/HMKEeKO.png)
	>
	> Similarly , hover over the graph to see tooltip
3. Lastly on the right-hand side of dashboard, Top 10 and Bottom 10 Item No based on Sales will be shown
	>![](https://i.imgur.com/kqu6rgl.png)
	>
	> Similarly, hover over the graphs to see tooltip
:::info 
**Note**  : To clear filter , **CTRL + Click** on the `Clear all filters` Button
:::


#### C. Internal KPI
This dashboard page measures each employee's performance in Aruki. By selecting for each employee in the `Sales Ranked by Employee` visual, one will be able to cross-filter other visuals to see the proportion of walk-in vs. direct orders, as well as top 10 countries for each employee.
![](https://i.imgur.com/B6gz1a1.png)

1. on the top right hand side of the dashboard, it contain the Employee Ranking by sales.
	>![](https://i.imgur.com/V6j2zm8.png)
	>
2. **Hover** over the graph to see employee's performance through the years
	> ![](https://i.imgur.com/soWsnaQ.png)

3. Selecting an employee (**Clicking on a bar**) in `Sales Ranked By Employee` Chart, it will show :
 	> (1) Details for top 10 countries they are in charge of
 	> (2) Walk-in sales to direct order ratio
 	> (3) Transaction details
 	> 
    > ![](https://i.imgur.com/WTjYGij.png)
:::info 
**Note** : To clear filter , **CTRL + Click** on the `Clear all filters` Button
:::
 

#### D. Country Analysis
This page shows customer and product analysis for each country. It is able to identify the top 30 customers for each country as well as their top-selling items.

1. On the left side of the dashboard, it contain the sales ranked by country.
	>![](https://i.imgur.com/esoPNPp.png)
	>
	> * The bigger the size of the data point, the higher the volume of sale

2. **Hover** over to show trends in the previous years
	>![](https://i.imgur.com/A06Xt4B.png)

3. Click on a datapoint in `Sales Ranked by country` to filter for 
		(1) Top customers per country
		(2) Top item numbers per country
	>	
	> ![](https://i.imgur.com/D5l4EqK.png)
	
4. The top-right corner of the dashboard contains a Treemap - `Sales Ranked by Top 30 Customers` 
	> ![](https://i.imgur.com/mKLBtxN.png)
	>  Largest square tile shows customer with most sales 
5. **Hover** over the treemap to see sales for the last few years for a particular customer
	>![](https://i.imgur.com/ExlzO0n.png)
 
:::info 
**Note**  : To clear filter , **CTRL + Click** on the `Clear all filters` Button
:::

### Possible PowerBI Dashboard Errors

1. Accidental misalignment of graphs while using the dashboard
* **Ctrl + Click** on the `Clear all filters` button on the top right corner of each dashboard and everything will return to its original state



​    