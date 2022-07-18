# Order Brushing Detection
**Order brushing** is a fraudulent practice in which shops create an artificial increase in their number of sales in an attempt to bolster their reputation and increase their ratings on e-commerce websites. 

The goal of this coding challenge is to create a baseline rule-based program for detecting potential order brushing. 

## Task
This order brushing detection activity &mdash; which highlights the importance of data analytics in e-commerce &mdash; is the **Week 1 Contest (Student Category)** of the **2020 Shopee Code League**. 

### Dataset
The dataset, stored in a comma-separated values (CSV) file, consists of four columns:
- `orderid` - Unique ID assigned to every transaction
- `shopid` - Unique ID assigned to every seller
- `userid` - Unique ID assigned to every buyer
- `event_time` - Timestamp of every recorded transaction

Note that the dataset is under the intellectual property of the contest organizers. Therefore, it is not published in this repository. For the same reason, the output of each cell in the Jupyter Notebook is also stripped. 

### Order Brushing
Order brushing is checked for every possible one-hour window. A shop is said to have conducted order brushing if its *concentration rate* (ratio of the number of transactions to the number of unique buyers) for a particular one-hour window is at least 3.0.

In addition, for every shop found to have conducted order brushing, the shop IDs of the *suspicious buyers* (those who registered the highest number of transactions during order brushing periods) have to be identified. 

### Submission Format
The results of the data analysis have to be stored in a CSV file consisting of two columns:
- `shopid` - ID of shop suspected of order brushing
- `userid` - ID of suspicious buyer

If a shop is not found to have conducted order brushing, the entry in the second column is set to 0. For shops with more than one suspicious buyer, the user IDs are listed in ascending order and separated using an ampersand (without any space before and after it).

Since the dataset is an intellectual property of the contest organizers, the CSV file containing the results is also not published in this repository. 

## Built Using
In creating the Jupyter notebook for this coding challenge, the following Python modules and libraries were used:

Libraries/Modules | Description | License
--- | ---| ---
[`math`](https://docs.python.org/3/library/math.html) | Provides access to the mathematical functions defined by the C standard | Python Software Foundation License
[`csv`](https://docs.python.org/3/library/csv.html) | Implements classes to read and write tabular data in CSV format | Python Software Foundation License
[`collections`](https://docs.python.org/3/library/collections.html) | Implements specialized container datatypes providing alternatives to Python’s general purpose built-in containers | Python Software Foundation License
<a href = "https://pandas.pydata.org/"><code>pandas</code></a> | Provides functions for data analysis and manipulation | BSD 3-Clause "New" or "Revised" License
<a href = "https://numpy.org/"><code>numpy</code></a> | Provides a multidimensional array object, various derived objects, and an assortment of routines for fast operations on arrays | BSD 3-Clause "New" or "Revised" License

## About the 2020 Shopee Code League
The **Shopee Code League**, an initiative of the Singapore-based e-commerce company Shopee, is a two-month coding challenge featuring a series of seminars and weekly programming contests on data science, data analytics, and algorithmic thinking. 

The 2020 Shopee Code League is the first edition of this event. As of June 30, 2020, it has drawn the participation of over 20,000 students and professionals from across Singapore, Indonesia, Taiwan, Thailand, the Philippines, Malaysia, China, and Vietnam.

More information can be found on its official page: https://careers.shopee.sg/codeleague/

## Author
- **Mark Edward M. Gonzales** <br/>
  mark_gonzales@dlsu.edu.ph <br/>
  gonzales.markedward@gmail.com
