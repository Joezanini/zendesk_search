# Zendesk Search

Welcome to **Zendesk Search**, a React-based application designed to enhance your Zendesk Support experience by enabling efficient search and interaction with tickets. This README provides detailed instructions on how to set up, run, and use the application.

---

## Table of Contents
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Usage Instructions](#usage-instructions)
- [Development Workflow](#development-workflow)
- [License](#license)

---

## Prerequisites

Before running the application, ensure you have the following installed:

1. **Node.js** (LTS version recommended)
2. **npm** (comes with Node.js)
3. **Zendesk CLI (`zcli`)** for managing Zendesk apps
4. Access to **Zendesk Support Agent Workspace**

---

## Getting Started

Follow these steps to set up and run the Zendesk Search application:

### 1. Clone the Repository
```bash
git clone <repository_url>
cd zendesk_search
```

### 2. Install Dependencies
In the root directory of the project, run:
```bash
npm install
```

### 3. Start the React Application
To start the React app, use the following command in the root directory:
```bash
npm run dev
```

### 4. Launch the Zendesk App Server
In a **separate terminal**, navigate to the `app_local` folder:
```bash
cd app_local
zcli apps:server
```

This command starts the local Zendesk app server, which integrates with the Zendesk Agent Workspace.

---

## Usage Instructions

Once both servers are running, follow these steps to use the Zendesk Search app:

### 1. Sign in to Zendesk Support
Open your browser in **private/incognito mode** and sign in to your Zendesk Support account.

### 2. Open a Ticket
Navigate to the Agent Workspace and open a new or existing ticket. The URL should look like this:
```
https://{subdomain}.zendesk.com/agent/tickets/{ticket_id}
```

### 3. Enable Zendesk App Integration
Append the following query parameter to the ticket URL and reload the page:
```
?zcli_apps=true
```
The final URL should look like this:
```
https://{subdomain}.zendesk.com/agent/tickets/{ticket_id}?zcli_apps=true
```

### 4. View the Zendesk Search App
Click on the **Apps** icon within the Zendesk Agent Workspace. The Zendesk Search app should now be visible and ready for use.

---

## Development Workflow

### Restarting the App
- If you make changes to the React code, stop and restart the `npm run dev` process to see updates.
- Similarly, restart `zcli apps:server` if changes are made to the `app_local` folder.

### Debugging
Use browser developer tools to inspect and debug issues. Monitor both the browser console and the terminal where the app is running for error messages.

