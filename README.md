# Gurukula
Automation Test Suite 
THis is the automation framework for the Gurukula application.

# Prerequisite
Following are the pre-requisites for the same:
## Eclipse IDE with TestNG 
## JDK 1.7 or higher
## Supporting JAR files (provided)
## apache tomcat (if needed to host the application)
## selenium jars
## Chrome Web Driver


## Instructions:
1. To launch the test suite, the provided project must be imported to the current workspace.
2. Configure the build path with respective jars
3. Resolve all the configuration issues if needed by importing the respective plugins (TestNG)
4. All the test cases are data driven
5. The data are fetched from the Excel Sheet (src\testData\TestData 1.xlsx)
6. To run the Test cases, make sure the data sheet has neccessary data.
7. Few actions like Login, Adding Staffs etc,. needs to be specified using the respective Action Column in the excel sheet.
8. Individual test cases can be run by clicking the Run as -> TestNG from the RUN menu. (src\testCases\TC_xx.java)
9. To run all the test cases, locate the TestNG.xml (configured to run the testcases).
10. The Test Run Report is generated in .html format for reporting purpose, which can be found in src\test-output\Test Suite\index.html.
11. Screenshots are taken for major actions that are performed on that page, which can be found on  src\Screenshots

## Defects found

### Defect 1: 
After clicking on the Login > Reset Password Page > Login, enter the valid credentials, the page is navigated to the Reset Password page.
### Defect 2: 
When the Email ID is given as admin@gmail, admin@admin, admin@local without the top level domain name, it doesnt not throw error for email validation. This behavour is found in all the pages where email is needed.
### Defect 3: 
The inline error message for Max character length for the Email is displayed for 100 or more characters while it should display for char length > 50. This behavour is found in all the pages where email is needed.
### Defect 4: 
No success message is shown after clicking the Reset Password Button.
### Defect 5: 
Register Page: Cannot successfully register even after providing correct data.
### Defect 6: 
Branches Page: No buttons for pagination is provided.
### Defect 7: 
We are able to create multiple branches with same Branch Code
### Defect 8: 
Can create duplicate staffs with same data.
### Defect 9: 
Admin Page: The changes were not saved.
### Defect 10: 
Password Page: The changes were not saved.
