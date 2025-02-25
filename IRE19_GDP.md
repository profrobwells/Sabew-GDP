Visualizing the State & Local Economy
================

------------------------------------------------------------------------

<img src="Images-Sabew/Bea logo.jpg" width="250" height="200" /> <img src="Images-Sabew/UARK Logo vert NEW copy.jpg" width="200" height="200" />

------------------------------------------------------------------------

**Hotel Wifi: XYZ**

**Password: ABC **

**Today's Presentation**

&lt;<http://ABC> - ADD HERE&gt;
===============================

<br>

Presenter
=========

-   Rob Wells, Ph.D., University of Arkansas, Fayetteville, AR

Co-Authors
==========

-   Jeannine Aversa, Bureau of Economic Analysis, Washington, DC
-   Thomas Dail, Bureau of Economic Analysis, Washington, DC

------------------------------------------------------------------------

**This 1 hour hands-on session will show journalists how to retrieve and analyze regional GDP data and build basic maps with their findings.**

Learning Outcome: Journalists will learn to retrieve customized economic data for their own cities, counties or states and the steps to put it on a basic map and an interactive chart. We will use Google Sheets and Tableau Public.

<br>
----

Download Tableau Public
-----------------------

> <a href="https://public.tableau.com/en-us/s/" target="_blank">Tableau Download: &quot;CNTL&quot; + click for a New Tab</a>

We'll configure this in the second part of the presentation, but you can start the download now. It is a 400 mb download that will take 1.46 GB on your hard drive.

Also, you will need to create a Tableau Public account.

<br>
----

Part 1: Storytelling with Local GDP Data
----------------------------------------

This section will analyze the storytelling possibilities with the Gross Domestic Product by Metropolitan Area data.

> <a href="https://www.bea.gov/newsreleases/regional/gdp_metro/gdp_metro_newsrelease.htm" target="_blank">GDP Release: &quot;CNTL&quot; + click for a New Tab</a>

Describe the data set

> Gross domestic product (GDP) by metropolitan area is the sub-state counterpart of the Nation's gross domestic product (GDP), the Bureau's featured and most comprehensive measure of U.S. economic activity. GDP by metropolitan area is derived as the sum of the GDP originating in all the industries in the metropolitan area.

> Contributions to growth are an industry's contribution to the state's overall percent change in real GDP. The contributions are additive and can be summed to the state's overall percent change. The statistics of GDP by metropolitan area released today are consistent with statistics of GDP by state released May 11, 2017.

> GDP at chained volume measure is adjusted for the effect of inflation to give a measure of ‘real GDP’.

![](Images-Sabew/Interactive%20Data%20Tables.jpg)

Data limitations

> This data series lags significantly. We are working with 2016 data, the most recent available, which was released September 20, 2017.

> But it is still the best you can get and you can't beat the price.

<br> <br>
---

### Step 1: Retrieve the Data

![](Images-Sabew/BEA19-GDP1.png)

> <a href="https://www.bea.gov/system/files/2018-09/gdp_metro0918.xlsx" target="_blank">Click here to download the Excel tables: &quot;CNTL&quot; + click for a New Tab</a>

-   Let's see what we have.
    -   Three tables of data.
    -   382 metropolitan areas.
    -   13 industrial sectors.

Walk through the tables:

**Table 1:** Basic GDP growth by metro, 2012-2017, and its rank nationally.
NYC is \#1, Sebring, Fla. is \#383. Houston is \#7, Fayetteville, AR is \#93.

**Table 2:** Inflation adjusted GDP, chained to 2009.
This is cool because it has the percentage change growth, 2015/2016, and ranks it. So Odessa, Texas makes the top of the list with 12.1 percent growth, a rate **nearly double that of China in 2017**. Don't believe me? Look it up: <https://data.worldbank.org/country/china>

Houston's growth was flat. Ranked \#314 And Fayetteville makes \#57 on the list, with 3.4% growth.

<br>
----

> **Question: What is the benchmark metric?**

<!--Answer: US Metro areas is 2.1% growth. Is your region above or below that benchmark?-->
<br>
----

We will do the map exercise with Table 2 in a bit. But we have to look at Table 3.

**Table 3:** This is where we get the industry data.
Contributions to Percent Change in Real Gross Domestic Product (GDP) by Metropolitan Area, 2017)

