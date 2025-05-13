# data-assignment--data-analysis-solved
**TO GET THIS SOLUTION VISIT:** [Data Assignment- Data Analysis Solved](https://www.ankitcodinghub.com/product/data-assignment-data-analysis-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;91861&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Data Assignment- Data Analysis Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
The objective of this exercise is to create a pipeline that ingests, cleans and joins three different files and outputs the final dataframe to a user specified file name of format .csv or .json. No README file is required, however you should write your code in a readable manner and document with comments.

The deliverable is a python script that will be called from the terminal and take an output file path as input, examples on how the script will be called below:

Note, the output type should be automatically inferred from the file path provided. Provided files:

employers.csv: contains basic information about our current clients.

quotes.csv: contains information about quoting a new product to our existing clients. The column EmployerId will be the key to join to employers.csv.

product_premiums.txt: This text file contains information about a clients current product mix and the premiums they are paying for each product. This file is not structured in a way that is readable by pandas.

Pipeline steps

Your pipeline should follow these steps:

<h1>1. Combine Employers and Quotes data</h1>
read the employers.csv and quotes.csv and merge them on EmployerId as an inner join. Ensure that the result is unique on EmployerId. If there are duplicates, keep the row with the latest quote date.

<h1>2.&nbsp; Create a new column named ClientTenure</h1>
based on the date the employer became a client and the date ProductX was quoted, determine the client tenure (in years, assuming 365 days a year) at the time of quote. Round to nearest integer.

<h1>3.&nbsp; Create a column named SizeRange</h1>
This will be a categorical column based on the Employees column, which is a count of the number of employees a client has. The resulting values in the new column will be:

<h1>4.&nbsp; Read product_premiums.txt</h1>
This file contains the products a client currently has, and the annual premium associated with each product. The file structure is not natively readable by pandas, so you must write a parser to extract the information into a dataframe. The file is structured to have a section start with EmployerId: 00000000 followed by a series of product and premium pairs, such as Product1: 9233. Each Id only occurs once. An employer can have duplicate products (one per location) but premiums will be unique. The resulting dataframe should look like this:

<h1>5.&nbsp; Aggregate the premium data from step 4 to the EmployerId level</h1>
Create the following columns:

ProductList: a comma separated string with the distinct products a client has. ex. ‘Product4,

Product1, Product2’

NumUniqueProducts: the number of unique products a client has. In the above example it would be 3.

SumPremium: A sum of the premium from all products.

The resulting aggregated dataframe should look like this:

<h1>6.&nbsp; Join aggregated premium data to the dataset created in steps 1-3 using pandasql</h1>
Write SQL to create an inner join on EmployerId. There will be a case statement, and the columns should be selected as follows:

Note that the aliases are not valid, they just represent which dataframe to pull the columns from. To use pandasql:

<h1>7. Write final DataFrame to file output specified by user</h1>
user specified file path to be read from command line. A user can specify a .csv file or .json file, but will not provide explicit instruction besides the file extension provided.
