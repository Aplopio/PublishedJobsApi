## Published Jobs Api


This is an api for published jobs on recruiterbox - it provides data in json/xml format. See below for details on our published-jobs api. 

Currently, we expose the following two methods

1. GET ```https://app.recruiterbox.com/api/<clientname>/published_openings```
2. GET ```https://app.recruiterbox.com/api/<clientname>/published_opening/<id>```

where 
- <clientname> is the alphanumeric id associated with your account. If you log in to recruiterbox at ```https://mycompany.recruiterbox.com```, then your ```clientname``` is ```mycompany```
- <id> in method (2) is the id returned for each opening in method (1)

For example, a GET request at ```https://app.recruiterbox.com/api/mycompany/published_openings``` will give you a list of all publicly published openings at a client name "mycompany", while a GET request at ```https://app.recruiterbox.com/api/mycompany/published_opening/12534``` gives you data on the first opening only.

The default return type is json, and you can request an XML response by adding a ```?format=xml``` GET paramater at the end of the above urls.


You can see some sample code that parses the response of the above API here: https://gist.github.com/Aplopio/2156509
