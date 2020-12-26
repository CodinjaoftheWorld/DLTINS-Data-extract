This repository is showing the steps to create lambda function for extracting the data from xml file provided in the assignment of the Python Engineer role in Steel-eye company.

Steps:
1. Create and activate the virtual environment named 'steeleye'. 
>> virtualenv -p /usr/bin/python3.6 steeleye

>> cd steeleye

>> source bin/activate

2. go to site-packages directory
>> cd lib/python3.6/site-packages

3. Install the requirements from requirements.txt
>> pip install -r requirements.txt 

4. Create a file lambda_fucntion.py in the current working directory and define your function in this file.

5. Create a zip file named ‘lambda_function.py’ with the following directories/files in the same directory.
- certifi(dir)
- chardet(dir)
- _distutils_hack(dir)
- idna(dir)
- requests(dir)
- urllib3(dir)
- distutils-precedence.pth(file)
- lambda_function(file)

 
6. Log in to the AWS console and access the lambda service.

7. Create a new function with the name ‘Steeleye’. Import the zip file created in step 5 from Actions button.
After the successful import content of the zip file should be visible in the Environment pane, visible towards the left side.

8. Go to Runtime settings by scrolling down, select runtime as ‘Python 3.6’, and save the changes.

9. Go to Basic Settings by further scrolling down the screen and increase the Memory(MB) to 4096 and Timeout to 5 mins.

10. Create a bucket in S3 services with the name of ‘steeleyetest3424’ and save the bucket.

11. Deploy the function by clicking on the ‘Deploy’ button.

12. Test the function by clicking on the ‘Test’ button.
13. Once the test is successful, open the S3 bucket, access the 'tmp' directory within the S3 bucket, and access the datafile.csv to get the records mentioned in the assignment. (datafile.csv file has 0.5 Million records). Data file is attached to the repository.
