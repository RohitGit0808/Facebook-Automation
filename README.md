📘 Facebook Signup Automation – Select DOB from Dropdown

📌 Problem Statement

Automate the Facebook Signup form to validate Date of Birth (DOB)
 selection using different methods from Selenium’s Select class and perform end-to-end form interaction
  with data-driven testing.

---

🎯 Objectives

Automate form interactions on Facebook’s signup page

Select Day, Month, and Year using:
selectByVisibleText() → for Day
selectByIndex() → for Month
selectByValue() → for Year

Fill form fields with data from an Excel file

Validate error messages for:
Missing password
Invalid mobile number

Capture screenshots and generate detailed reports

---

💡 Technologies Used

Java 11

Selenium WebDriver 4.34.0

TestNG 7.8.0

Apache POI 5.4.1 (for Excel data)

ExtentReports 5.0.9 (for reporting)

Maven

WebDriverManager 6.2.0

Eclipse IDE



---

📁 Project Structure

facebook-automationdob/
├── src/
│ ├── main/
│ │ └── java/
│ │ └── com.facebook/
│ │ ├── base/
│ │ │ └── DriverSetup.java
│ │ ├── pages/
│ │ │ ├── Facebook_Login_Page.java
│ │ │ └── Signup_Page.java
│ │ ├── utils/
│ │ │ ├── ExcelReadWrite.java
│ │ │ ├── ExtentReportManager.java
│ │ │ └── ScreenshotUtility.java
│ │ └── models/
│ │ └── UserData.java
│ └── test/
│    └── java/
│       └── com.facebook.tests/
│         └── FacebookSignup_Test.java
├── testng.xml
└── pom.xml
---

🧾 Test Workflow Overview

1. Launch the browser based on the configuration


2. Navigate to Facebook.com


3. Click “Create New Account”


4. Fill in First Name, Last Name, and Mobile Number using data from Excel


5. Leave the Password field blank to validate the password error message


6. Select Date of Birth (DOB):

Day: selected by visible text
Month: selected by index
Year: selected by value



7. Choose Gender based on Excel input


8. Submit the form


9. Validate displayed error messages for:

Password

Mobile number



10. Print the error messages to the console


11. Close the browser




---

🧪 Test Case Highlights

testFacebookSignup

Verifies that the Facebook signup form can be filled using test data
Ensures dropdowns are selected using different methods of Selenium’s Select class
Validates error handling for incomplete input fields
Supports data-driven testing with multiple datasets



---

▶️ How to Run the Tests

Using Eclipse
Import the project
Right-click on testng.xml
Select Run As → TestNG Suite


Using Command Line

Open terminal in the project directory
Run: mvn clean test



---

📸 Test Artifacts

Screenshots for both success and failure scenarios
HTML reports using ExtentReports
Console logs and structured logging using Log4j2
TestNG and JUnit-style reports in output folder



---

🛠️ Troubleshooting

Issue Solution

Browser not launching Check driver setup in config.properties
Excel data not loading Ensure correct file path and sheet name
Locators not working UI might have changed — update element locators
Timeout errors Adjust wait times in configuration
TestNG not detected Ensure the TestNG plugin is installed in Eclipse



---

📌 Key Features

Page Object Model (POM) for clean structure
Excel-driven testing for flexibility and scalability
Multiple dropdown handling techniques
Detailed reporting with ExtentReports
Error validation and logging
Reusable utility classes for screenshots, Excel reading, waits, and reporting
Cross-browser support with WebDriverManager




