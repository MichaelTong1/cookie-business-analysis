# cookie-business-analysis
Using PowerBI, analyzing a cookie business using their order invoices

### Feb 23 2024

My first data engineering project. Although I have had experience in Power BI before, the last time I worked with it was 2021. 

The YouTube video I will be referncing is: 

[Power BI Tutorial for Beginners](https://www.youtube.com/watch?v=NNSHu0rkew8)

The two tables we have are Customers and Orders.

### Feb 24 2024

Preview of Customers: 
| Customer ID      | Customer Name | Phone | Address | City | State | Zip | Country
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | 
| 152689|	YT Restaurants|	999-999-9999|	123 Main Street|	Seattle|	WA	 | 98121	|United States |
|452584	| Acme Grocery Stores	|801-583-8695	|3215 Tori Lane	|Salt Lake City	|UT	|84113	|United States
| ... | ... | ... | ... | ... | ... | ... | ... | 
325698	|Cascade Grovers|	251-655-2909	|2217 Lonely Oak Drive|	Seattle|	WA	|98121	|US

Prevew of Orders: 
| Order ID|	Customer ID	|Rush Shipment|	Cookies Shipped	|Revenue	|Cost	|Order Date
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- 
|103190	|152689	|Yes	|526	|2630	|1315|	2/10/2022
|103240|	325698	|No	|774	|3870	|1935|	6/18/2022
| ... | ... | ... | ... | ... | ... | ... |
999861	|452584	|Yes	|457	 |$2,285.00 	 |$1,142.50 	|3/20/2020

There are some inconsistencies within the data, therefore some clean up is needed. For example, the **revenue** and **cost** columns in Orders are consistent. Some are formatted as currency and some are plain numbers. Let's convert all of these values to currency for simplicity. 


![In PowerBI, we can do this easily by choosing Currency as the format](/Images/ChangingtoCurrency.png "Updating the format from General to Currency")

### Feb 26 2024

Today I noticed that the country column had inconsistent data. There were some labeled "United States" and some labeled "US." For simplicity, let's transform all of the data so it says United States. To ensure that any future data will be consistent, we will need to make this change in the front-end, whether it's a POS (point of sales) system, a web application, or even human error. Placing data validation is important to ensure consistent and accurate data. 

![If we go into the Home tab --> Transform Data, then we can make this change here.](/Images/ConvertingUS.png "Converting US to United States")

### Feb 28 2024 

After a few days of working on the visual, I have decided to present two pages. One is the home page where we can see the raw data. The second is the dashboard where we can see the visuals. 

![Here we can see the data page](/Images/Visual-Version1.png "Data Page")