Note the first column is the percentage change growth we saw in the Table 2. So that's a handy reference.

Data limitations - weirdness

> You may see a notation (D) in some cells. The footnote says: "(D) Not shown to avoid disclosure of confidential information, but the estimates for this item are included in the totals." What that means is this particularly industry is pretty small or has just a few dominant actors, so disclosure of the information would reveal confidential business information. Which is no fun whatsoever.

Data Cleaning

> The Google sheet you have has been cleaned and modified so it will play well with Tableau. Basically, the BEA spreadsheet was cleaned to remove merged cells, a data dictionary was created to keep track of our changes and new headers were created. Here is a 10-minute video on how to do this yourself:

> <a href="https://www.youtube.com/watch?v=5bS-GKvFzBk" target="_blank">Video on Excel Data Cleaning: &quot;CNTL&quot; + click for a New Tab</a>

And here is the end result in a Google Sheet. Add this sheet to your Google Drive or download it as a spreadsheet on your computer.

> <a href="https://docs.google.com/spreadsheets/d/1FBV9eQ18zNHk56pQxcDs-Jz8P3wywhcFeUo6UD-rtqs/edit?usp=sharing" target="_blank">Cleaned Data: &quot;CNTL&quot; + click for a New Tab</a>

<br> <br> <br>
---

### Step 2: Basic Interactive Chart

For this part, we will use Tableau Public to produce charts and a map. Download the app if you haven't already

![](Images-Sabew/Tableau%20Public.jpeg)

> <https://public.tableau.com/en-us/s/>

You will need to create a Tableau Public account.

Launch the app.

Tableau accepts many data sources. Under "To a Server" there's an option for Google Sheets. Or if you have downloaded the cleaned spreadsheet to your computer, you can link to it via Excel.

> <a href="https://docs.google.com/spreadsheets/d/1FBV9eQ18zNHk56pQxcDs-Jz8P3wywhcFeUo6UD-rtqs/edit?usp=sharing" target="_blank">Cleaned Data: &quot;CNTL&quot; + click for a New Tab</a>

With the Google Sheets link, select Sheet 3 and drag it to the pane that says "Drag sheets here."
![](Images-Sabew/Tableau%20data.jpeg)

Clean the data with the "Data Interpreter." Click the box is right above the sheet listing.

**Now, look at the data.**

"Metro Area" and "State" should be the only things in text: Metro area is a blue "ABC." That's a dimension. The state is a blue Globe. That's a geographic field. The rest should be with a green \# sign. Those are measures. The difference is crucial in Tableau. ![](Images-Sabew/dimensions.jpeg)

We're ready. Click on "Sheet 1" in lower lefthand corner.
![](Images-Sabew/Sheet1.jpeg)

**Welcome to a Tableau Worksheet**

![](Images-Sabew/Tableau%20worksheet.jpeg)

1.  Drag the "Metro Area"" dimension to Columns
2.  Drag the "Percent Change in real GDP" measure to Rows

-   You should have an image like this:

![](Images-Sabew/tableau%20image1.jpeg)

-   This is your basic graph of GDP growth by metro area in from 2015 to 2016.
-   Let's sort it, high to low.

![](Images-Sabew/Tableau%20Arrow.jpeg)

-   To do this, hover your mouse over the Y axis and a small arrow icon will emerge. Click it and it sorts your sheet.

![](Images-Sabew/Tableau%20Image1%20Sorted.jpeg)

-   Filter to Fayetteville and Little Rock

    -   To filter, click on the down arrow on blue pill in columns, "Metro Area." Click "Show Filter." A list of all 382 metro areas appears in a box on the sheet.

-   Configure the filter by clicking a down arrow to the right of "Metro Area." Select the option "Multiple Values Dropdown."

![](Images-Sabew/Tableau%20dropdown.jpeg)

-   Deselect "All" so nothing is checked. Then search for the following and individually select:

    -   Fayetteville
    -   Fort Smith
    -   Hot Springs
    -   Jonesboro
    -   Little Rock
    -   Pine Bluff
    -   U.S. metropolitan areas

> You now have a GDP growth chart for the metro areas in Arkansas with a U.S. comparison. You can do the same with your state later on.

