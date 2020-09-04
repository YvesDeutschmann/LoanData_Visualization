# Tableau Visualization for Prosper Loan Dataset

## About the data
Prosper Marketplace is a peer-to-peer lending platform. Think of it like eBay for loans. Borrower request personal loans on the platform provided by Prosper. Investors browse this catalog of loan requests and decide whether to partially fund a loan request upon credit scores, ratings and other key figures that are provided by Prosper Marketplace.

## Dataset
The Prosper loan dataset was provided by Udacity as part of their Data Set Options for the Data Analyst Nanodegee. The dataset includes 113,937 loan requests and 81 variables including loan amount, borrower rate (or interest rate), current loan status, borrower income, and many others.

You can view final version of my [Prosper Loan Data Story](https://public.tableau.com/views/LoanViz-feedbackI/Story-final?:embed=y&:display_count=yes&publish=yes) by clicking on image below:

[![visualization image](https://github.com/jubins/Tableau-Projects/blob/master/ProsperLoanData/data/pld_screenshot.png)](https://public.tableau.com/views/LoanViz-feedbackI/Story-final?:embed=y&:display_count=yes&publish=yes)

## SUMMARY
This visualization is trying to investigate the Prosper dataset regarding the use of revolving credits. I
started with an introduction page to give a brief overview of what the reader can expect from the
following pages. The first dashboard describes the general development of income, revolving credits
and possible related variables. For all these three variables we can notice one trend, that is upwards.
Though all figures are growing, it is the credit balance that is rushing in front in terms of growth
leading to a higher debt-to-income-ratio.

The second sheet is showing for what the requested loan amounts were used for and the
development of this distribution from 2007 to 2013. We can clearly see that the loans with the
purpose of debt consolidation have a massive growth in terms of loan amounts per year. In 2013,
the amount of loans for debt consolidation was higher than the total loan volume of 2012!


On the third and fourth dashboard we dive deep into the loans for debt consolidation and see if
there are any differences for income levels, the related debts for this level and wherein the USA the
most of these debts are aggregated. Sheet three is showing us that there is a clear gap in the
development of the income and the available credit balance for an income less than 50.000$ per
year. The last sheet is showing a relation between debt and available credit balance. Accounts with
an income less than 50.000$ tend to have a credit balance that is too high in relation to this income
resulting in high debt-to-income-ratios (DIR). The lower the income range, the higher the variance
for the DIR is. The map doesn’t reveal any “center of debt” or pattern. Though, you might have
noticed that there isn’t a single datapoint for North Dakota for an income of 75.000$ and above.

## DESIGN CHOICES
For the first chart, I chose a combined bar and line chart because I wanted to show a development
over time. I dismissed a line graph with 2 lines because the range of values for both lines was too
wide to display them on the same scale. So, I draw 2 scales and decided to use a clear optical
encoding in form of a trace as a bar chart and a trace as a line graph.

The second chart is showing a development over time for all three variables. So, I decided to use a
line chart. Because all variables show data for the same time, I use the same time scale for all of
them and split the y-axis for the three variables. I didn’t want to gather the lines on the y-axis in one
chart because this wouldn’t show the details I want to show for each variable as the range of values
is too wide. To further point on the development I added trend lines to all three variables.
On the next chart, I wanted to show multiple variables all in the same place. There is a time scale,
categorical data and numerical data that I wanted to show in a compact form. I chose a tree chart as
this chart allows me to display the development of the numeric values over time while also breaking
down the data down into two separate categories pairs. With the loan amount encoded with size, it
is possible to quickly compare the amounts for different categories and/or years.


The last dashboard is showing four more charts – this time only for loans with the purpose of debt
consolidation. All the charts can be filtered by income range with a drop-down menu on the upper
left corner. You can choose only one income range at a time because I clearly want to show patterns
for this category. This dashboard is all about the differences between these categories.
The first two charts on the upper right, are showing the development of data over a timeframe so I
chose a line chart. For the upper chart, I decided to split up the y-axis in two separate charts because
the range of values doesn’t fit a shared y-axis. Though, for the lower part, I combined both lines on
the same y-axis to clearly show a gap between both variables, if there is one. To further stress this
out I added trend lines for both variables.


The third chart is a scatterplot on the upper left because I want to display a relation of two variables.
I decided to use a transparency level to deal with overplotting in certain areas of the chart.
The last chart on the bottom is a map that is encoded by color. Encoding with size didn’t work out
because the range of values was too narrow to quickly recognize differences between the states.
Encoding over color achieves exactly this.
