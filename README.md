# **Stock Market Kafka Real-Time Data Engineering Project**

## **Introduction**  
This project demonstrates an **end-to-end data engineering pipeline** for handling **real-time stock market data** using **Apache Kafka** and AWS services. The project showcases how to stream, process, store, and query large volumes of stock market data efficiently.  

### **Key Objectives**:  
- Stream real-time stock market data using **Apache Kafka**.
- Process and store data in **AWS S3** for scalability and durability.
- Use **Glue Crawlers** and **Glue Catalog** to build a metadata catalog for the data lake.
- Query processed data using **AWS Athena**.
- Visualize insights using SQL queries and analytics tools.

---

## **Technologies Used**  

### **Programming Language**  
- Python  

### **AWS Services**  
1. **S3 (Simple Storage Service)**: For storing processed data.  
2. **Glue Crawler**: To crawl and organize the data schema.  
3. **Glue Catalog**: To create a centralized metadata repository.  
4. **Athena**: For querying the processed data stored in S3.  
5. **EC2**: For hosting Kafka and running the pipeline.
6. **QuickSight**: for visualization and analysis


### **Big Data Tools**  
- **Apache Kafka**: For real-time data streaming.  

---

## **Architecture**  
<img src="Architecture.jpg">
The architecture follows a modular design, comprising the following components:  

1. **Data Producer**:  
   - A Python script simulates stock market data and streams it into Kafka topics.  

2. **Apache Kafka**:  
   - Manages real-time data streaming using topics.  

3. **AWS S3**:  
   - Stores the processed stock market data as raw and transformed files in a data lake.  

4. **Glue Crawler and Catalog**:  
   - Automates schema creation and organizes data for querying.  

5. **Athena**:  
   - Executes SQL queries on the data stored in the S3 bucket for analytics.  

---

## **Dataset Details**  

The project uses a **simulated dataset** named `indexProcessed.csv`, which contains the following fields:  
- **Timestamp**: The date and time of the stock data point.  
- **Stock Symbol**: The unique ticker symbol for the stock (e.g., AAPL for Apple Inc.).  
- **Price**: The current trading price of the stock.  
- **Volume**: The number of shares traded during the given timestamp.  
- **Open Price**: The stock's opening price for the day.  
- **High Price**: The stock's highest price during the day.  
- **Low Price**: The stock's lowest price during the day.  

---

## **Steps to Execute the Project**  

1. **Setup Kafka**:  
   - Install and configure Apache Kafka on an EC2 instance.  
   - Create Kafka topics for streaming stock market data.  

2. **Simulate Real-Time Data**:  
   - Write a Python producer script to simulate stock market data and publish it to Kafka topics.  

3. **Consume Data from Kafka**:  
   - Develop a Python consumer script to read data from Kafka topics and store it in AWS S3 in **CSV format**.  

4. **Setup AWS Glue**:  
   - Configure a Glue Crawler to organize and catalog the stock market data stored in S3.  

5. **Query Data using Athena**:  
   - Use Athena to run SQL queries on the cataloged data.  
   - Generate insights such as the highest traded stock, daily price trends, etc.  

6. **Visualize Data (Optional)**:  
   - Use tools like AWS QuickSight, Tableau or Power BI to visualize the queried data for better insights.  

---

## **Folder Structure**  
