## Youtube - Power Bi

**Situation:** We are working for a Company who has already moved to the Cloud (AWS). We will be part of his Marketing team. They want to collect some data from Youtube to create some Dashboards to check the Weekly performance of some Youtube Channels. They want to figure out if there is any relationship between the day of the week that the video was uploaded with the amount of views and likes to find the best time to post their videos.

**Objective:** Execute the processing tasks with AWS (Glue Service) to convert the Raw Data into Processed data to allow users to create their Dashboards.

**List of tasks that I've completed in this project:**

- Create Account ( We won't use Root Account to execute any task )
- Create user , groups, roles and attach policies to our group and roles to allow services to connect each other.
- Create 2 Buckets in S3 with some folders to store our Raw Data and Master Data. We also created an extra Bucket to store the queries we executed in Athena.

![Bukets](https://user-images.githubusercontent.com/46005983/194966245-cf13f507-9dca-4bd2-a44b-cb1c0ca254c8.JPG)

- Create a Glue Job to clean our Data. This Job will take our csv file from **marketing-raw** Bucket and It will store it in **marketing-master** Buket after processing in Parquet format.

![GlueJob](https://user-images.githubusercontent.com/46005983/194966849-8d8bf1ee-7c64-439b-9b72-c4248c845bcb.JPG)

- Create a Crawler and Database in AWS Glue. The crawler will allow us to have many sources in our ata Catalog after scaning.




<img width="2112" alt="AWS WorkFlow" src="https://user-images.githubusercontent.com/46005983/194967828-59150834-1ae9-4b40-a7f7-ecf6bea62f2b.png">


