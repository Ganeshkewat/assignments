# assignments
Case Study Assignment for Data Engineer
The case study consists of two parts:
- Hands-on Assignment – tests the technical abilities of a candidate in an example that is very
similar to a daily bread of a data engineer with focus on relevant technology, concepts, and
programming languages.
- Theoretical Assignment – tests the ability of a candidate to read and understand technical
concepts and pass them to other stakeholders in a proper and well-written form.
Please don’t forget to collect the required output documents and send the to the recruiter
organizing the interview.
You can contact petr.svec@emea.merkleinc.com with any questions related to the assignments.
Hands-on Assignment
Prerequisites
- Identify files needed for the exercise saved in the public S3 bucket:
o https://merkle-de-interview-case-study.s3.eu-central1.amazonaws.com/de/user.csv
o https://merkle-de-interview-case-study.s3.eu-central1.amazonaws.com/de/order.csv
o https://merkle-de-interview-case-study.s3.eu-central1.amazonaws.com/de/item.csv
o https://merkle-de-interview-case-study.s3.eu-central1.amazonaws.com/de/event.csv
- Spin up a Spark environment of your choice. If you don’t have one at your disposal, we
recommend a Databricks Community instance (the one that is not hosted on AWS, Azure nor
GCP) available at https://databricks.com/try-databricks. It is free, does not expire and does
not require a payment card.
Assignment
- Load prerequisite files from S3 to HDFS (or alternative like DBFS or S3).
- Using your business acumen understand the content of the files.
- Create a spark script to create a small data lake that would consist of:
o 1. Layer
▪ Contains external tables for all prerequisite files
▪ All attributes are of STRING type. No transformations are applied.
o 2. Layer
▪ Contains all datasets from the first layer
▪ All attributes have common naming convention
▪ All attributes have proper datatypes based on the attribute name and
common logic
▪ All struct collection attributes are flattened and transformed to proper data
types
▪ Fact tables are properly partitioned based on meaningful attributes
o 3. Layer
▪ Contains following data marts:
• “top_items” data mart with all sold items with additional attributes:
o For every year (based on the created_at attribute):
▪ Total number of an items sold in a particular year
▪ Rank of an item based on the total number of items
sold in a particular year
▪ Total sales from an item in a particular year
▪ Rank of an item based on the total sales in a
particular year
o Total number of items sold in all years
o Rank of an item based on the total number of sales
o Total sales of an item in all years
o Rank of an item based on the total sales
• “top_buyers” data mart with top 20 customers who contributed on
the total sales the most with additional attributes:
o Total sales contributed
o Rank based on the total sales
o Last order creation date
o The overall most viewed item of a customer
Expected Output
- IPython Notebook with Python or Scala script that contains all actions necessary to fulfil the
assignment including required DDLs
o PySpark is preferred
o All code blocks should be documented
o Data mart creation and attributes are documented using Markdown
Theoretical Assignment
- Explain in couple of paragraphs the difference between Data Lakehouse and Data
Warehouse
o Focus on the benefits of the Data Lakehouse
o Explain the main enablers of the Data Lakehouse
o Try to suggest a reference architecture for a Data Lakehouse in cloud (e. g. AWS)
- Imagine that reader of your document is a client who is budget owner with limited technical
knowledge
Expected Output
- PowerPoint, Word, or any other document format you consider fitting.
