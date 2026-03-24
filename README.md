API Testing Project- Workflow & Negative Testing (Postman)  

Overview: This project demonstrates end-to-end API testing of a Trello-like system using Postman. It focuses on validating core CRUD workflows, negative scenarios, and data reliability across requests.

🎯 Objectives:

-Validate core API workflows (Create → Read → Update → Delete).    
-Apply risk-based testing principles.  
-Implement negative testing scenarios.  
-Ensure data consistency across requests.  
-Demonstrate structured QA thinking using Postman scripting.  


Testing Strategy: This project follows a real-world QA approach:  

✅ 1. Happy Path Validation  
-Validate core workflow functionality.  
-Ensure endpoints return expected status codes (200/201).  
-Confirm resources are created, updated, and deleted correctly.  

⚠️ 2. Negative Testing (High Priority)  
-Invalid resource IDs (randomized strings).  
-Missing or malformed inputs.  
-Deleted resource validation (expecting 404).  
-Error handling and response validation.  

🔄 3. Workflow Validation  
-Chain requests using dynamic data (IDs).  
-Validate data persistence across multiple requests.  
-Ensure system behaves correctly after state changes.  

🧾 4. Assertions & Validation
-Status code validation.  
-Response body checks.  
-Data integrity verification.  
-Console logging for debugging and traceability.  

🛠 Tools & Technologies:  
-Postman (Collections, Environments).  
-JavaScript (Pre-request & Test scripts).  
-REST APIs.  

📊 Example Test Scenarios  
-Create resource → verify success (200/201).  
-Retrieve resource → validate correct data.  
-Delete resource → verify removal.  
-Retrieve deleted resource → expect 404.  
-Invalid ID request → validate error handling.  

📸 Screenshots Included:  
-Example request + response validation.  
-Pre-request scripts (dynamic data handling).  
-Post-response tests (assertions & validation).  
-Negative test case execution.  

🚀 How to Use:  
-Import the Postman collection.  
-Set up an environment with: API key, Token.  
-Run requests individually or as a collection.  

💡 Key Takeaways:  
-Demonstrates backend-focused QA skills.  
-Highlights risk-based and negative testing mindset.  
-Shows ability to validate workflows, not just endpoints.  
-Uses scripting to simulate real-world test automation patterns.  
