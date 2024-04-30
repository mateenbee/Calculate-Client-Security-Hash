This repository contains a UiPath automation workflow for interacting with the ACME System 1 web application. The automation follows a series of steps to log in, access the dashboard, retrieve work items, process specific tasks of WI5 type, generate security hashes, and update their status.

## Overview

RPA built on REFramework - uses an orchestrator queue to upload queue items.

The automation workflow performs the following steps:

- **Open ACME System 1 Web Application:** Launches the ACME System 1 web application.
- **Login to System 1:** Logs into System 1 with the provided email and password.
- **Access Dashboard:** Navigates to the dashboard, where the user can select a specific menu item.
- **Access Work Items Listing:** Retrieves all available tasks to be performed and outputs the work items.
- **Process WI5 Activities:**
  - **Open Details Page:** Opens the details page of each WI5 activity to retrieve client details.
  - **SHA1 Hash Generation:** Opens a SHA1 generator webpage and provides input (ClientID and ClientCountry) to generate the client's security hash.
  - **Retrieve Security Hash:** Retrieves the client security hash value from the webpage.
  - **Update Work Item:** Updates the status of the work item to "Completed" and adds a comment with the obtained security hash.
  - **Continue with Next WI5 Activity:** Proceeds to process the next WI5 activity until all are completed.
