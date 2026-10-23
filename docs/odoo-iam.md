# Odoo for Docusign IAM
Learn how to install, configure, and use the Odoo Extension for Docusign to seamlessly synchronize customer records and agreement data between Docusign and your Odoo ERP.
## Overview
The Odoo Extension for Docusign integrates your Odoo ERP database with Docusign App Center and eSignature workflows. It enables automated record verification, customer lookup, and automated data entry during and after agreement signing.
## How to Install and Configure
### Step 1: Locate the Odoo App in Docusign App Center
![Odoo app listing in Docusign App Center](assets/01-odoo-app-center.png) 

In your Docusign account, navigate to **App Center** and search for **Odoo** by ePillars Systems. 

![Install App action](assets/02-install-app.png)

Click **Install App**.
### Step 2: Connect Your Odoo Account
1. Click **Connect Account**. <br>
<img src="assets/03-connect-account.png" width="500" alt="Connect Account">  <br>
3. Click **Install and Authorize**. <br>
<img src="assets/04-install-and-authorize.png" width="500" alt="Install and Authorize dialog">  <br>
4. Choose **Private** or **Shared** as the connection type, then click **Next**.<br>
<img src="assets/05-connection-type.png" width="500" alt="Choose a connection type">   <br>
5. Enter a name for the connection and click **Login**. <br>
<img src="assets/06-connection-login.png" width="500" alt="Name the connection and log in">  <br>
7. On the next page, enter the Odoo instance login details and click **Submit**.<br>
<img src="assets/07-odoo-login-details.png" width="500" alt="Enter Odoo instance login details">   <br>
- When prompted to establish a connection, enter your target Odoo server credentials:
- **Odoo Database URL:** Your Odoo instance URL (for example, `https://mycompany.odoo.com`)
- **Database Name:** The target Odoo database name (for example, `mycompany`)
- **Username:** Your Odoo user account email or username
- **Password:** Your Odoo user password or API key
  
### Step 3: Grant User Consent<br>
<img src="assets/08-oauth-consent.png" width="500" alt="Odoo OAuth consent screen">  <br/>
- After submitting your login details, review the requested access permissions on the Odoo OAuth Consent Screen and click **Allow Access** to establish the connection.
## How to Use the App
- In the workflow builder, click **Add Step**, then choose **Read from Odoo** or **Writeback to Odoo** based on the workflow requirement.

#### 1. Search and Select Records
Use the **Read from Odoo** action in Docusign workflows to query contacts by ID, name, email, or phone number directly from your active Odoo database.

<img src="assets/10-search-records.png" width="500" alt="Search and select Odoo records">   <br>

#### 2. Choose Read from Odoo
<img src="assets/09-read-from-odoo.png" width="500" alt="Choose Read from Odoo">   <br>
#### 3. Create and Update Records
Choose the **Writeback to Odoo** step to create or update customer records in Odoo.

1. Select the connection. <br>
<img src="assets/11-select-connection.png" width="500" alt="Select the Odoo connection"> 

2. Select the fields.
![Select Odoo fields](assets/12-select-fields.png)  <br>
3. Map the fields for the corresponding create or update action.
![Map fields for create or update](assets/13-map-fields.png)  <br>
4. Create rules that identify the matching or filtering criteria. <br>
<img src="assets/14-matching-rules.png" width="500" alt="Configure matching or filtering rules"> 

## Frequently Asked Questions

### Is my Odoo password stored by Docusign?
- No. Passwords are processed securely over encrypted SSL connections to authenticate XML-RPC sessions and generate OAuth access tokens. Your credentials are never shared with third parties.
### What Odoo data models are supported?
- The extension currently supports Contacts and Customers. Support for Sales Orders and Invoices can be enabled upon request.
### How do I revoke access?
- You can disconnect or delete the connection at any time from **Docusign App Center → Connected Apps**.
## Need Help or Custom Support?
- If you encounter any issues configuring your Odoo connection or require custom workflow integration, please reach out to our team:
- **Email Support:** [support@epillars.com](mailto:support@epillars.com)
- **Contact Portal:** [https://www.epillars.com/contact](https://www.epillars.com/contact)
