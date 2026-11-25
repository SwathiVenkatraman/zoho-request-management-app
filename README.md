# Request Management App

A simple request tracking app built with **Zoho Creator** and **Deluge**. Users submit a request through a form, receive a confirmation email, and get another email when the status of their request changes.

## Features
- Request form with name, email, title, description, priority (Low, Medium, High) and status (New, In Progress, Completed)
- Report page listing all submitted requests
- Automatic confirmation email when a request is submitted
- Automatic email when a request moves to In Progress or Completed

## How it works
1. A user submits the **Request Form**.
2. A workflow runs on successful submission and sends a confirmation email using a Deluge `sendmail` script.
3. When a record is edited and its status becomes *In Progress* or *Completed*, a second workflow sends a status update email.

## Tech used
Zoho Creator, Deluge scripting

## Screenshots
![Request form](screenshots/request-form.png)
![All requests report](screenshots/all-requests-report.png)
![Workflows](screenshots/workflows.png)
![Confirmation email](screenshots/email-request-received.png)
![Status update email](screenshots/email-status-update.png)

## Deluge scripts
- [Request received email](scripts/request-received-email.deluge)
- [Status update email](scripts/status-update-email.deluge)

## What I learned
- Building forms, reports and workflows in a low-code platform
- Writing Deluge scripts that read form values and send emails
- Debugging a script error caused by a mismatched field link name
