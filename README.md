# Azure Function Example

This is meant to be an example on how to setup and run an Azure Function Project. 
Once you initialize the project and select your trigger you should upload it to a github repo and setup the repo inside an Azure Function.

## Quick Setup
```
 1. Clone Repo
 2. Create Azure process with github deployments enabled connected to the new repo
 3. Go through all prompts and save.
 4. This will create a github workflow in your project.
 5. 12/16/2023 Github workflow might fail to push your code back to Azure. This is due to having no tests.
 6. Just remove this line `npm run test --if-present` in `.github/workflows/main_nameofworkflow.yml`
```

## Installation (If you want to start from scratch and generate yourself)

```bash
# Use the following command to initialize a new Node.js project.
npm init

# Install the Azure Functions Core Tools by running the following command in the Terminal window.
npm install -g azure-functions-core-tools

# Use the following command to create a new Azure Functions project in your project folder
func init --worker-runtime node

# Add a new Azure Function to your project by running the following command in the Terminal window
func new

# Will prompt you asking what your trigger is. Typically use HTTP Trigger, and then follow the prompts to create the function.
# Write your Azure Function code in the code file that was generated for the function (Project Name/index.js

# Once you have written your Azure Function, use the following command to test it locally
func start
```

# Testing

For this example after "func start" it will be running the function locally.
Try the below links and see the code working in index.js:
[http://localhost:7071/api/HttpTrigger](http://localhost:7071/api/HttpTrigger)

[http://localhost:7071/api/HttpTrigger?name=yo](http://localhost:7071/api/HttpTrigger?name=yo)
