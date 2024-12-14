# Project---FileHandler
# Introduction

Accurate and efficient management of product information is essential for the success of e-commerce businesses. This information enables informed decision-making and facilitates effective marketing strategies. However, traditional methods of handling product data may be cumbersome and prone to errors. They often involve manual entry and maintenance processes, leading to inconsistencies and inefficiencies. By harnessing the capabilities of Python programming, we can develop a solution that automates tasks such as adding, reading, updating, and deleting product information. This streamlined approach not only enhances data accuracy and reliability but also improves operational efficiency.

The kind of operations that we are going to focus on have an acronym: CRUD (Create, Retrieve, Update, and Delete).

 CRUD operations represent the four basic functions that are essential to interact with a database or a data storage system. The acronym CRUD stands for Create, Read, Update, and Delete. These operations form the foundation of most applications that store and manipulate data. Understanding CRUD is crucial for developers working on web, software, and database applications.

Here's a brief overview of each operation:

- Create: This operation is used to add new records to a database. It involves inserting data into a database table or a data structure. For example, adding a new user to a user database is a Create operation.

- Read: The read operation is used to retrieve or read data from a database. It involves querying the database to fetch information based on certain criteria. For example, fetching a list of all users from a user database is a Read operation.

- Update: This operation is used to modify existing data in a database. It involves updating one or more fields of a database record. For example, changing a user's email address in a user database is an Update operation.

- Delete: The Delete operation is used to remove records from a database. It involves deleting one or more records from a database table. For example, removing a user from a user database is a Delete operation.

These operations are vital for managing data effectively in any application. They allow applications to perform basic data management tasks, ensuring that the data is accurate, consistent, and accessible.

 In this project, we'll implement a customized version of CRUD operations. Here's an overview of what you'll build:

1. Create: The creation process is handled by the create() function, which orchestrates three sub-functions:

- add_sales_data(): Adds sales data.

- add_product_details(): Adds product details.

- add_product_descriptions(): Adds product descriptions.

2. Read: The reading process is facilitated by the read() function, which coordinates three sub-functions:

- display_sales_data(): Displays sales data.

- display_product_details(): Displays product details.

- display_product_descriptions(): Displays product descriptions.

3. Update: The updating process is managed by the update() function, which invokes three sub-functions:

- update_sales_data(): Updates sales data.

- update_product_details(): Updates product details.

- update_product_descriptions(): Updates product descriptions.

4. Delete: Deletion is handled by the delete() function.

5. CRUD: The master function, crud(), serves as the central hub, orchestrating all the operations to perform CRUD actions seamlessly from a single point.

 The file and the data set used in this project are available in the folder called "LW - Python Project - FileHandler" in the student folder linked here.

# Problem Statement
In the dynamic landscape of e-commerce, efficient management of product information is essential for businesses to thrive. However, organizing and updating vast arrays of product details, sales data, and product descriptions can be a daunting task without the right tools in place. The absence of a robust system for managing product information can lead to inconsistencies, errors, and inefficiencies in operations.

 To address this problem, you have been hired as a software developer for a Software company that builds various technologies for e-commerce platforms. Your job is to utilize your programming knowledge to automate some of the tasks that occur in these e-commerce platforms. Specifically, your role involves implementing functionalities for seamlessly adding, reading, updating, and deleting product details, sales data, and product descriptions. 

# Understanding the Data
You have one main folder called main_folder containing one CSV file and 2 subfolders called product_details and product_description. The directory structure is expected to be as follows:

The sales_data.csv contains sales data for various products over 14 days. Each row represents a unique product identified by its Product_SKU, and each column represents the number of sales for that product on a specific day (Day1 to Day14). The values in the cells indicate the number of units sold for each product on the corresponding day.

The product_details folder contains JSON files named after each product's SKU (e.g., details_AISJDKFJW93NJ.json, details_DJKFIEI432FIE.json). These JSON files contain detailed information about each product, such as its name, brand, model, specifications, price, and availability. For example, take a look at the below screenshot of the JSON file details_AISJDKFJW93NJ.json.

The product_description folder contains TXT files named after each product's SKU (e.g., description_AISJDKFJW93NJ.txt, description_DJKFIEI432FIE.txt). These TXT files contain descriptions of each product. For example, take a look at the below screenshot of the TXT file description_AISJDKFJW93NJ.txt.

Q1: Your first task is to set up the environment for this project by loading the required packages and modules.

