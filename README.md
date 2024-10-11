API Automation with Postman - CRISP

This project contains a Postman collection for automating API testing of the CRISP GET API. 
The collection includes various requests to check response status,response time and verify string in response body.

Prerequisites Postman: 
Ensure you have Postman installed.

Getting Started
Clone or Download the Repository Clone the repository to your local machine using Git or download it as a ZIP file.
https://github.com/ranjitakulkarni/Postman/CRISP

Copy code git clone https://github.com/ranjitakulkarni/CRISP.git

Open Postman Launch Postman on your computer.

Import the Collection Click the "Import" button in the top left corner. Choose the "Link" tab. Paste the URL to the Postman collection:

Copy code https://raw.githubusercontent.com/ranjitakulkarni/CRISP/refs/heads/master/CRISP.postman_collection.json Click "Continue" and then "Import".

Set Up Environment Variables.
Click on the gear icon in the top right corner and select "Manage Environments". 
Create a new environment [QA] and define variables such as: baseUrl: https://apimgmt-dev-crisp.azure-api.net

Execute Tests Select the imported collection from the left sidebar. Choose a request to execute. Click the "Send" button to see the response.

Run Collection Runner (Optional) To run all requests in the collection: Click on the collection name and select "Run".

## Test Cases

| Test Case Name                                      | Test Description                                                                                       | Expected Result                                                                                                    
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------
| Search Patient by valid PatientID                   | Verify Patient information is returned when using GET method with valid Patient ID                    | Patient details is returned including all required information for valid Patient ID,Status Code 200,Response Time,Schema
| Search Patient by invalid PatientID                 | Verify Patient information is not returned & error message is displayed for invalid Patient ID        | Patient details is not returned for invalid Patient ID,Status Code 4XX,Response Time                              |
| Search Patient by providing blank PatientID         | Verify Patient information is not returned & error message is displayed for blank Patient ID          | Patient details is not returned for blank Patient ID,Status Code 4XX,Response Time                                |
| Search Patient by valid Patient Name                | Verify Patient information is returned when using GET method with valid Patient Name                  | Patient details is returned including all required information for valid Patient Name,Status Code 200,Response Time,Schema |
| Search Patient by invalid Patient Name              | Verify Patient information is not returned & error message is displayed for invalid Patient Name      | Patient details is not returned for invalid Patient Name,Status Code 4XX,Response Time                     |
| Search Patient by not providing Patient Name        | Verify Patient information is not returned & error message is displayed for blank Patient Name        | Patient details is not returned for blank Patient Name,Status Code 4XX,Response Time                        |
| Search Patient by valid format of Patient DOB       | Verify Patient information is returned when using GET method with valid Patient DOB                   | Patient details is returned including all required information for valid Patient DOB,Status Code 200,Response Time,Schema |
| Search Patient by invalid format of Patient DOB     | Verify Patient information is not returned & error message is displayed for invalid Patient DOB       | Patient details is not returned for invalid Patient DOB,Status Code 4XX,Response Time                       |
| Search Patient by not providing Patient DOB         | Verify Patient information is not returned & error message is displayed for blank Patient DOB         | Patient details is not returned for blank Patient DOB,Status Code 4XX,Response Time                        |
| Search Patient by valid Address                     | Verify Patient information is returned when using GET method with valid Patient Address               | Patient details is returned including all required information for valid Patient Address,Status Code 200,Response Time,Schema |
| Search Patient by invalid Address                   | Verify Patient information is not returned & error message is displayed for invalid Patient Address   | Patient details is not returned for invalid Patient Address,Status Code 4XX,Response Time                    |
| Search Patient by not providing any Address         | Verify Patient information is not returned & error message is displayed for blank Patient Address     | Patient details is not returned for blank Patient Address,Status Code 4XX,Response Time                    |

