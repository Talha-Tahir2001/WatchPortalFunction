# WatchPortalFunction

## Overview

WatchPortalFunction is an Azure Function implemented in C# that serves as an HTTP-triggered endpoint for retrieving watch information. It allows users to query for details of a watch based on a model ID provided in the query string.

## Features

- Retrieve watch information using HTTP GET or POST requests.
- Handles requests with a query parameter `model` to specify the watch model.
- Returns watch details as a JSON response.
- Logs information about incoming requests.

## Technologies Used

- C#
- Azure Functions
- ASP.NET Core
- Newtonsoft.Json

## Prerequisites

- [.NET SDK](https://dotnet.microsoft.com/download) installed on your machine.
- [Azure Functions Core Tools](https://learn.microsoft.com/en-us/azure/azure-functions/functions-run-local) for local development and testing.
- [Azure Account](https://azure.microsoft.com/free/) for deploying the function to Azure.

## Getting Started

### Clone the Repository

```bash
git clone https://github.com/your-username/WatchPortalFunction.git
cd WatchPortalFunction
```
## Build and Run Locally

1.  Open the project in your preferred IDE (such as Visual Studio or Visual Studio Code).
    
2.  Ensure you have the Azure Functions Core Tools installed for local development.
    
3.  Run the function locally using the following command:
		`func start`		
4. The function will be available at 			`http://localhost:7103/api/WatchInfo`.
## Usage

### Sending Requests

-   To retrieve watch details, send an HTTP GET or POST request to the function URL with a `model` parameter.
**Example Request:**
`GET http://localhost:7071/api/WatchInfo?model=abc`
### Example Response
-   If the `model` parameter is provided:
    `Watch Details: abc, Solid, Titanium, Roman, Silver, 15` 
    
-   If the `model` parameter is missing:    
    `Please provide a watch model in the query string`
## Deployment

To deploy the function to Azure:

1.  Create a Function App in the Azure Portal.
    
2.  Publish the function to Azure using Visual Studio or the Azure CLI.
    `func azure functionapp publish <YourFunctionAppName>`
3. Once deployed, you can access the function using the URL provided by Azure.
    

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any improvements or bug fixes.
## For Future

-   **Database Integration**: Implement database connectivity to retrieve watch details dynamically based on the model ID.
-   **Authentication**: Add authentication and authorization to restrict access to the API.
-   **Enhanced Logging**: Improve logging capabilities to track usage metrics and potential errors.
-   **Error Handling**: Add comprehensive error handling and user-friendly error messages.
-   **Extended Features**: Introduce new features such as watch comparison, recommendations, and detailed specifications.
-   **UI Development**: Create a user-friendly web interface to interact with the API.
## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For questions or feedback, please contact talha666tahir@gmail.com.
