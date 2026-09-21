Manual Login Test Cases
Test Environment
Application: Sauce Demo
Browser: Chrome
Operating System: Windows
Testing Type: Manual Testing
TC-001 — Valid Login

Test Objective:
Verify that a user can successfully log in using valid credentials.

Test Data:

Username: standard_user
Password: secret_sauce

Steps:

Navigate to the Sauce Demo login page.
Enter standard_user in the username field.
Enter secret_sauce in the password field.
Click Login.

Expected Result:
The user should be successfully authenticated and taken to the application's main inventory page.

Actual Result:
The user was successfully logged in and taken to the application.

Status: PASS ✅

TC-002 — Invalid Password

Test Objective:
Verify that the application prevents login when an incorrect password is entered.

Test Data:

Username: standard_user
Password: Incorrect password

Steps:

Navigate to the Sauce Demo login page.
Enter standard_user in the username field.
Enter an incorrect password.
Click Login.

Expected Result:
The login attempt should be rejected and the user should receive an appropriate error message.

Actual Result:
The login attempt was rejected and the following error message was displayed:

Epic sadface: Username and password do not match any user in this service.

Status: PASS ✅

Additional Observation:
An initial attempt did not display the error message. The test was repeated to verify the behavior, and the error message appeared on the subsequent attempt. No defect was logged because the behavior could not be consistently reproduced.

TC-003 — Blank Password

Test Objective:
Verify that the application prevents login when the password field is left blank.

Test Data:

Username: standard_user
Password: Blank

Steps:

Enter standard_user in the username field.
Leave the password field blank.
Click Login.

Expected Result:
The login attempt should be rejected and the user should receive an appropriate validation message.

Actual Result:
The login attempt was rejected and the following error message was displayed:

Epic sadface: Password is required

Status: PASS ✅
