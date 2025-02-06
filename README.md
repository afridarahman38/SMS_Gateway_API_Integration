# SMS_Gateway_API_Integration_Testing
This repository documents the **API Testing** conducted for the SMS Gateway API Integration of a bank. The purpose of this testing was to verify the functionality, security, and reliability of the API endpoints using **Postman.** The tests were designed to ensure that the bank’s SMS gateway API meets expected behavior and can handle various real-world scenarios, such as login authorization, OTP generation, and token management.

## Project Overview
In this project, we focused on testing the integration between the bank’s mobile application and its SMS gateway. The **Mobile Send API** is responsible for generating OTPs and sending them to users’ mobile numbers, while the **Login API** handles user authorization through login credentials and authentication tokens. The testing was focused on ensuring that:

-- The system responds correctly to valid and invalid user credentials.
-- OTPs are sent only with valid and authorized tokens.
-- Expired or missing tokens are properly handled by the API.
-- The system performs as expected when interacting with invalid mobile numbers.

## Testing Details
- **Testing Category:** Non-Functional Testing
- **Testing Type:** API Testing
- **Tool Used:** Postman

## Issues and Improvements
While most of the test cases passed successfully, there was a failure when using expired or older auth tokens to send OTPs. This behavior needs to be addressed to improve security and ensure that expired tokens do not bypass the system’s restrictions.

-- **Issue:** The system allowed OTPs to be sent with expired auth tokens.
-- **Suggested Improvement:** Implement a stricter validation process for token expiration and ensure the system responds with an unauthorized access message when using invalid or expired tokens.

## Conclusion
The **SMS Gateway API** performed well in most of the test cases, meeting the expected results for user authorization and OTP delivery. However, the issue with expired tokens highlights the need for further security enhancements. This testing project provided valuable insights into the API’s functionality and its potential for integration with the bank’s mobile platform.

## Future Work
-- Investigate and resolve the expired token issue.
-- Continue testing for edge cases, such as invalid data formats and rate-limiting behaviors.
-- Automate these test cases using Postman collections for continuous integration in the development pipeline.



##### Feel free to explore, clone, or contribute to this project! If you find any issues or would like to suggest improvements, please open an issue or submit a pull request.
