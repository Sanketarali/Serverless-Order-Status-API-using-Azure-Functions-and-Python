# Serverless-Order-Status-API-using-Azure-Functions-and-Python
This project is a serverless API developed using Azure Functions and Python, designed to efficiently manage order status updates. It dynamically connects to an Azure SQL Database to fetch and return order details, ensuring cost efficiency and scalability by provisioning servers only when invoked.

# Features

Serverless Architecture: No need for continuous server management; runs only when called.

Azure SQL Integration: Retrieves real-time order details dynamically.

Highly Scalable: Handles occasional API requests efficiently.

User-Friendly Frontend: Provides real-time order status updates for customers.

Cost-Effective: Reduces operational costs by using compute resources only on demand.

# Technologies Used

Azure Functions (Python)

Azure SQL Database

Python (Flask/FastAPI) for API logic

Azure API Management (optional for enhanced security and monitoring)

Frontend (React.js/HTML + JS, depending on implementation)

# Installation & Setup

Azure Subscription

Python 3.x

Azure CLI & Azure Functions Core Tools

SQL Server or Azure SQL Database

#  Clone the Repository
git clone <repository_url><br>
cd azure-functions-order-api

# Install Dependencies
pip install -r requirements.txt

# Set Up Environment Variables
Create a .env file and add the following details:

# Run Locally
func start

# Deploy to Azure
az login<br>
az functionapp create --resource-group <resource_group> --consumption-plan-location <location> --runtime python --name <function_name> --storage-account <storage_name><br>
func azure functionapp publish <function_name><br>

# Example Request
curl -X GET https://your-function-app.azurewebsites.net/api/order-status/12345

# Example Response
{<br>
    "order_id": "12345",<br>
    "status": "Shipped",<br>
    "estimated_delivery": "2024-07-10"<br>
}

# Contribution

Fork the repo & create a new branch.

Commit changes and push to the branch.

Create a pull request.