You will achieve all of this by completing the following sub-task:

1. Write code to import the following packages:

- For handling raw data files: os

- For working with JSON files: json

- For working with CSV files: csv

- For pretty-printing Python data structures: pprint

Q2: Then, you will ensure that the necessary files are loaded into the working environment. This includes loading sales data from a CSV file, product details from JSON files, and product descriptions from text files. 

We recommend that you either use Jupyter Notebook or Google Colab to build and execute your code. You will achieve all of this by completing the following tasks:

1. In case you are using Google Colab,

- import drive from google.colab and mount your Google Drive or

- import files from google.colab.

2. In case you are using Jupyter Notebook, please make sure that your files and folders are all in the right place.

3. Use a function named load_data() to read data from the sales_data.csv file, JSON files in the product_details folder, and TXT files in the product_description folder and store them in three dictionaries called sales_data, product_details and product_desctiptions.

Q3: Next, you will explore the loaded data by displaying its content. This includes displaying sales data, product details, and product description of products using their product SKU.

You will perform the following in this task:

1. Display sales_data, product_details, and product_descriptions dictionaries.

2. Create a list named product_skus which contains product SKUs extracted from one of the dictionaries using dict.keys().

3. Display sales data, product details, and product description of a product using the product_skus list.

4. Find the length of sales_data, product_details, and product_descriptions dictionaries.

Q4: A new laptop model, the Acer Aspire 3, laptop has been launched by Acer.  Your task is to create a function that lets the admin add sales data, product details, and product description for this new product.

The code should help the admin to accomplish the following tasks:

1. Use a function named add_sales_data() to add sales data for Acer Aspire 3, which has the following sales data:

- Product SKU: TYS56KFJW93NJ

- Sales data for the past 14 days:  [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]

2. Use a function named add_product_details() to add new product details for Acer Aspire 3, which has the following product details:

- Product name: Laptop

- Brand: Acer

- Model: Acer Aspire 3

- Specifications: Intel Core i3 N305 Laptop (Windows 11 Home/8 GB/512 GB SSD) A314-36M, 35.56 cm (14") Full HD Display, 1.4 KG, Pure Silver

- Price: INR 32,999.00

- Availability: In stock

3. Use a function named add_product_description() to add a product description for Acer Aspire 3, which has the following product description:

- Product Description: The Aspire 3 is ready to go with the latest Intel® Core™ i3 N-Series Processors1 with UHD Graphics—ideal for the entire family, with performance and productivity at the core. Perfect to get more out of work, study, or play.

4. Use a function named create() that calls the functions defined in 1, 2, and 3 to add product details, sales data, and product descriptions for the Acer Aspire 3 laptop at once.

Q5: Let’s say the admin wants to review the details of the Acer Aspire 3 laptop before making any updates. In this case, you'll create functions to allow the admin to display the sales data, product details, and product description of the Acer Aspire 3 laptop.

The code should help the admin to accomplish the following tasks:

1. Use a function named display_sales_data() to display sales data for Acer Aspire 3.

2. Use a function named display_product_details() to display product details for Acer Aspire 3.

3. Use a function named display_product_descriptions() to display product description for Acer Aspire 3.

4. Use a function named read() that calls the functions defined in 1, 2, and 3 to display sales data, product details, and product descriptions for Acer Aspire 3 at once.

Q6: Acer decides to release a software update for the Acer Aspire 3 laptop, which includes performance enhancements, new features and price increases. In this task, you will implement functionality to let the admin update sales data, product details, and product description. 

The code should help the admin to accomplish the following tasks:

1. Use a function named update_sales_data() to update sales data for Acer Aspire 3

2. Use a function named update_product_details() to update product details for Acer Aspire 3.

3. Use a function named update_product_descriptions() to update the product description for Acer Aspire 3.

4. Use a function named update() that calls the functions defined in 1, 2, and 3 to update sales data, product details, and product descriptions for Acer Aspire 3 at once.

Q7: Suppose Acer discontinues the production of the Acer Aspire 3 laptop due to the release of its successor, the Acer Aspire 4.  The admin wants to remove all information related to the Acer Aspire 3. In this task, you will implement functionality to let the admin delete sales data, product details, and product description.

The code should help the admin to accomplish the following task:

1. Use a function named delete() to delete sales data, product details, and product descriptions for Acer Aspire 3 whose product SKU is TYS56KFJW93NJ at once.
