# CST8917 – Lab 1: Azure Functions Text Analyzer

**Course:** CST8917 – Serverless Applications  
**Student:** Saizal Saini<br>
**Student Number:** 041168394 

---

## Demo Video Link

Here is the Link: 
https://youtu.be/35VeZGgPkpo
## Overview

This project is an Azure Functions application developed using Python.  
It implements an HTTP-triggered **Text Analyzer API** that processes input text and returns statistics such as word count, character count, sentence count, and estimated reading time.

The function is developed and tested locally using **Azure Functions Core Tools** and **Azurite**, then deployed to **Microsoft Azure**.

---

## Features

- HTTP-triggered Azure Function
- Accepts text via query string or JSON request body
- Returns structured JSON analysis results
- Runs locally and in Azure

---

## Technology Stack

- Python 3.12
- Azure Functions (Python v2 programming model)
- Azure Functions Core Tools
- Azurite (Azure Storage Emulator)
- Visual Studio Code

---

## Project Structure

1. function_app.py contains the main Azure Functions application code, including the HTTP‑triggered functions such as TextAnalyzer (and later GetAnalysisHistory).

2. requirements.txt lists the Python packages required by the function; these dependencies are installed automatically during deployment to Azure.

3. local.settings.json stores environment variables and connection strings used for local development and is excluded from source control for security reasons.

4. .funcignore specifies which files and folders should be excluded when deploying the function to Azure.

5. .gitignore prevents unnecessary or sensitive files (such as virtual environments and local settings) from being committed to Git.

6. The .venv directory holds the Python virtual environment used during development.

7. README.md provides documentation explaining the project, how to run it locally, and how to use the available endpoints.

8. DATABASE_CHOICE.md (Part 2) documents the selected Azure database, justification, and cost considerations.

---

## Running the Project Locally

### Prerequisites
Ensure the following are installed:

- Python 3.12  
- Visual Studio Code  
- Azure Functions Core Tools  
- Azure Functions extension for VS Code  
- Azurite (Azure Storage Emulator)

### Steps

1. Open the project folder in **Visual Studio Code**.

2. Create or verify the `local.settings.json` file  
   (this file is not committed to Git):

   ```json
   {
     "IsEncrypted": false,
     "Values": {
       "FUNCTIONS_WORKER_RUNTIME": "python",
       "AzureWebJobsStorage": "UseDevelopmentStorage=true"
     }
   }
3. Start the Azurite storage emulator:<br>
In VS Code: F1 → Azurite: Start

4. Start the Azure Function:<br>
Press F5 in VS Code OR<br>
Run the following command in the terminal:<br>
 func start

 5. The function will be available locally at:
 http://localhost:7071

 6. Test the function using a browser, curl, or REST client:

 http://localhost:7071/api/TextAnalyzer?text=Hello world

 7. Stop the function by pressing Ctrl + C in the terminal.

 ---
 ---

 ## Summary

 In this lab, an Azure Functions application was successfully developed, tested, and deployed using Python. The project demonstrated the complete serverless development workflow, including local development with Azure Functions Core Tools and Azurite, implementation of an HTTP‑triggered Text Analyzer function, and deployment to Microsoft Azure. Through this exercise, key concepts such as event‑driven architecture, environment configuration, and cloud deployment were reinforced, providing practical experience with building and managing serverless applications.

 ---
 ---

 # THANKS
