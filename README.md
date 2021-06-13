# Crawler
This repository contains code for crawling websites coded in Python language.
The code contains the components highlighed in yellow color:

![image](https://user-images.githubusercontent.com/54773570/121823214-31200780-ccbd-11eb-8db5-80ca3b0fd854.png)
# Url Frontier
The URL frontier consists if of front queues and back queues. Initially the URL frontier contains the seed urls stored in the seed.txt file. The process is multithreaded and isolated from each other. To maintain politeness, the wait time for sending another request to the same server is set to be 15 seconds.
# Fetch and Parse
After getting a url from the back queue, it's content is retrieved and stored in an XML file. Then the content of the page is parsed, and all urls are retrieved and then filtered and then added to the frontier. 
# Url Filter
In this component, all the restricted urls written in the robot.txt file are filtered. Then all those urls are removed which have already been crawled or are in the frontier.