-   Tweak the chart.

    -   Drag "Percent Change in real GDP" to Color in the Marks Column near the worksheet. You can select a custom color palette by clicking on colors.

    -   Double Click on the heading, "Sheet 1" and type in a headline. I typed "Fayetteville leads Arkansas GDP Growth in 2016 Source: Bureau of Economic Analysis." Use the formatting tools to center.

    -   Drag "Percent Change in real GDP" to the "Label" icon in the Marks box. This is to the left of the chart. Numbers will appear above the bars on the chart.

    -   Format the numbers and legend. Look at the Marks card. Find the green pill representing the label "Sum(Percent Change in Real GDP)." Click the down arrow in this label. Click Format.

    -   Format the numbers, continued: The Format pane appears to the left. Under "Default," select "Numbers." Then select "Number - Custom." Select two decimal places and put a % sign in the suffix.

    -   Format the Y axis legend. Left click on the Y axis to see menu. Select "Format." See the formatting pane on left: select "Axis." On "Scale," select no decimals and put a % sign in the suffix.

    -   Drag the "Metro Area" Filter and then the Color legend to just below the X axis.

    -   Rename the tab "Sheet 1" to "Arkansas GDP"

-   Your chart should look like this:

> <a href="https://public.tableau.com/profile/rob.wells#!/vizhome/SabewTable1/ArkansasGDP?publish=yes" target="_blank">Tableau Chart: &quot;CNTL&quot; + click for a New Tab</a>

<br> <br> <br>
---

#### Step 3: Basic Map

We'll use the same data for a map. First, we have to convert the Dimension "Metro Area" to geographic data, or we need to "Geocode" this dimension.

-   Geocode Data
    -   Click on "Metro Area" down arrow
    -   Select "Geographic Role" and then Select "CBSA/MSA"
        -   this converts the text of Metro Area into data for mapping.

![](Images-Sabew/Geocode1.jpeg)

Notice in Measures that Latitude and Longitude measures are now created.

**Follow These Steps In This Order:**

> -   Click on "new worksheet" tab at lower right. It creates Sheet 2.
> -   Drag Longtidue to Columns, Latitude to Rows
> -   In upper right "Show Me" menu, click on the map icon. A grayed out world map appears.
> -   Drag "Metro Area" to the sheet. A U.S. map appears with blue dots.

> -   Filter "Metro Area" blue pill in the Marks formatting box next to the sheet. Click "Show Filter" and format the filter as "multiple values dropdown" as we had in the past.
> -   Deselect "All" so nothing is checked. Then select:
> -   Fayetteville
> -   Fort Smith
> -   Hot Springs
> -   Jonesboro
> -   Little Rock
> -   Pine Bluff

> -   Change "Automatic" in Marks Card. Click down arrow and select "Map." The blue metro areas will appear on the map.
> -   Drag from Measures "Percent Change in real GDP" to the worksheet.
> -   Bring up the data labels. Drag "Percent Change in real GDP" to Label box on Marks card.
> -   Add Metro area names. Drag "Metro Area" to Label on Marks card. Click the Options box to allow labels to overlap
> -   Format labels, drag search box, legend to bottom, write a headline

<br>
----

**Your finished map should look like this:**

![](Images-Sabew/Finished%20Map.jpeg)

<br>
----

-   If you are good with this tutorial, then create a chart and map for your local community. Chart the rate of industry-specific sector growth by chooings one or more of the following:
    -   Arts, entertainment, recreation, accommodation, and food services
    -   Construction
    -   Durable-goods manufacturing
    -   Educational services, health care, and social assistance
    -   Finance, insurance, real estate, rental, and leasing
    -   Government
    -   Information
    -   Professional and business services
    -   Trade
    -   Transportation and utilities

Figure out some other visualization!

Thank you.

Follow up questions:
====================

-   Rob Wells - <rswells@uark.edu> or @rwells1961

-   Jeannine Aversa - <Jeannine.Aversa@bea.gov>

-   Thomas Dail - <Thomas.Dail@bea.gov>

--

<img src="Images-Sabew/Bea logo.jpg" width="250" height="200" /> <img src="Images-Sabew/UARK Logo vert NEW copy.jpg" width="200" height="200" />

--

--30--
