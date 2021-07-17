# Starbucks_DataWarehouse_OLAP
OLAP cube(s) and BI Layer of the Starbucks Data Warehouse implemented using SSDT, SSAS and Excel Visualizations along with SSRS Repots.

Data extracted are related to Starbucks customer interactions with offeres sent by the company and other transactions done by the customers. The aim of the data warehouse in the data engineering perspective is to maintain customer details, offer details, track customer's location details over times, provide a way to convert currency types and amounts using relavent daily exchange rates which means maintaining daily exchange rates, and keep transactional data of customer interactions with offers and other payments.

# Initial Source(s):
* https://www.kaggle.com/blacktile/starbucks-app-customer-reward-program-data
* Note that the initial dataset has been changed to replicate datasets of different types and to enable a rich set of ETLs.

# Sources Prepared using the initial dataset:
* starbucks_offers MySQL database - offer data and offer type data.
* Starbucks_Offers MSSQL database - channel data which the offers are being sent.
* Profile.txt - customer profiles.
* Location.txt - customer addresses.
* transcript.csv - a set of two years worth of transactions and offer interactions done by customers.
* Exchange Rates API - an API call to free.currconv.com/api/v7 to get daily exchnge rates: USD to LKR and vice versa.

# EER
![image](https://user-images.githubusercontent.com/31137252/119243627-1bb83180-bb86-11eb-9e49-9087604a116b.png)

# Data Warehouse Architecture and Schema
![image](https://user-images.githubusercontent.com/31137252/119243743-4eaef500-bb87-11eb-8666-45b839c46650.png)
![image](https://user-images.githubusercontent.com/31137252/119243750-59698a00-bb87-11eb-8e35-14108b62e167.png)
*. EventSK in the FactTable had been added mistakenly and was removed in the current version of the OLAP solution.

# SSRS Report Types Available
* Drill-down
* Drill-through
* Parameterized
* Matrix

# Dashboard in Excel
![sb_dashboard_excel](https://user-images.githubusercontent.com/31137252/126027319-a2cde124-46e8-46ba-afba-04a168a483db.png)

*. for more info: refer the complete project report.
