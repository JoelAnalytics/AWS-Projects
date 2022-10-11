## Youtube - Power Bi

**Situation:** We are working for a Company who has already moved to the Cloud (AWS). We will be part of his Marketing team. They want to collect some data from Youtube to create some Dashboards to check the Weekly performance of some Youtube Channels. They want to figure out if there is any relationship between the day of the week that the video was uploaded with the amount of views and likes to find the best time to post their videos.

**Objective:** Execute the processing tasks with AWS (Glue Service) to convert the Raw Data into Processed data to allow users to create their Dashboards.

<img width="2112" alt="AWS WorkFlow" src="https://user-images.githubusercontent.com/46005983/194967828-59150834-1ae9-4b40-a7f7-ecf6bea62f2b.png">

**List of tasks that I've completed in this project:**

- Create an Account ( We won't use our Root Account to execute any task )
- Create an user , groups, roles and attach policies to our group and roles to allow services to connect each other.
- Create 2 Buckets in S3 with some folders to store our Raw Data and Master Data. We've also created an extra Bucket to store the queries that we executed in Athena.
- Create a Glue Job to clean our Data. This Job will take our CSV file from **marketing-raw** Bucket and It will store it in **marketing-master** Buket in PARQUET format.
- Create a Crawler and Database in AWS Glue. The crawler will allow us to have many sources in our Data Catalog after scaning.
- We used Athena to run queries in SQL format to explore our Data. We will use this service to conect AWS with Power BI
- We will create 2 Lambda functions to automatize the entire process. This will allow us to upload a file to S3 Bucket raw and then everything will be excecuted automatically and the final result will be available in Athena.
