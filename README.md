# OrangeHRM BDD Automation Test

The framework has been built using the Page Object Model (POM) concept and TestNG. This project
contains automated BDD test scenarios for the OrangeHRM demo application, implemented using 
the Page Object Model design pattern. The following flow is covered in this project:

1. Log in to the OrangeHRM application using admin credentials.
2. Navigate to the Admin module and create a new Job Title by providing job title, description, and notes.
3. Verify the success message after saving the job details.
4. Navigate to the PIM module and add a new employee with personal information.
5. Enable Create Login Details and provide the username and password for the employee.
6. Verify the success message after saving the employee record.
7. Update the employee details by selecting Male on the Employee List page and save the changes.
8. Verify the successful update message.
9. Log out from the application using the profile dropdown.

                              BDD Testcases

Scenario: Login, create job title, add employee, update gender, and logout
    Given User navigates to "https://opensource-demo.orangehrmlive.com/web/index.php/auth/login"
    When the user enters username "Admin" and password "admin123"
    And the user clicks on the login button
    And the user clicks on the Admin button
    And the user clicks on the Job button
    And the user selects Job Titles from the dropdown
    And the user clicks on the Add button
    And the user enters Job Title, Job Description, and Notes
    And the user clicks on the Save button
    Then the message should be displayed as "Save Successfully."
    When the user clicks on the PIM button
    And the user clicks on the Add Employee button
    And the user enters FirstName, MiddleName, and LastName
    And the user enters a new Employee ID number
    And the user clicks on Create Login Details
    And the user provides Username, Password, and Confirm Password
    And the user clicks on the Save button
    Then the message should be displayed as "Save Successfully."
    When the user navigates to the PIM Employee List page
    And the user selects the male gender
    And the user clicks on the Save button
    Then the message should be displayed as "Successfully Updated."
    When the user clicks on the menu dropdown in the top right corner
    And the user clicks on Logout
    Then the user should be logged out successfully


