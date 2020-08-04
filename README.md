# Order Brushing Detection
**Order brushing** is a fraudulent practice in which shops create an artificial increase in their number of sales in an attempt to bolster their reputation and increase their ratings on e-commerce websites. 

The goal of this project is to create a baseline rule-based program that can be used to detect potential order brushing. 

## Task
This order brushing detection activity, which highlights the importance of data analytics in e-commerce, is the **Week 1 Contest (Student Category)** of the **2020 Shopee Code League**. 

### Dataset
The dataset, stored in a comma-separated values (CSV) file, consists of four columns:
- *Order ID* - a unique ID is assigned to every transaction
- *Shop ID* - a unique ID is assigned to every seller
- *User ID* - a unique ID is assigned to every buyer
- *Date and time of order* - the timestamp of every transaction is recorded

Note that the dataset is an intellectual property of the contest organizers. Therefore, the CSV file containing the data is not published in this project. For the same reason, the output of each cell in the Jupyter Notebook is also stripped. 

### Order Brushing
Order brushing is checked for every possible one-hour window. A shop is said to have conducted order brushing if its *concentration rate* (ratio of the number of transactions to the number of unique buyers) for a particular one-hour window is at least 3.0.

In addition, for every shop found to have conducted order brushing, the shop IDs of the *suspicious buyers* (those who registered the highest number of transactions during order brushing periods) have to be identified. 

### Submission Format
The results of the data analysis have to be stored in a CSV file consisting of two columns:
- *Shop ID* 
- *User ID(s) of suspicious buyer(s)*

If a shop is not found to have conducted order brushing, the entry in the second column is set to 0. For shops with more than one suspicious buyer, the user IDs are listed in ascending order and separated using an ampersand (without any space before and after it).

Since the dataset is an intellectual property of the contest organizers, the CSV file containing the results is also not published in this project. 

## Built Using
This project was built using a **Jupyter Notebook**. The following Python modules and libraries were used:
- *math* - https://docs.python.org/3/library/math.html
- *csv* - https://docs.python.org/3/library/csv.html
- *collections* - https://docs.python.org/3/library/collections.html
- *pandas* - https://pandas.pydata.org/
- *NumPy* - https://numpy.org/

The first three are part of the Python standard library while the latter two are open-source, BSD-licensed libraries.

## About the 2020 Shopee Code League
The **2020 Shopee Code League**, an initiative of the Singapore-based e-commerce company Shopee, is a two-month coding challenge featuring series of seminars and weekly programming contests on data science, data analytics, and algorithmic thinking. As of June 30, 2020, it has drawn the participation of over 20,000 students and professionals from across Singapore, Indonesia, Taiwan, Thailand, the Philippines, Malaysia, China, and Vietnam.

More information on the said event can be viewed on its official page: https://careers.shopee.sg/codeleague/

## Author
- **Mark Edward M. Gonzales** <br/>
  mark_gonzales@dlsu.edu.ph <br/>
  gonzales.markedward@gmail.com
